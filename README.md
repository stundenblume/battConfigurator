# LiIon Battery Configurator

Ein interaktives Tool zur Planung und Visualisierung von Li-Ion Akkupacks (optimiert für eFoils).

## Features
- **Zellen-Datenbank**: Verwaltung von Zelltypen mit Preisstaffelung und individuellen Links zu Datenblättern/Shops.
- **Zell-Formate (Raster)**: Datenbank für Abmessungen (Grid H/V, Honeycomb-Offset, Zell-Höhe). Unterstützt Standardformate wie 18650 und 21700.
- **Gehäuse-Datenbank**: Speichern von Innenmaßen und Preisen für verschiedene Cases.
- **Intelligenter Konfigurator**:
    - Eingabe von S (Seriell) und P (Parallel) Verschaltung.
    - Physisches Layout (Zellen pro Reihe) einstellbar.
    - **Neu**: Automatisches Snake-Routing (horizontal oder vertikal) basierend auf dem Seitenverhältnis des Packs.
    - **Neu**: Dynamische Honeycomb-Rotation (90° Drehung bei vertikaler Ausrichtung).
- **Visualisierung**: 
    - Echtzeit-SVG mit Bauraum-Check.
    - Farbliche Gruppierung der Parallel-Paare.
    - Prominente Nickel-Streifen Darstellung.
- **Analyse**: 
    - Leistungsbasierte Last-Berechnung (W -> A) mit visueller Warnung (Orange/Rot).
    - Berechnung der Ausnutzung von Fläche und Volumen in Prozent.
    - Wirtschaftlichkeits-Check (€/kWh).
- **Vergleich**: Sortierbare Tabelle zum Benchmarking verschiedener Setups.
- **Datenhaltung**: LocalStorage (Browser) & JSON Export/Import.

## Nutzung
Einfach die `index.html` im Browser öffnen. Keine Installation nötig.

## Technischer Stack
- HTML5 / CSS3 (Tailwind CSS, DaisyUI)
- Vanilla JavaScript (keine Frameworks)
- SVG (dynamisch generiert)
