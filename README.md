# LiIon Battery Configurator

Ein interaktives Tool zur Planung und Visualisierung von Li-Ion Akkupacks (optimiert für eFoils).

## Features
- **Zellen-Datenbank**: Verwaltung von Zelltypen (Samsung 30Q, Molicel P42A, etc.) mit Preisstaffelung (Einzel vs. 100 Stk).
- **Gehäuse-Datenbank**: Hinterlegen von Bauraum-Maßen (L x B x H) und Preisen.
- **Pack-Konfigurator**:
    - Eingabe von serieller (S) und paralleler (P) Verschaltung.
    - Physisches Layout (Zellen pro Reihe) wählbar.
    - Anordnung: **Grid** oder **Honeycomb** (versetzt).
    - Automatische Rastermaß-Berechnung (z.B. 22.5mm für 21700er Halter).
- **Visualisierung**: Echtzeit-SVG Vorschau mit Bauraum-Check (blinken bei Überschreitung).
- **Wirtschaftlichkeit**: Berechnung von Gesamtkosten, Wh und €/kWh.
- **Vergleich**: Speichern mehrerer Konfigurationen zum direkten Vergleich.
- **Datenhaltung**: Lokale Speicherung im Browser (LocalStorage) sowie JSON Export/Import.

## Nutzung
Einfach die `index.html` in einem modernen Webbrowser öffnen. Es sind keine externen Abhängigkeiten oder Server erforderlich (Tailwind & DaisyUI werden via CDN geladen).

## Technischer Stack
- HTML5 / CSS3 (Tailwind CSS, DaisyUI)
- Vanilla JavaScript
- SVG für die Grafiken
