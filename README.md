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

## Platzhalter (vor Kampagnenstart ersetzen)

- **Logo & Rot-Ton:** CI-Nachbau. Zentral tauschbar über die CSS-Tokens oben in `index.html` (`--rot`, `.logo`).
- **Fotos:** beige Platzhalter-Flächen (mit „Platzhalter“-Tag) → echte Azubi-Fotos/Videos.
- **Alle Werte mit `*`:** Vergütung, Urlaub, Platzzahlen pro Standort, 48-h-Versprechen → mit BRAUN final abstimmen.
- **Daten pflegen:** Standorte & Berufe liegen als JS-Arrays (`STANDORTE`, `BERUFE`) unten in `index.html`.

## PDF neu bauen

```bash
npm i playwright   # Chromium muss vorhanden sein
node render.mjs    # Script siehe LändleDigital-Repo bzw. Session
```

(Screenshots in `pitch/img/` entstehen aus dem Portal; danach rendert Chromium `pitch/pitch.html` als A4 quer mit `printBackground`.)

---
Erstellt von LändleDigital GmbH · Juli 2026 · Inhalte teilweise beispielhaft, siehe `*`-Fußnoten.
