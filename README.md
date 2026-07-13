# BRAUN Möbel-Center · Azubi-Offensive 2027

Konzept-Paket von **LändleDigital** für das Erstgespräch am 13.07.2026:

| Was | Wo |
|---|---|
| 🛋️ **Azubi-Portal** (klickbarer Prototyp in BRAUN-CI) | [`index.html`](index.html) |
| 📄 **Pitch-PDF** (3 Seiten, LändleDigital-CI) | [`pitch/Azubi-Offensive-2027_BRAUN_x_LaendleDigital.pdf`](pitch/Azubi-Offensive-2027_BRAUN_x_LaendleDigital.pdf) |
| 🖨️ Druckvorlage des Pitchs (HTML → PDF) | [`pitch/pitch.html`](pitch/pitch.html) |

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
