# BRAUN Möbel-Center · Azubi-Offensive 2027

Konzept-Paket von **LändleDigital** für das Erstgespräch am 13.07.2026:

| Was | Wo |
|---|---|
| 🛋️ **Azubi-Portal** (klickbarer Prototyp in BRAUN-CI) | [`index.html`](index.html) |
| 📱 **Werbe-Creatives** (6 Social-Ads, fertige PNGs) | [`creatives/out/`](creatives/out) |
| 🖼️ Creative-Übersicht (alle 6 auf einen Blick) | [`creatives/creatives-uebersicht.png`](creatives/creatives-uebersicht.png) |
| 🗂️ **Creatives 4:5 als ZIP** (8 Stück, 1080×1350: 5 Collage + 3 Hero) | [`creatives/BRAUN-Azubi-Creatives-4x5.zip`](creatives/BRAUN-Azubi-Creatives-4x5.zip) |
| 📄 **Pitch-PDF** (3 Seiten, LändleDigital-CI) | [`pitch/Azubi-Offensive-2027_BRAUN_x_LaendleDigital.pdf`](pitch/Azubi-Offensive-2027_BRAUN_x_LaendleDigital.pdf) |
| 🖨️ Druckvorlage des Pitchs (HTML → PDF) | [`pitch/pitch.html`](pitch/pitch.html) |

## Das „gewisse Etwas“

- **Azubi-Check – die Verkaufs-Challenge** (Sektion `#check`): 6 anspruchsvolle Rechen-Aufgaben aus dem Verkaufsalltag (Mehrfach-Rabatt, MwSt/Netto, Anzahlung + Raten, Dreisatz) mit **Countdown pro Frage, Punkten fürs Tempo und Combo-Bonus** im Game-Look. Ergebnis = Punktzahl + Rang + „X/6 richtig“, wird an die Bewerbung angehängt → **echte Vorqualifizierung** im Funnel, ohne jemanden hart abzuweisen. Der Hebel gegen „viele Bewerbungen, aber schwache Mathe-Kenntnisse“ (anspruchsvoll genug, um wirklich zu filtern).
- **Live-Countdown** bis zum Ausbildungsstart 01.09.2027 (tickt sekündlich).
- **Azubi-Testimonials** mit illustrierten Avataren (Beispiel-Stimmen*).
- **Social-/Reel-Block**: zeigt die echten Kampagnen-Creatives in Handy-Rahmen – verbindet Ads & Portal sichtbar.
- **Konfetti** beim Absenden der Bewerbung (perfekter Moment für die Live-Demo; respektiert `prefers-reduced-motion`).

## Werbe-Creatives (zum Zuschicken)

6 Beispiel-Ads in BRAUN-CI, exakte Ad-Maße, in `creatives/out/`:

| Datei | Format | Angle |
|---|---|---|
| `creative-1-story-brand` | 1080×1920 | Slogan/Brand |
| `creative-2-feed-angebot` | 1080×1080 | 34 Plätze / Angebot |
| `creative-3-story-hook` | 1080×1920 | „Ohne Anschreiben“-Hook |
| `creative-4-feed-testimonial` | 1080×1080 | Azubi-Zitat |
| `creative-5-story-usp` | 1080×1920 | Antwort in 48 h |
| `creative-6-feed-regional` | 1080×1080 | 9 Standorte |

Neu bauen: `creatives/creatives.html` im Browser öffnen bzw. per Playwright je `.creative` als Element-Screenshot @2x exportieren.

## Im Meeting zeigen

- **Portal:** `index.html` im Browser öffnen (läuft komplett offline, alle Fonts liegen lokal).
  Demo-Highlights: Beruf-Karten → Detail-Dialog · Standort-Filter · „Hier bewerben“ übernimmt den Standort ins Formular · Formular absenden → Erfolgs-Screen mit Standort-Routing.
- **Live-Link:** In den Repo-Settings **GitHub Pages** (Branch `main`) aktivieren → Portal ist unter `https://saviold.github.io/bmc/` abrufbar, z. B. fürs iPad.
- **PDF:** liegt fertig gerendert im `pitch/`-Ordner.

## Datenstand (aus Braun-Rückmeldung, Juli 2026)

- **Nur eine Ausbildung** wird beworben: **Kaufmann/-frau im Einzelhandel** (Start 01.09.2027). Keine weiteren Stellen im Portal.
- **9 Standorte** suchen aktiv: 5 Häuser à 1–2 Plätze, 4 Häuser à 4–6 Plätze → **bis zu 34** für Start **09/2027** (2026 nahezu voll).
- Einzige harte Anforderung: **keine 5 in Mathe** – Rest entscheidet das persönliche Gespräch (nur noch im FAQ, nicht mehr als Slogan/Kachel).
- Slogan im Mittelpunkt: **„Richte dir deine Zukunft ein.“**
- CI: **Gelb/Schwarz** nach Website & Logo. Zentrale = **Reutlingen**.

## Platzhalter (vor Kampagnenstart ersetzen)

- **Logo:** ✅ Original liegt als `assets/img/braun-logo.png` im Repo und wird automatisch eingesetzt (Auto-Detect in `index.html`; SVG-Nachbau bleibt als Fallback). Gelb-Ton zentral über CSS-Token `--gelb`.
- **Bilder:** aktuell selbst erstellte Illustrationen im BRAUN-Look (SVG-Sprite oben in `index.html`) → später durch echte Azubi-Fotos/Videos ersetzen oder ergänzen.
- **Alle Werte mit `*`:** Vergütung, 48-h-Versprechen, Zuordnung welcher Standort 1–2 bzw. 4–6 Plätze hat → mit BRAUN final abstimmen.
- **Daten pflegen:** Standorte & Berufe liegen als JS-Arrays (`STANDORTE`, `BERUFE`) unten in `index.html`.

## PDF neu bauen

```bash
npm i playwright   # Chromium muss vorhanden sein
node render.mjs    # Script siehe LändleDigital-Repo bzw. Session
```

(Screenshots in `pitch/img/` entstehen aus dem Portal; danach rendert Chromium `pitch/pitch.html` als A4 quer mit `printBackground`.)

---
Erstellt von LändleDigital GmbH · Juli 2026 · Inhalte teilweise beispielhaft, siehe `*`-Fußnoten.
