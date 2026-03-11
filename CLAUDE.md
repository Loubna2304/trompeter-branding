# Trompeter24.de E-Bike Branding Tool

## Projekt
- **Webseite:** trompeter24.de (NICHT trompeterhaus24.de)
- **Zweck:** Branding-Tool für Social-Media-Bilder und -Videos
- **Datei:** `/Users/ki/Claude/Trompeter24.de/index.html` (Single-File Web-App)
- **Live-URL:** https://loubna2304.github.io/trompeter-branding/
- **GitHub Repo:** https://github.com/Loubna2304/trompeter-branding
- **GitHub User:** Loubna2304 (loubna@el-faouzi.de)

## Branding-Konzept
- E-Bike-Bereich soll **getrennt vom Autohaus** gebrantet werden
- Autohaus-Farben (Rot #C7001A, Blau #004A80, Grün #b5e941) werden NICHT verwendet

## Farbschema E-Bikes
- **Schwarz (#1a1a1a)** — Hauptfarbe (Waldbike-Logo ist schwarz, geometrische Dreiecke)
- **Orange (#ff6e00)** — Akzentfarbe (i:SY Markenfarbe)
- **Weiß** — Text
- Quelle: Analyse der Partner-Marken Waldbike + i:SY

## E-Bike Partner-Marken
- **Waldbike**: Schwarzes Logo, überlappende Dreiecke, minimalistisch, aus dem Schwarzwald
- **i:SY**: Orange (#ff6e00) als Markenfarbe, Montserrat Font, kompakte E-Bikes

## Trompeter24.de Webseite-Infos
- Autohaus + Werkstatt + E-Bikes in Lünen-Brambauer
- VW Service Partner, 40+ Jahre Erfahrung
- E-Bike Unterseiten: Waldbike, i:SY Bike, Fahrrad-Service, Dienstrad-Leasing
- Kontakt: info@trompeter24.de, 0231 99 94 40-0
- Social: Google, Facebook, Instagram, LinkedIn, YouTube

## Tool-Features
- Drag & Drop Upload (JPG, PNG, WebP, MP4, WebM)
- **4 Design-Varianten (alle Fahrrad-/E-Bike-thematisch):**
  1. **Rahmen** — Orange Eck-Klammern + Gradient + Akzentlinie + Text
  2. **Rad** — Stilisiertes Fahrrad-Rad (Felge + 12 Speichen + Nabe mit "e") unten rechts, Text links daneben
  3. **Speichen** — Kompakter Speichen-Burst (14 Speichen) aus der Ecke unten rechts, orange Bögen, Text im Strahlbereich
  4. **Kettenkranz** — Kompaktes Fahrrad-Kettenblatt (20 schmale Zähne, 4-Arm Spider modern, Schraubenlöcher, "e" in Nabe), Text links daneben
- **Individuelle Design-Wahl pro Datei** — Dropdown in jedem Queue-Item, nicht nur global
- Einstellbare Balkenhöhe, Transparenz, Bildformat, Qualität
- Batch-Verarbeitung, Vorschau, Download
- Font: Montserrat (wie i:SY)
- Komplett auf Deutsch

## Design-Historie
- **Minimal** (dezenter Balken) und **Bold** (diagonale Streifen) wurden entfernt — Kunde fand sie nicht überzeugend
- Ursprünglich Swoosh-Design inspiriert von Autohaus Rheims (Facebook) — wurde als "alt/Fernsehtechnisch" empfunden und durch moderne Bike-Designs ersetzt
- Kunde wünscht sich **Fahrrad-Icons/-Elemente** im Branding, keine abstrakten Swooshes
- Kettenkranz v1 war zu groß + wirkte wie Lokomotiv-Zahnrad → v2 kleiner (9% statt 14%), schmale Zähne, 4-Arm statt 5-Arm
- Speichen v1 Linien waren zu lang → v2 kompakter (25% statt 45% Reichweite)
- Referenz: Autohaus Rheims (Moers) und Auto Franken (VW) für Wasserzeichen-Konzept auf Facebook
- Entwürfe wurden dem Kunden (Christoph + Andreas) in Social-Media-Gruppe zur Abstimmung geschickt

## Kunde / Kommunikation
- Ansprechpartner: **Christoph** und **Andreas** (Social-Media-Gruppe)
- Kommunikation: **informell, Du-Form**, locker
- Entwürfe zur Abstimmung geschickt (4 Designs, jeweils mit demselben Beispielbild)
- Wartet auf Feedback der Gruppe

## Video-Verarbeitung
- MediaRecorder mit **voller Originalauflösung** (kein Downscaling)
- **Hohe Bitrate** (8-10 Mbps) für gute Qualität
- VP9 Codec bevorzugt, VP8 als Fallback
- FFmpeg.wasm wurde getestet, war aber viel zu langsam (10+ Min) — verworfen
- Output: WebM (Bilder: JPG/PNG/WebP wählbar)

## Design-Referenz
- Kunde hat ein Beispielbild gezeigt (Screenshot: trompeter_ebike_post.jpg)
- Stil: Eck-Klammern oben, "TROMPETER" groß unten, "trompeter24.de | E-BIKES" mit Akzentlinie
- Inspiration: Facebook-Posts von Autohaus Rheims (Logo-Badge mit Swoosh unten rechts) und Auto Franken

## Technische Notizen
- Single-File HTML App (kein Build-Tool nötig)
- Gehostet via GitHub Pages (Branch: main, Path: /)
- Git Config im Repo: Name "Loubna", Email "loubna@el-faouzi.de"
- `drawBranding()` akzeptiert einen optionalen `design`-Parameter (für pro-Datei-Auswahl)
- Jedes Queue-Item speichert `item.design` — bei Design-Änderung wird Status auf "pending" zurückgesetzt
- Text in allen Designs hat Auto-Skalierung, damit nichts abgeschnitten wird
- Noch NICHT gepusht — wird erst nach Kunden-Feedback gepusht
