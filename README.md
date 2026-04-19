# 🏛️ A16 News – Abteilung 16 Verkehr und Landeshochbau

Täglicher Newscrawler für die Abteilung 16 des Amts der Steiermärkischen Landesregierung.
Kategorien: Straßenbau, Lärmschutz, Verkehrsplanung, Landeshochbau, UVP & Recht.

---

## Dateien im Paket

```
a16-news/
├── fetch_news.py                    ← Python-Script (Root)
├── README.md
├── .github/
│   └── workflows/
│       └── daily-update.yml        ← GitHub Actions Workflow
└── docs/
    ├── index.html                  ← Website
    └── data.json                   ← Platzhalterdaten
```

---

## Schritt-für-Schritt Upload

### 1. Neues GitHub Repository erstellen
1. Gehe zu **github.com** → oben rechts **„+"** → **„New repository"**
2. Name: `A16-Verkehr-News`
3. Wähle **„Public"**
4. Klicke **„Create repository"**

### 2. Dateien hochladen
1. Im neuen Repository: **„uploading an existing file"** klicken
2. **Alle Dateien und Ordner** aus diesem ZIP hochladen:
   - `fetch_news.py` → in den Root
   - `.github/workflows/daily-update.yml` → in den `.github/workflows/` Ordner
   - `docs/index.html` → in den `docs/` Ordner
   - `docs/data.json` → in den `docs/` Ordner
3. **„Commit changes"** klicken

> **Wichtig:** Der `.github` Ordner ist versteckt — auf Mac mit **Cmd+Shift+Punkt** sichtbar machen.

### 3. Gemini API Key hinterlegen
1. Repository → **Settings** → **Secrets and variables** → **Actions**
2. **„New repository secret"**
3. Name: `GEMINI_API_KEY`
4. Value: deinen neuen Google Gemini API Key
5. **„Add secret"**

### 4. GitHub Pages aktivieren
1. Repository → **Settings** → **Pages**
2. Source: **„Deploy from a branch"**
3. Branch: **`main`**, Folder: **`/docs`**
4. **„Save"**

Nach 1–2 Minuten ist die Website live unter:
`https://DEIN-USERNAME.github.io/A16-Verkehr-News`

### 5. Ersten Lauf starten
1. Repository → **Actions** → **„A16 News Update"**
2. **„Run workflow"** → **„Run workflow"**
3. Nach ~10 Minuten erscheinen die ersten News

---

## Zeitplan
Der Job läuft täglich um **05:00 Uhr Graz** automatisch.

## Kategorien
| Kategorie | Themen |
|---|---|
| 🛣️ Straßenbau & Sanierung | Neubau, Sanierung, Tunnel, Brücken |
| 🔇 Lärmschutz | Lärmschutzwände, -fenster, UVP |
| 🚦 Verkehrsplanung | Mobilität, Radwege, ÖV |
| 🏛️ Landeshochbau | Öffentliche Gebäude, Investitionen |
| ⚖️ UVP & Rechtliches | Genehmigungen, Einsprüche |
