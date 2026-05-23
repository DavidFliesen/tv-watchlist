# 📺 My Watchlist — TV Schedule Tracker

A beautiful, fully offline TV show watchlist tracker with a 65-show database, smart search, colored cards, and next-season return dates. No account required. No API keys. No tokens. Just open it in a browser and go.

-----

## ✨ Features

- **65-show built-in database** — search by name and all details fill in automatically
- **Smart fuzzy search** — finds shows even from partial names or keywords
- **Next Season info** — shows estimated return dates, TBD status, or ended/cancelled
- **Add / Edit / Delete** — fully manage your personal watchlist
- **Colored show cards** — each show gets a unique color theme for easy scanning
- **Network filter bar** — filter your list by CBS, Netflix, Prime Video, etc.
- **Status badges** — color-coded Renewed, Airing, In Production, Ended, Cancelled
- **Similar show recommendations** — 3 suggestions per show
- **Auto-saved** — your watchlist persists in browser localStorage automatically
- **Save Data** — download your entire watchlist as a `.json` backup file anytime
- **Upload Data** — restore a previously saved `.json` file to reload your watchlist
- **Clear All** — wipe your watchlist with a confirmation prompt (with tip to save first)
- **Mobile friendly** — responsive layout works on phone, tablet, and desktop
- **Zero dependencies** — single HTML file, no build step, no server needed

-----

## 🚀 Getting Started

### Option A — GitHub Pages (recommended)

1. Fork or clone this repository
1. Make sure the file is named `index.html` in the root of the repo
1. Go to **Settings → Pages → Source → Deploy from branch → main**
1. Your app will be live at `https://yourusername.github.io/your-repo-name`

### Option B — Run locally

Just double-click `tv-watchlist.html` (or `index.html`) in any modern browser — Chrome, Firefox, Safari, or Edge. No web server needed.

### Option C — Share the file directly

Send the HTML file to anyone. They open it in their browser and it works immediately. Their watchlist is saved in their own browser.

-----

## 📋 How To Use

|Action              |How                                                                        |
|--------------------|---------------------------------------------------------------------------|
|Add a show          |Click **+ ADD SHOW**, type a name, pick from the search results            |
|Show not in database|Click “Enter manually” to fill in your own details                         |
|Edit a show         |Click the ✏️ pencil icon on any card                                        |
|Delete a show       |Click the 🗑️ trash icon and confirm                                         |
|Filter by network   |Click any network pill in the toolbar                                      |
|**Save Data**       |Click 💾 **Save Data** in the data toolbar — downloads a `.json` backup file|
|**Upload Data**     |Click 📂 **Upload Data** — restore a previously saved `.json` file          |
|**Clear All**       |Click 🗑️ **Clear All** — removes all shows after a confirmation prompt      |
|Your data           |Auto-saved to your browser’s localStorage on every change                  |

-----

## 🗄️ Show Database

The built-in database includes 65 popular shows across all major networks and streaming services:

**Broadcast:** ABC, CBS, NBC, FOX  
**Streaming:** Netflix, Prime Video, Hulu, Max, Paramount+, Apple TV+, Disney+, Peacock, FX

Includes shows from these genres: drama, comedy, thriller, sci-fi, procedural, fantasy, action, mystery, and more.

If a show isn’t in the database, use the manual entry form — you can fill in all fields yourself and it saves exactly like any other show.

-----

## 💾 Data Management

Your watchlist is automatically saved to browser `localStorage` as you make changes. The data toolbar (below the network filter bar) gives you three additional controls:

**Save Data** — exports your full watchlist as a dated `.json` file (e.g. `my-watchlist-2026-05-22.json`). Use this to back up your list, move it to another browser or device, or share it with someone else.

**Upload Data** — loads a `.json` file you previously saved. This completely replaces your current watchlist with the contents of the file. The app validates the file before applying it.

**Clear All** — removes every show from your watchlist after a confirmation prompt. The dialog reminds you to save a backup first. This action cannot be undone.

> **Tip:** Before clearing or switching browsers, always use **Save Data** first. Then use **Upload Data** on the new browser to restore everything instantly.

-----

## 🔒 Privacy

- **No data leaves your device** — ever
- No analytics, no tracking, no cookies
- No account, no login, no email required
- Your watchlist lives only in your own browser’s `localStorage`
- Clearing browser data will reset your watchlist to the defaults

-----

## 🛠️ Technical Details

|Item             |Detail                                                    |
|-----------------|----------------------------------------------------------|
|Stack            |Vanilla HTML + CSS + React 18 (via CDN)                   |
|JSX transpilation|Babel Standalone (via CDN)                                |
|Storage          |Browser `localStorage`                                    |
|Fonts            |Google Fonts — Inter + Bebas Neue                         |
|External calls   |Google Fonts only (purely cosmetic — app works without it)|
|File size        |~50 KB (single file)                                      |
|Browser support  |Chrome, Firefox, Safari, Edge (any modern browser)        |

-----

## 📄 License

MIT License — see [LICENSE](#license-text) below.

This software is provided **“as is”**, without warranty of any kind. You are free to use, copy, modify, and distribute it for any purpose.

-----

## 👨‍💻 About the Developer

**David Fliesen** — *SunTzu* — Sole Proprietor, **Cibola Studios**  
Summerville, South Carolina

David is a Hybrid Generative AI Multimedia Developer with a background spanning U.S. Navy Combat Camera photojournalism, 20+ years in multimedia production, and DoD simulation and virtual agent development. He completed Purdue Online / Simplilearn’s Applied Generative AI Specialization and actively builds AI-powered applications across web, mobile, and immersive platforms.

**Background & Skills**

- 🎖️ U.S. Navy Combat Camera — photojournalism and visual media
- 🎮 DoD simulation & virtual agents — Army Research Lab, Sonalysts (MEDATAR, Sim Wars, Project MOSES, MMOWGLI)
- 🤖 Generative AI development — LangChain, LangGraph, Groq, OpenAI, Anthropic
- 📱 Meta Quest VR developer
- 🎵 Suno AI music creator
- 🎙️ Voice over artist & character animator
- 📰 Creator of *Sisters of Summerville* — a daily AI-generated comic strip

**Find David Online**

|Platform   |Link                                                                        |
|-----------|----------------------------------------------------------------------------|
|Portfolio  |[davidfliesen.github.io](https://davidfliesen.github.io)                    |
|LinkedIn   |[linkedin.com/in/fliesen](https://linkedin.com/in/fliesen)                  |
|GitHub     |[github.com/DavidFliesen](https://github.com/DavidFliesen)                  |
|Comic Strip|[sisters-of-summerville.github.io](https://sisters-of-summerville.github.io)|

-----

## 📜 License Text

```
MIT License

Copyright (c) 2026 David Fliesen / Cibola Studios

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```