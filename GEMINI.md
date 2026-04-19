# Projekt-Mandate (GEMINI.md)

Diese Regeln sind für alle zukünftigen Bearbeitungen durch KI-Agenten bindend.

## Grundprinzipien
1. **Single-File Policy**: Das gesamte Projekt (HTML, CSS, JS) muss in der `index.html` verbleiben. Keine Aufteilung in mehrere Dateien, es sei denn, der User verlangt es explizit.
2. **CDN Usage**: Tailwind CSS und DaisyUI werden über CDN eingebunden. Keine lokalen Node-Module oder Build-Steps.
3. **No Dependencies**: Keine zusätzlichen JS-Frameworks (React, Vue, etc.). Nur Vanilla JavaScript.
4. **Data Persistence**: `localStorage` ist der primäre Speicherort. Die Export/Import Logik muss immer alle Datenbanken (Zellen, Gehäuse, Vergleiche) umfassen.

## Berechnungs-Standards
- **Rastermaß**: 
    - 18650 = 19.5mm Standard.
    - 21700 = 22.5mm Standard.
    - Honeycomb-Offset: Horizontal = Rastermaß, Vertikal (21700) = 19.5mm.
- **Wirtschaftlichkeit**: Preis pro kWh immer auf Basis der Nominalspannung (3.7V pro Zelle) berechnen.

## UI/UX Vorgaben
- **Theme**: `data-theme="emerald"` als Default.
- **Validierung**: Visuelle Warnungen (Blinken/Rot) im SVG bei Bauraum-Überschreitung sind Kernfeature und müssen erhalten bleiben.
