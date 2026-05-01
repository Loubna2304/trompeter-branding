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
- Etablierter Claim: **"E-BIKES AUS DEM AUTOHAUS"** (von Andi/Andreas bestätigt)
- Logo analog der Visitenkarte von Andreas

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
- **5 Design-Varianten:**
  1. **Rahmen** — Orange Eck-Klammern + Gradient + Akzentlinie + Text
  2. **Rad** — Stilisiertes Fahrrad-Rad (Felge + 12 Speichen + Nabe mit "e") unten rechts, Text links daneben
  3. **Speichen** — Kompakter Speichen-Burst (14 Speichen) aus der Ecke unten rechts, orange Bögen, Text im Strahlbereich
  4. **Kettenkranz** — Kompaktes Fahrrad-Kettenblatt (20 schmale Zähne, 4-Arm Spider modern, Schraubenlöcher, "e" in Nabe), Text links daneben
  5. **Autohaus** — "E-BIKES AUS DEM AUTOHAUS" Logo-Stil (nach Visitenkarte von Andreas)
- **Individuelle Design-Wahl pro Datei** — Dropdown in jedem Queue-Item, nicht nur global
- Einstellbare Balkenhöhe, Transparenz, Bildformat, Qualität
- Batch-Verarbeitung, Vorschau, Download
- Font: Montserrat (wie i:SY)
- Komplett auf Deutsch

