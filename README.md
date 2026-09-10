# CommandX — Lagedashboard

Statisches, eigenständiges Dashboard (Chart.js inline, keine externen Abhängigkeiten).

Die Seite wird per GitHub Actions auf GitHub Pages veröffentlicht
(`.github/workflows/pages.yml`, Branch `claude/github-pages-publish-adux8d`).

## Raster / Bedienung

Die Module liegen in einem 12-Spalten-Snap-Raster (Zeilenhöhe 38 px, 12 px Abstand):

- **Verschieben** – Kopfzeile ziehen; die Zielzelle wird als gestrichelter Platzhalter angezeigt.
- **Skalieren** – rechte Kante, untere Kante oder die Ecke unten rechts ziehen.
- **Tastatur** – Kopfzeile fokussieren, dann Pfeiltasten (verschieben) bzw. `Shift` + Pfeiltasten (skalieren).
- Kollidierende Module weichen nach unten aus, danach fallen alle Module wieder nach oben.
- Jedes Modul hat eine Mindestgröße; kleiner lässt es sich nicht ziehen.
- Das Layout wird im `localStorage` gespeichert; **Zurücksetzen** stellt das Ausgangslayout wieder her.
- Unter 760 px Breite schaltet die Ansicht auf eine einspaltige Stapelansicht um (ohne Drag & Drop).
