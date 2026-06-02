# KI-Nutzung im Projekt Quantum Dot Studio

## Übersicht

Im Rahmen dieses Projekts werden KI-gestützte Tools als **Werkzeuge** eingesetzt, um die Entwicklungsgeschwindigkeit zu erhöhen und die Code-Qualität zu sichern. Alle wesentlichen Architekturentscheidungen, physikalischen Modelle und Algorithmen werden eigenständig entwickelt, verstanden und durch Unit-Tests verifiziert.

## Eingesetzte KI-Tools

### 1. GitHub Copilot / Claude Code (Code-Generierung)

- **Einsatzzweck**: Erstellung von Boilerplate-Code (MVVM-ViewModels, Klassengerüste, Properties), repetitive Aufgaben wie INotifyPropertyChanged-Implementierungen, XAML-Templates
- **Beitrag**: Beschleunigt die Grundstrukturierung, reduziert Tippaufwand für syntaktisch bekannte Muster
- **Kritische Prüfung**: Jeder generierte Codeblock wird vor Commit auf physikalische Korrektheit und Einhaltung der Architektur geprüft

### 2. Claude / ChatGPT (Wissensvalidierung)

- **Einsatzzweck**: Plausibilitätsprüfung physikalischer Gleichungen (Brus-Gleichung, Schrödinger-Gleichung in Kugelkoordinaten), LaTeX-Syntax-Korrektur, Erklärung komplexer numerischer Methoden (Eigenwertberechnung)
- **Beitrag**: Qualitätssicherung der Dokumentation und Formeln
- **Kritische Prüfung**: Alle Formeln werden gegen Standardlehrbücher (Bimberg, Grundmann: "Quantum Dot Heterostructures") validiert

### 3. KI-gestützte Dokumentation

- **Einsatzzweck**: Strukturierung von Wiki-Artikeln, Sprachprüfung, Formatierung von Tabellen und Listen
- **Beitrag**: Lesbarkeit und Konsistenz der Projektdokumentation

## Grenzen der KI-Nutzung

Die folgenden Bereiche werden **ausschließlich eigenständig** bearbeitet:

- Softwarearchitektur und Moduldesign
- Physikalische Modellierung und Implementierung der Gleichungen
- Unit-Tests und Verifikation der Berechnungsergebnisse
- UML-Diagramme und Softwareentwurf
- Reflexion über den Entwicklungsprozess im Wiki

## Transparenz

Jeder Commit, der signifikante KI-Unterstützung enthält, wird mit einem entsprechenden Hinweis im Commit-Message oder als Inline-Kommentar versehen. Die vollständige Dokumentation der KI-Nutzung ist in diesem Dokument nachvollziehbar.
