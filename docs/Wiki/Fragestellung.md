# Fragestellung

## Leitfrage

**Wie lässt sich die Größenabhängigkeit der optischen Eigenschaften (Bandlücke, Emissionsfarbe) von Halbleiter-Quantum-Dots in einer interaktiven 3D-Simulation realisieren und für die universitäre Lehre visualisieren?**

## Unterfragen

### 1. Physikalisches Modell
Welche quantenmechanischen Approximationen (unendlicher sphärischer Potentialtopf, effektive Masse, Coulomb-Korrektur nach Brus) liefern eine praktikable und numerisch stabile Beschreibung der Energieniveaus in direkten Halbleiter-Nanokristallen?

### 2. Visualisierung
Wie transformiert man die abstrakten Eigenzustände (Wellenfunktionen, Energieniveaus) in eine intuitive 3D-Darstellung, die räumliche Wahrscheinlichkeitsdichten und das zugehörige Emissionsspektrum gleichzeitig zeigt?

### 3. Softwarearchitektur
Welche modulare Architektur (MVVM, Service-orientierte Kernlogik) erlaubt eine wartbare und erweiterbare Implementierung in C# / WPF, so dass später weitere Materialien, Potentialprofile oder Exportformate hinzugefügt werden können?

### 4. Validierung
Wie lässt sich die Korrektheit der physikalischen Berechnungen (Eigenwerte, Bandlücken-Verschiebung) gegen analytische Lösungen und Literaturwerte sicherstellen?

## Abgrenzung

**Im Scope:**
- Unendlicher sphärischer Potentialtopf als quantenmechanisches Modell
- Zinkblende-Kristallstruktur (CdSe, InP, PbS) als geometrische Basis
- Echtzeit-3D-Visualisierung der Atompositionen und Wahrscheinlichkeitsdichten
- Interaktive Parametersteuerung (Radius, Material)
- LaTeX-Export der Ergebnisse und Formeln

**Out of Scope:**
- Endliche Potentialtöpfe (zu hoher numerischer Aufwand für das Zeitbudget)
- Vollständige Coulomb-Matrixelemente und Multipartikel-Effekte
- Erweiterte Materialien außerhalb der vorselektierten Gruppe
- Web-basierte oder plattformübergreifende Bereitstellung (reines WPF-Desktop-Tool)
