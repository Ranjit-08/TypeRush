# ⚡ TypeRush — Typing Practice App

A beautiful, animated typing trainer that runs **100% locally in your browser**.
No build tools, no npm, no database — one HTML file.

![modes](https://img.shields.io/badge/modes-6-8b5cf6) ![deps](https://img.shields.io/badge/dependencies-0-22d3ee) ![size](https://img.shields.io/badge/size-~50_KB-lightgrey)

---

## 🖥️ What you need on a new laptop

The app is extremely light. You only need **2 things**:

| Requirement | Why | Check command |
|---|---|---|
| **Any modern browser** | Edge / Chrome / Firefox / Safari / Brave — you already have one | — |
| **Python 3** (only to serve the app) | Runs a tiny local web server. Nothing else is installed | `python --version` |

> 💡 Already used a real server before (VS Code Live Server, `npx serve`, WAMP/XAMPP)? Any of those work too. Python is just the simplest universal option.

### Installing Python (skip if `python --version` works)

**Windows:**
- Option A: `winget install Python.Python.3.12` (PowerShell)
- Option B: download from <https://www.python.org/downloads/> → run installer → **check "Add Python to PATH"** ✅ during install

**macOS:**
```bash
brew install python3        # if you have Homebrew
# or: xcode-select --install   (gives you python3)
```

**Linux (Ubuntu/Debian):**
```bash
sudo apt update && sudo apt install -y python3
```

---

## 🚀 Getting the app onto the new laptop

Pick **any one** of these two ways:

### Step 1 — Get the code

**Way A: Clone with Git** (recommended if Git is installed — check with `git --version`)
```bash
git clone https://github.com/Ranjit-08/TypeRush.git
cd TypeRush
```

**Way B: Download ZIP** (no Git needed)
1. Open <https://github.com/Ranjit-08/TypeRush>
2. Green **`< > Code`** button → **Download ZIP** → extract it anywhere

### Step 2 — Start the local server

Open a terminal **inside the app folder** and run:

**Windows (PowerShell or CMD):**
```powershell
python -m http.server 4780
```
*(If `python` isn't recognized on Windows, try `py -m http.server 4780`)*

**macOS / Linux:**
```bash
python3 -m http.server 4780
```

### Step 3 — Open the app

In your browser, go to:

```
http://localhost:4780
```

That's it. Start typing. 🎉

> ✅ **Even simpler option:** because the app is a single self-contained HTML file, you can also just **double-click `index.html`** — it opens and works without any server. (Fonts load from Google Fonts when online; everything else is fully offline.)

---

## 🧯 Troubleshooting

| Problem | Fix |
|---|---|
| `python` not recognized (Windows) | Use `py -m http.server 4780`, or reinstall Python with "Add to PATH" ticked |
| `Address already in use` / port busy | Another app is on port 4780 — run `python -m http.server 5000` and open `http://localhost:5000` instead |
| Page won't load | Make sure the terminal is still running (the server closes when you close it) and you're on the same laptop |
| Google fonts look different | You're offline — the app falls back to system fonts; all features still work |
| Want the server in the background (macOS/Linux) | `nohup python3 -m http.server 4780 &` |

---

## 🎮 How to use

**Modes** (pick from the home screen):

| Mode | Description |
|---|---|
| ⚡ Blitz 15s | Quick burst |
| 🚀 Classic 30s | Sprint (most popular) |
| 🏃 Marathon 60s | Endurance |
| 🎯 Sprint 25 / 50 | Finish a fixed word count |
| ✍️ Quote | Famous quotes with punctuation |

**Shortcuts:**

| Key | Action |
|---|---|
| *(first keystroke)* | Starts the clock |
| `Tab` | Restart / new test |
| `Esc` | Back to menu |
| `Ctrl` + `Backspace` | Delete the whole word |
| `Enter` (on results) | Next test |

Personal bests are saved in your browser's localStorage per mode — they move with the laptop/browser profile, not with the code.

---

## 📁 Project structure

```
TypeRush/
├── index.html   ← the entire app (HTML + CSS + JS, zero dependencies)
└── README.md    ← this file
```

## 🛠️ Built with
- Plain HTML / CSS / JavaScript — no frameworks, no build step
- JetBrains Mono + Space Grotesk (Google Fonts, optional)
- WebAudio API for keypress sounds, Canvas API for charts & confetti

---

*Runs fully locally — your keystrokes and scores never leave your machine.*
