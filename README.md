# Schulportal 📰

Ein schulinternes Nachrichtenportal, gehostet auf GitHub Pages. Schülerinnen und Schüler können PDF-Artikel veröffentlichen, die übersichtlich auf der Startseite angezeigt werden.

## 🚀 Live-Demo

Nach dem Deployment unter: `https://<dein-github-username>.github.io/<repository-name>/`

---

## 📁 Projektstruktur

```
schulportal/
│
├── index.html                  ← Startseite (Übersicht & PDF-Viewer)
├── README.md                   ← Diese Datei
│
├── assets/
│   ├── css/
│   │   └── style.css           ← Styling der gesamten Webseite
│   ├── js/
│   │   ├── main.js             ← Lädt Artikel & befüllt die Startseite
│   │   ├── search.js           ← Suchleisten-Logik
│   │   ├── viewer.js           ← PDF-Anzeige Logik
│   │   └── publish.js          ← Veröffentlichen-Modal
│   └── img/
│       └── logo.png            ← Schullogo (optional)
│
├── pdfs/
│   └── *.pdf                   ← Veröffentlichte PDFs
│
├── data/
│   └── articles.json           ← Metadaten aller Artikel
│
└── .github/
    └── workflows/
        └── deploy.yml          ← GitHub Action für automatisches Deployment
```

---

## 📝 Artikel veröffentlichen

### Schritt 1 – PDF hochladen
Lade dein PDF in den Ordner `/pdfs/` hoch. Wähle einen eindeutigen, beschreibenden Dateinamen (z.B. `schulausflug-bern.pdf`).

### Schritt 2 – Eintrag in articles.json
Öffne die Datei `data/articles.json` und füge einen neuen Eintrag hinzu:

```json
{
  "titel": "Mein Artikel-Titel",
  "autor": "Vorname Nachname",
  "datum": "2025-04-01",
  "datei": "mein-artikel.pdf"
}
```

> **Tipp:** Du kannst den JSON-Eintrag auch direkt über den «Veröffentlichen»-Button auf der Webseite generieren lassen.

### Schritt 3 – Pushen
Commite und pushe deine Änderungen. GitHub Actions deployt die Seite automatisch.

---

## ⚙️ GitHub Pages einrichten

1. Gehe zu deinem Repository → **Settings** → **Pages**
2. Unter **Source** wähle **GitHub Actions**
3. Die Seite ist nach dem ersten Push verfügbar

---

## 🎨 Farbpalette

| Name | Hex | Verwendung |
|------|-----|------------|
| Tief Schwarz | `#0A0A0A` | Seitenhintergrund |
| Nacht | `#1A1A2E` | Karten-Hintergrund |
| Marineblau | `#0D3B6E` | Navbar-Hintergrund |
| Kräftigblau | `#40C4FF` | Primärer Akzent / Text |
| Smaragd | `#1A6B50` | Button-Hintergrund |
| Kräftiggrün | `#00E676` | Highlights / Button-Text |

---

*Schulportal · 2025*
