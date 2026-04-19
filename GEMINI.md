# Projekt-Mandate (GEMINI.md)

Diese Mandate sind strikt zu befolgen. Abweichungen nur nach expliziter Bestätigung durch den User.

## 1. Architektur & Technologie
- **Single-File Policy**: Die gesamte Applikation (Logik, Design, Struktur) lebt in der `index.html`. 
- **Framework-Verbot**: Keine Verwendung von React, Vue, Angular oder ähnlichen Frameworks. Ausschließlich Vanilla JavaScript verwenden.
- **Styling**: Tailwind CSS und DaisyUI über CDN (`https://cdn.tailwindcss.com` und `https://cdn.jsdelivr.net/npm/daisyui...`).
- **Assets**: Favicons oder Bilder müssen als SVG eingebettet (Data-URI) sein. Keine externen Asset-Dateien.

## 2. Datenbanken & Datenhaltung
- **Storage**: Alle Daten (Zellen, Formate, Gehäuse, Vergleiche) liegen im `localStorage`.
- **Datenintegrität**: 
    - Der Export/Import muss immer das gesamte Datenmodell (alle 4 Listen) abdecken.
    - Löschoperationen müssen vom User bestätigt werden.
    - Fehlende Datenfelder (z.B. durch alte Versionen) müssen in der Render-Logik abgefangen werden (Default-Werte).

## 3. Berechnungs- & Visualisierungs-Logik
- **Rastermaß-Dominanz**: Physische Berechnungen basieren primär auf den konfigurierten Rastermaßen (Grid H, Grid V, Grid Honey), nicht nur auf dem Zelldurchmesser.
- **Snake-Logic**: 
    - Das Pack muss einen kontinuierlichen Verschaltungspfad (Snake) haben.
    - Die Ausrichtung (Horizontal vs. Vertikal) entscheidet sich automatisch am Seitenverhältnis oder der P-Gruppen-Passung.
    - Die Nickel-Streifen-Visualisierung muss diesem Pfad exakt folgen.
- **Honey-Rotation**: Bei einem Wechsel von horizontaler zu vertikaler Ausrichtung muss das Honeycomb-Muster um 90° mitgedreht werden (Offset-Achse wechselt).
- **Wirtschaftlichkeit**: Alle €/kWh Berechnungen basieren auf der Nominalspannung von 3.7V.

## 4. UI/UX Standards
- **Zustand**: Alle Datenbank-Karten sind standardmäßig minimierbar (Collapse).
- **Feedback**: 
    - Bauraum-Überschreitung führt zu Blinken/Rot-Färbung im SVG.
    - Elektrische Überlast (Last/Strom Kachel) wird farblich kodiert (Orange >= 80%, Rot >= 95%).
- **Vergleich**: Die Vergleichstabelle muss sortierbar sein. Klick auf eine Zeile lädt die entsprechende Konfiguration in den Editor.
- **Versionierung**: Im Footer muss der Zeitstempel der letzten Code-Änderung unauffällig sichtbar sein.

## 5. Coding Style
- **Fehlerbehandlung**: `updateCalc()` muss in einem try-catch Block liegen, um zu verhindern, dass fehlerhafte SVG-Koordinaten die gesamte App einfrieren.
- **Funktionalität**: Logik (Berechnung) und View (DOM-Manipulation) sollten getrennt gehalten werden, soweit es die Single-File Architektur zulässt.
