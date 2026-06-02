# Entwicklungszyklus

## Phase 1: Initiierung (bis 29. Juni 2026)

- [x] GitHub-Repository anlegen
- [x] README.md mit Projektbeschreibung erstellen
- [x] Wiki-Startseite (Idee & Zielstellung) schreiben
- [x] Repository auf GitHub veröffentlicht
- [x] Betreuer (Prof. Zug, Herr Göhler) als Collaborator einladen
- [x] Entwicklungszyklus-Dokumentation im Wiki ergänzen

## Phase 2: Spezifikation & Entwurf (bis 6. Juli 2026)

- [ ] Detaillierte Fragestellung formulieren: Welche physikalischen Modelle (unendlicher vs. endlicher Potentialtopf? Welche Materialparameter?)
- [ ] Anforderungsanalyse: Funktionale / nicht-funktionale Anforderungen
- [ ] UML-Klassendiagramm: Domänenmodell (Material, QuantumDot, ElektronenZustand, LatticeEngine, Solver, Renderer)
- [ ] UML-Sequenzdiagramm: Interaktion "Benutzer ändert Radius → System berechnet → Renderer aktualisiert"
- [ ] Softwarearchitektur festlegen: MVVM-Pattern für WPF, Service-Driven Architecture für Core
- [ ] **Bestätigung der Idee und des Entwurfs durch Betreuer einholen**

## Phase 3: Implementierung (6. Juli – 30. Juli 2026)

### Sprint A: Domänenmodell & Solver (Woche 1)
- [ ] Projektstruktur in Visual Studio anlegen (.sln + 5 Projekte)
- [ ] Material-Datenbank (CdSe, InP, PbS: Bandlücke, effektive Massen, Dielektrizitätskonstante)
- [ ] Lattice-Generator (Zinkblende-Gitter, sphärische Ausschnittlogik)
- [ ] Quantenmechanischer Solver (Lösung Schrödinger-Gleichung in Kugelkoordinaten, Eigenwertberechnung)
- [ ] Unit-Tests für Solver-Modul

### Sprint B: Renderer & UI (Woche 2)
- [ ] Helix-Toolkit-Integration in WPF
- [ ] 3D-Gitterdarstellung (Atompositionen als Billboard-Spheres)
- [ ] Wahrscheinlichkeitsdichte-Cloud (Volumetrische Darstellung oder Heatmap auf Oberfläche)
- [ ] UI-Controls: Material-Auswahl, Radius-Slider, Energieanzeige
- [ ] Farbschema für Atomtypen implementieren

### Sprint C: Diagramme & Export (Woche 3)
- [ ] OxyPlot-Integration für Energieniveau-Diagramm
- [ ] Emissionsspektrum-Plot (Größenabhängige Bandlücken -> Peak-Verschiebung)
- [ ] LaTeX-Templating-Engine (String-basiert)
- [ ] Berichtsexport: Parameter, Formeln, Screenshots, Ergebnistabelle

### Sprint D: Integration & Polishing (Woche 4)
- [ ] MVVM-ViewModels für alle Ansichten
- [ ] Fehlerbehandlung und Validierung
- [ ] Performance-Optimierung (Lazy Loading, Caching)
- [ ] Dokumentation ergänzen: API-Beschreibung der Module, Tutorial für Endnutzer
- [ ] KI-Nutzungsdokumentation finalisieren

## Phase 4: Abschluss (30. Juli 2026)

- [ ] Finaler Build getestet
- [ ] Alle Wiki-Seiten vollständig
- [ ] UML-Diagramme final
- [ ] Letzter Commit auf main, Tag `v1.0.0`
- [ ] Repository-Archivierung durch Betreuer

## KI-Nutzung (laufend dokumentieren)

| KI-Tool | Einsatzzweck | Beitrag |
|---------|-----------|---------|
| GitHub Copilot / Claude Code | Code-Vorschläge, Boilerplate-Generierung für MVVM-Pattern | Beschleunigung repetitive Aufgaben |
| ChatGPT / Claude | Physikalische Formeln prüfen, LaTeX-Syntax validieren | Qualitätssicherung Dokumentation |
| Sonstige | (wird ergänzt) | |

> **Hinweis**: KI wird als Werkzeug eingesetzt, nicht als Ersatz für eigenständiges Design. Alle wesentlichen Architekturentscheidungen und komplexen Algorithmen werden eigenständig entwickelt und durch Unit-Tests verifiziert.