## Design 5: Autohaus — ✅ FERTIG
- **Logo:** Gemini-generiertes PNG mit transparentem Hintergrund (1200x250, ~237KB Base64)
- **Farben:** Fahrräder links+rechts in Orange (#ff6e00), Text "E-BIKES AUS DEM AUTOHAUS" in Weiß
- **Rendering:** Direkt als PNG mit Alpha-Transparenz auf Gradient — kein `lighten` compositing mehr nötig
- **Logo-Größe:** 65% der Bildbreite, zentriert
- **"trompeter24.de"** dezent unter dem Logo (weiß, 45% Opacity)
- **Funktion:** `drawDesignAutohaus()` — einfaches `drawImage()`, keine manuellen Orange-Kreise
- **Historie:** Altes Visitenkarten-JPEG (signal-2026-03-11-175630.jpeg) wurde durch Gemini-Logo ersetzt (2026-03-23). Pixelweise Färbung von JPEGs hat nie sauber funktioniert (JPEG-Artefakte).

## Design-Historie
- **Minimal** (dezenter Balken) und **Bold** (diagonale Streifen) wurden entfernt — Kunde fand sie nicht überzeugend
- Ursprünglich Swoosh-Design inspiriert von Autohaus Rheims (Facebook) — wurde als "alt/Fernsehtechnisch" empfunden und durch moderne Bike-Designs ersetzt
- Kunde wünscht sich **Fahrrad-Icons/-Elemente** im Branding, keine abstrakten Swooshes
- Kettenkranz v1 war zu groß + wirkte wie Lokomotiv-Zahnrad → v2 kleiner (9% statt 14%), schmale Zähne, 4-Arm statt 5-Arm
- Speichen v1 Linien waren zu lang → v2 kompakter (25% statt 45% Reichweite)
- Referenz: Autohaus Rheims (Moers) und Auto Franken (VW) für Wasserzeichen-Konzept auf Facebook
- Entwürfe wurden dem Kunden (Christoph + Andreas) in Social-Media-Gruppe zur Abstimmung geschickt
- **2026-03-14:** Feedback von Andi (Andreas) — will etablierten Claim "E-BIKES AUS DEM AUTOHAUS" mit Logo von Visitenkarte nutzen → neues Design 5 "Autohaus" erstellt

## Kunde / Kommunikation
- Ansprechpartner: **Christoph** und **Andreas** (Social-Media-Gruppe)
- Kommunikation: **informell, Du-Form**, locker
- **Andreas (Andi):** Hat Feedback gegeben (2026-03-14) — will "eBikes aus dem Autohaus" Branding mit etabliertem Logo (Visitenkarte)
- Entwürfe zur Abstimmung geschickt — Design 5 "Autohaus" basierend auf Andis Feedback

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
- **Autohaus-Logo:** signal-2026-03-11-175630.jpeg (Visitenkarte Andreas) — geteiltes Fahrrad mit "E-BIKES AUS DEM AUTOHAUS"

## Logo-Dateien
- **Original:** `/Users/Shared/Logo E-Bike.png` (2220x464, RGBA) — schwarzer Hintergrund, Bikes orange, Text weiß
- **Transparent:** `/Users/Shared/Logo E-Bike transparent.png` — schwarzer Hintergrund entfernt (mit geglätteten Kanten), für CapCut & Video-Editing
- **Motiv:** Zwei E-Bikes (links Hinterrad mit Stecker, rechts Vorderrad mit Batterie/Blitz), Text "E-BIKES AUS DEM AUTOHAUS" in der Mitte

## Social Media Posting

### Posting-Rhythmus
- **3x pro Woche** (z.B. So / Di / Do oder So / Di / Fr)
- Mix aus Reels (Video) und Foto-Posts
- Zielgruppe: **Generation X** (ca. 45-60 Jahre)
- Plattformen: Instagram & Facebook
- Bearbeitung: **CapCut** (Free Version) für Videos, **Branding-Tool** für Fotos
- Freigabe über **Signal-Gruppe** (Christoph + Andreas)
- **Caption + Signal-Nachricht-Workflow:** Texte als `.txt` auf Desktop ablegen (`caption_xxx.txt` + `signal_freigabe_xxx.txt`) → Datei mit TextEdit öffnen → Cmd+A, Cmd+C → in Insta/FB/Signal einfügen. Vermeidet Terminal-Renderer-Artefakte beim Copy-Paste.

### Posting-Zeiten
- Sonntag: 10-12 Uhr
- Dienstag: 18-20 Uhr
- Donnerstag: 12-14 Uhr
- Freitag: 18-20 Uhr

### Medien-Album
- **Ordner:** `/Users/ki/Claude/Trompeterhaus Album Kopie/`
- **Top-Auswahl:** `/Users/ki/Claude/Trompeterhaus Album Kopie/Top Bilder Social Media/`
- Fertige Reels werden dort als `Trompeter24 Reel DD.MM.YYYY mit logo.mp4` gespeichert

### Bereits gepostete/verwendete Medien
- **KW13 (24.03.-30.03.2026):**
  - Mo 24.03.: IMG_7386.mov (Dropper-Sattel Trick)
  - Do 27.03.: IMG_8044.mov (Erste-Person-Fahrt am Kanal)
  - So 29.03.: IMG_7396.mov (E-Bike + Live-Band) — **VIRAL: ~18.000 Views auf Instagram** (Bike-Challenge "Wie lange hältst du dich drauf?")
- **KW14 (31.03.-06.04.2026):**
  - Fr 04.04.: Trompeter24 Reel für 04.04.2026.mp4 (fertig)
  - So 06.04.: IMG_7062.mov — Reel "Bike-Challenge" (Wie lange hältst du dich drauf?)
  - Di 08.04.: IMG_7047.jpeg — Foto "Hund im Lastenrad" (Design 5 Autohaus)
- **KW16 (13.04.-19.04.2026) — Festival-Posts:**
  - Sa 18.04.: Live-Dreh beim DEW21 Festival — **Baumstamm-Challenge** mit mehreren Teilnehmern (Lila-Helm „12,4 kg", Beige-Shirt „14 kg", Weinrot)
  - So 19.04.: **3 Reels** aus dem Baumstamm-Material gepostet (vor Festivalende 17 Uhr) + Countdown-Stories dazwischen
- **KW17 (20.04.-26.04.2026) — Festival-Nachlauf aus Archiv 2025:**
  - Sa 25.04.: IMG_7091.mov (Action am Stand, Kunde auf buntem Bike) — Caption-Hook „Samstagmorgen, Sonne raus, Bike raus"
  - So 26.04.: IMG_7081.mov (Kunde auf orange Waldbike, Probefahrt) — Caption-Hook „Guck dir das Grinsen an"
  - Freigabe-Nachricht an Christoph + Andreas via Signal am 21.04.2026 (Captions als Fließtext mitgeschickt, direkt kopierbar)
- **KW18 (27.04.-03.05.2026) — Live-Material aus Festival-Live-Dreh 18.04.:**
  - Di 28.04.: **DJI_20260418_141601_564_video.mov** — Reel **„Andi: Verkauft!"** (Andreas vom Festival-Stand, hebt Gravel-Bike hoch + ruft „Verkauft!", Off-Stimme „Mitarbeiter des Monats"). Throwback-Hook brückt zum Showroom Brambauer. ⚠️ **Performance: nur ~500 Views** (vs. 18k–80k bei Challenge-Reels). Throwback ohne Mitmach-Mechanik zieht bei dieser Audience nicht.
  - Story (Datum offen): **IMG_2060.mov** — Saxophonist Lünen vom 25.04. (3 Min Video → in 3× 15-Sek-Häppchen schneiden, gestaffelt posten)
  - Sa 02.05. + So 03.05.: **offen** — Festival-Archiv 2025 ist ausgereizt (IMG_7099 zu kurz/nicht spannend, IMG_7092 zu langweilig, IMG_7085 schon gepostet). Loubna holt frisches Material aus iCloud (anderer User-Account) in den Nachschub-Ordner.
  - **Reel-Schnittplan Andi:** Cold Open auf „Verkauft!" (Sek 0-1), Off-Witz „Mitarbeiter des Monats" (Sek 1-3), Andi-Charakter (Sek 3-7), Bikes-Schwenk (Sek 7-11), End-Screen schwarz „Jetzt im Showroom Brambauer" (11-15). Veralteter Original-CTA „kommt nach Dortmund" rausgeschnitten.
  - **Untertitel manuell** (CapCut Free hat keine Auto-Captions ohne Pro): „Schon eins verkauft heute?" / **VERKAUFT!** (orange, größer) / „Mitarbeiter des Monats." / „Andi vom Trompeter-Stand in Dortmund."
  - **Caption + Signal-Freigabe-Texte** liegen auf Desktop: `/Users/ki/Desktop/caption_andi_reel.txt` + `/Users/ki/Desktop/signal_freigabe_andi_reel.txt`
- **Performance-Erkenntnisse:**
  - Challenge-Format (Bike-Challenge) hat 18K+ Views gemacht → **Format funktioniert bei der Zielgruppe**
  - Kollegin Oldtimer-Video: ~40.000 Views, viele Kommentare
  - Danach Einbruch (normal nach viralem Post, Algorithmus "beruhigt sich")
  - **Andi „Verkauft!" Reel (Di 28.04.): nur ~500 Views** — Throwback ohne Challenge-Hook performt schlecht. Festival-Material ohne Mitmach-Mechanik zieht nicht.
  - **Loubnas Strategie-Frage (30.04.):** Eigener Bike-Instagram-Account erwogen. Empfehlung: erstmal nicht splitten — 500 Follower wegwerfen, USP „E-Bikes aus dem Autohaus" lebt vom Kombi-Account. Format-Problem (kein Challenge-Hook), nicht Account-Problem.

### KW16 (13.04.-19.04.2026) — DEW21 E-Bike Festival Woche
- **Festival:** DEW21 E-Bike Festival Dortmund, Fr 17.04. – So 19.04.2026
- **Trompeter-Stand:** Reinoldikirche Nord, 91m² Aussteller-Fläche
- **Neue Modelle:** Waldbike Tilia 2.0, Sorbus 2.0, Castanea (Hardtail) — alle mit Gore-Antrieb
- **Highlight-Hook:** Verlosung Waldbike im Wert €4.000 (Baumstamm-Schätzen)
- **Angebot:** Quercus statt UPE €7.000 → nur €4.500 während Festival
- **Gutscheine:** €100 beim eBike-Kauf, €49 für Inspektion, 15% auf Zubehör+Parts
- **Festival-Programm Highlights:**
  - Fr 17.04.: Eröffnung 14:00, Critical Mass 19:00
  - Sa 18.04.: E-Bike Tour "Hafen, Hopfen, Wald" 11:00, CargoBike Polo 13-17:00, Kettenkino 20:30
  - So 19.04.: Mountainbike Trial Show mit Dominik Raab (11:00, 13:00, 15:00 Katharinenstraße), Festivalende 17:00

### KW16 Reel-Plan — alle aus Festival-Archiv 2025 (Plan B falls kein Live-Material)
- **Sa 18.04.:** IMG_7042.mov (Festival-Atmosphäre, Menge in Dortmund City)
- **So 19.04.:** IMG_7085.mov (Challenge "How slow can you go?" — siehe unten, in Bearbeitung)
- **Di 21.04.:** IMG_7099.mov (3 Leute lachend auf Cargo-Bike) oder IMG_7092.mov (Service-Angle)
- **Live-Material-Priorität:** Wenn Christoph/Andreas Sa/So filmen + morgens schicken → Live-Content posten, Archiv als Backup auf spätere Wochen verschieben

### Festival-Archiv 2025 (Videos vom 12.-13.04.2025, letztes DEW21 Festival) — KOMPLETT VERBRAUCHT/UNBRAUCHBAR
- **Auswahl (6 Videos für Reels):**
  - IMG_7042.mov (Festival-Atmosphäre/Menge, morgens) — ✅ gepostet Sa 18.04.2026
  - IMG_7081.mov (Kunde auf orange Waldbike, Probefahrt) — ✅ gepostet So 26.04.2026
  - IMG_7085.mov ("How slow can you go?" Challenge) — ✅ gepostet (Datum nachtragen)
  - IMG_7091.mov (Action am Stand, Kunde auf buntem Bike) — ✅ gepostet Sa 25.04.2026
  - IMG_7092.mov (Service/Schrauber-Moment am Stand) — ❌ verworfen (50 Sek, langweilig, nichts passiert, nichts gesagt)
  - IMG_7099.mov (3 Leute lachend auf Cargo-Bike) — ❌ verworfen (14 Sek, zu schnell, nicht spannend genug für Reel)

### Baumstamm-Challenge Reels — Sonntag 19.04.2026 (UMGESETZT)
- **Quelle:** Live-Dreh vom Sa 18.04.2026 am Festival-Stand (von Christoph/Andreas gefilmt, abends geschickt)
- **Inhalt:** Mehrere Passanten schätzen das Gewicht eines Baumstamms am Fahrradlenker. Schätzungen: „12,4 kg" (Lila-Helm/POC), „glatte 14 kg" (Beige-Shirt), weitere Teilnehmer. Am Ende Schwenk auf Aufstellschild mit QR-Code + Preisen.
- **Output:** 3 separate Reels (je 12–15 Sek), einer pro Teilnehmer, alle gleiche Struktur
- **Reel-Struktur (pro Teilnehmer):**
  - 0–2 s: Hook — Person hebt Stamm, Overlay „Was schätzt du? 🪵"
  - 2–6 s: Schätzung (Originalton), Zahl als Orange-Overlay (z. B. „12,4 kg?")
  - 6–9 s: QR-Schild-Schwenk, Overlay „QR scannen & mitmachen"
  - 9–15 s: Schwarzer End-Screen (siehe Template)
- **Varianten-Hooks:** Reel 1 „Was schätzt du? 🪵" / Reel 2 „Dein Tipp? 🤔" / Reel 3 „Wer liegt näher dran?"
- **Posting-Rhythmus:** vor 12 Uhr / ~13 Uhr / ~15 Uhr, dazwischen Stories mit Countdown-Sticker
- **Learnings:** Live-Material schlägt Archiv; authentische Passanten + Originalton = hohe Retention

### End-Screen-Template „SO MACHST DU MIT" (für Gewinnspiel-Reels)
Schwarzer Hintergrund (5–6 Sek, länger als normal weil Lesezeit), wiederverwendbar:
```
SO MACHST DU MIT

1. QR-Code am Stand scannen
2. Baumstamm-Gewicht schätzen
3. Waldbike (4.000 €) gewinnen


HEUTE LETZTER TAG · bis 17 Uhr
Reinoldikirche Nord · Dortmund
```
- Überschrift weiß Bold, Nummern in Orange (#FF6E00), Dringlichkeits-Zeile Orange Bold
- Logo unten mittig, letzte 3 Sek (PNG-Overlay: `/Users/Shared/Logo E-Bike transparent.png`)
- Font: Montserrat Bold / Oswald Bold

### Reel-Produktions-Pattern (CapCut Free)
Wiederverwendbarer Workflow für Event-Content mit mehreren ähnlichen Clips:
1. **Ein Master-Reel bauen** (1 Teilnehmer, komplette Struktur inkl. End-Screen)
2. **Projekt in CapCut duplizieren** (lange drücken → Duplicate)
3. In Kopie nur Personen-Clip + Zahl-Overlay austauschen, Rest 1:1 gleich
4. Export und wiederholen
→ 3 Reels in ~40 % der Zeit statt jedes einzeln zu bauen
- **Features (Free-Version):** Text-Overlays, Pop-Animation, 9:16 Hochformat, 1080p/60fps Export, manuelle Untertitel via Text-Tool
- **NICHT in Free verfügbar (2026-04-27 bestätigt):** Auto-Captions / automatische Untertitel-Generierung ist Pro-only → Untertitel müssen manuell getippt werden, Stil einmal einstellen + per Duplicate auf weitere Blöcke übernehmen
- **Untertitel-Faustregel:** Mindestens 1,5–2 Sek pro Block, max. 6-7 Wörter pro Block, lieber wenige längere Blöcke statt viele schnelle (Gen X braucht Lesezeit)
- **Ton:** Originalton behalten (Authentizität > Trending Sound bei Gen X)
- **Übergänge:** Jump Cuts, keine Fades (passt zum Challenge-Tempo)

### Signal-Gruppe Nachricht (Festival-Filmbriefing, verschickt 16.04.2026)
- Bitte an Christoph + Andreas: Samstag Stand-Selfie, Probefahrt-Reaktionen, Baumstamm-Verlosung erklären
- Sonntag: Dominik Raab Trial Show filmen (11:00, 13:00, 15:00 Uhr)
- Instagram-Live-Option bestätigt (Account-Zugang auf Handy nötig)
- Tipp: Querformat, ruhige Hand, Clips morgens bis ~11 Uhr schicken für Mittags-Post
- Fallback: Falls kein Material → Archiv 2025 wird gepostet

### Nachschub Trompeter Ordner — Festival-Live-Dreh 18.04.2026 (gesichtet 27.04.2026)
**Ordner:** `/Users/ki/Claude/Trompeterhaus Album Kopie/Nachschub Trompeter/` — 27 Videos
**Highlights:**
- ⭐ **DJI_20260418_141601_564_video.mov** (15 MB, 40 Sek, 720x1280) — Andi „Verkauft!" am Festival-Stand → KW18 Reel Di 28.04.
- **DJI_20260418_141738_957_video.mov** (28 MB, 1:16 Min) — Pärchen am Bike-Stand, Beratungs-Stimmung
- **IMG_2060.mov** (70 MB, 3:07 Min, vom 25.04., GPS Lünen 51.6144, 7.5219) — Saxophonist in roter Jacke, IGA 2027 Schild → Story-Material
- **IMG_1877.mov** (17 MB) — Mann am offenen Sprinter, Auslieferung → Story (Behind-the-scenes)
- **IMG_1886.mov** (14 MB) — Reinoldikirche-Turm Hochformat → Story-Übergang
- **IMG_1891.mov** (38 MB, doppelt vorhanden) — Wide-Shot Festival-Platz, orange Schirme + Reinoldikirche → Story
- **IMG_1895.mov** (18 MB, doppelt vorhanden) — Pinkes Mountainbike auf Holzpodest, Waldbike-Stand → Produkt-Reel-Material
- **IMG_1897.mov** (19 MB) — Selfie Andi (Glatze/Bart/Brille) mit Trompeter-Shirt → Story / Vorstellung
- ⚠️ **IMG_1898.mov** (21 MB) — Junge Person mit lila POC-Helm — sehr wahrscheinlich „12,4 kg"-Schätzer aus Baumstamm-Challenge, **vermutlich schon verbraucht** in Reels vom 19.04.
- ⚠️ **IMG_1903.mov** (12 MB) — Zwei Männer im Gespräch, Baumstamm mit Schraubzwinge davor — Roh-Material Baumstamm, **vermutlich schon verbraucht**
- **IMG_1922.mov** (17 MB) — Person geht von hinten weg, kein klarer Bike-Bezug
- Diverse kleinere IMG-Files (1710, 1875, 1880, 1881, 1883, 1884, 1887, 1893, 1923, 1955) — noch nicht im Detail gesichtet
**Aufräum-Notiz:** IMG_1891 / IMG_1893 / IMG_1895 liegen als Original + (1)-Duplikat → kann später bereinigt werden

### Noch verfügbare Top-Videos (nicht verwendet, außerhalb Festival-Archiv)
- IMG_7373.mov (Pylonen-Parcours auf Hof)
- IMG_7385.mov (Nahaufnahme Bremshebel/Details)
- IMG_8043.mov (Erste-Person-Fahrt Waldbike, kurz)

### Noch verfügbare Top-Bilder (nicht verwendet)
- IMG_7058.jpeg — Mann präsentiert Waldbike am Messestand
- IMG_7065.jpeg — Team-Selfie am Stand (3 Leute, lustig)
- IMG_7216.jpeg / IMG_7220.jpeg — Zwei Personen auf Bikes im Autohaus-Showroom
- IMG_7381.jpeg — Messestand draußen, alle Bikes aufgereiht
- IMG_6961.jpeg — Lastenrad bei Nacht, beleuchteter Förderturm
- IMG_8372.jpeg — Selfie Waldbike auf Kanalbrücke
- IMG_0776.jpeg — Andreas mit i:SY im Showroom
- IMG_0833.jpeg — Waldbike draußen im Grünen
- IMG_9400.jpeg — Waldbike TILIA 2.0 auf Messe (Finalist CyclingWorld 2026)
- IMG_8190.jpeg — Christoph + Andreas mit Pokal im Autohaus
- IMG_1261.jpeg — Waldbike Rucksack (Zubehör, Unboxing)
- 3800531b / 8f740c4e — Erwachsener im Cargo-Bike auf Markt (lustig)
- 98E96C30.jpeg — i:SY Cargo Studiobild "Willkommen bei Trompeter"

### Content-Ideen & Hooks (Gen X)
- **Challenge/Interaktion:** "Wie lange hältst du dich drauf?" → Kommentare pushen
- **Humor + Tiere:** Hund im Lastenrad → Scroll-Stopper
- **USP Autohaus:** Bikes im Showroom zwischen Autos → "Wo andere Autos verkaufen..."
- **Nostalgie:** "Der Moment, wenn du zum ersten Mal aufsteigst" → erinnert ans erste Fahrrad
- **Spritpreise:** "Wie viel hast du diese Woche getankt?" → Alltagsbezug
- **Live-Events:** E-Bike + Konzert/Markt → spontane Erlebnisse
- **Throwback nach Events:** Festival-Material auch Tage/Wochen später posten, mit zeitlicher Brücke zum Showroom („Was nicht über die Theke ging, steht jetzt im Showroom") — verlängert Festival-Wirkung
- **Cold Open auf Höhepunkt:** Bei Reel mit Original-Audio-Highlight (z.B. „Verkauft!"-Schrei) → Höhepunkt direkt als ersten Frame zeigen, nicht chronologisch erzählen — Algorithmus-Booster für Retention

## Technische Notizen
- Single-File HTML App (kein Build-Tool nötig)
- Gehostet via GitHub Pages (Branch: main, Path: /)
- Git Config im Repo: Name "Loubna", Email "loubna@el-faouzi.de"
- `drawBranding()` akzeptiert einen optionalen `design`-Parameter (für pro-Datei-Auswahl)
- Jedes Queue-Item speichert `item.design` — bei Design-Änderung wird Status auf "pending" zurückgesetzt
- Text in allen Designs hat Auto-Skalierung, damit nichts abgeschnitten wird
- Design 5: `drawDesignAutohaus()` mit `AUTOHAUS_LOGO_B64` (PNG, transparent, Bikes orange)
- Base64-Logo geladen in `autohausLogoImg`, `autohausLogoReady` Flag
- Gepusht am 2026-03-23 — Live unter https://loubna2304.github.io/trompeter-branding/
