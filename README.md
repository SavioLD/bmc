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

- **9 Standorte** suchen aktiv: 5 Häuser à 1–2 Plätze, 4 Häuser à 4–6 Plätze → **bis zu 34** für Start **09/2027** (2026 nahezu voll).
- Einzige harte Anforderung: **keine 5 in Mathe** – Rest entscheidet das persönliche Gespräch (so auch im Portal-FAQ & in den „harten Fakten“).
- CI: **Gelb/Schwarz** nach Website & Logo (schwarzes BRAUN mit gelber Kontur + BMC-Badge, als SVG nachgebaut). Zentrale = **Reutlingen**.

## Platzhalter (vor Kampagnenstart ersetzen)

- **Logo & Gelb-Ton:** CI-Nachbau. Zentral tauschbar über die CSS-Tokens oben in `index.html` (`--gelb`, `--ink`) und die `logo__mark`-SVGs → gegen echte Logo-Datei tauschen.
- **Fotos:** beige Platzhalter-Flächen (mit „Platzhalter“-Tag) → echte Azubi-Fotos/Videos.
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
