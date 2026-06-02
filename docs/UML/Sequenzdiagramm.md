# UML-Sequenzdiagramm: Radius-Änderung

```mermaid
sequenceDiagram
    actor Benutzer
    participant UI as MainViewModel
    participant Solver as QuantumSolver
    participant Lattice as LatticeEngine
    participant Renderer as Renderer3D
    participant Chart as ChartEngine

    Benutzer->>UI: Slider bewegen (Radius ändern)
    UI->>Solver: CalculateEnergyLevels(R, Material)
    Solver->>Solver: Brus-Formel anwenden
    Solver->>Solver: Radiale Eigenwerte berechnen
    Solver-->>UI: EnergyLevels, Bandlücke, Wellenlänge

    UI->>Lattice: GenerateZincBlende(R, Material)
    Lattice->>Lattice: Unendliches Gitter erzeugen
    Lattice->>Lattice: FilterInsideSphere()
    Lattice-->>UI: List~Atom~

    UI->>Renderer: RenderAtoms(AtomList)
    UI->>Renderer: RenderProbabilityCloud(Grundzustand)
    Renderer-->>UI: 3D-Szene aktualisiert

    UI->>Chart: PlotEnergyLevels(EnergyLevels)
    UI->>Chart: PlotSpectrum(EmissionWellenlaenge)
    Chart-->>UI: Diagramme aktualisiert

    UI-->>Benutzer: Live-Vorschau (3D + Diagramme + Farbe)
```

## Beschreibung der Interaktion

1. **Trigger**: Der Benutzer bewegt den Radius-Slider in der WPF-UI.
2. **Berechnung**: Das ViewModel ruft den `QuantumSolver` auf, der für den neuen Radius die Energieniveaus (Brus-Korrektur) und Emissionswellenlänge berechnet.
3. **Geometrie**: Parallel wird der `LatticeEngine` aufgerufen, der ein neues sphärisches Gitterstück generiert.
4. **Visualisierung**: `Renderer3D` zeichnet Atome und Wahrscheinlichkeitswolke neu. `ChartEngine` aktualisiert Energieniveau-Balken und Spektrum.
5. **Feedback**: Der Benutzer sieht alle drei Darstellungen (3D-Struktur, Energiediagramm, Emissionsspektrum) in Echtzeit aktualisiert.

## Parallelisierung

Der Berechnungsprozess (Solver + LatticeEngine) läuft synchron im UI-Thread innerhalb von <200 ms. Bei Bedarf könnte ein `Task.Run` die Berechnung in den Hintergrund verlagern und das Ergebnis per `Dispatcher`-Rückruf zurückliefern. Für den vorliegenden Scope (R ≤ 10 nm, ~1000 Atome) ist keine Asynchronität nötig.
