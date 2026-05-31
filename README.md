# 📺 TV-Watchlist — TV Schedule Tracker

A beautiful, fully self-contained TV show tracker. Search from a built-in database of 65 shows, look up any show live on the internet, organize shows into three tabs, drag to reorder, view IMDb pages, and track next-season return dates — all in a single HTML file with no account, no API keys, and no installation required.

🔗 **Live app:** <a href="https://davidfliesen.github.io/tv-watchlist" target="_blank">davidfliesen.github.io/tv-watchlist</a>

-----

## ✨ Features

### 🔍 Show Search & Lookup

- **65-show built-in database** — instant results for popular shows with all details pre-filled
- **Live internet search** — automatically queries the free [TVmaze API](https://www.tvmaze.com/api) when a show isn’t found locally; works for virtually any TV show ever made, worldwide
- **Smart fuzzy search** — finds shows from partial names or keywords, no exact spelling required
- **Two-tier results** — local “In Database” results appear instantly; “Found Online 🌐” internet results load automatically after a short pause
- **Duplicate detection** — if you try to add a show already on your list, the app warns you and directs you to the edit button instead of creating a duplicate
- **Manual entry fallback** — if a show isn’t found anywhere, enter all details yourself

### 📋 Show Cards

- **Colored show cards** — each show gets a unique persistent color theme (purple, green, teal, gold, etc.); color stays with the show regardless of position or tab
- **Card color picker** — a row of 12 color swatches at the bottom of every card lets you reassign any card’s color with one tap; selected color is highlighted with a white ring and saved immediately
- **Next Season banner** — prominent display of estimated return date, TBD, in production, or ended status with matching icons (📅 ⏳ 🎬 🏁)
- **Air day & time** — shows the broadcast day and ET time for network shows
- **Color-coded status badges** — Renewed (green), Airing (purple), In Production (blue), Final Season (gold), Ended (red), Cancelled (orange)
- **Similar show recommendations** — 3 suggestions per show based on genre; internet-found shows get genre-matched recommendations automatically from a 27-genre recommendation map
- **IMDb link** — a yellow **IMDb** button sits inline below the show title, to the left of the network/service badge; clicking it queries TVmaze for the verified IMDb ID and opens the exact show page directly; the verified ID is cached so subsequent clicks are instant
- **Clickable recommendations** — every show name in the “If you like this” section is a clickable link that looks up and opens that show’s IMDb page via the same TVmaze lookup

### 📝 Show Management

- **Three tabs** — **Now Watching** for shows you’re actively following, **Awaiting** for shows between seasons, **Completed** for finished shows; count badge on each tab
- **Move between tabs** — context-aware buttons on every card: Watching cards have **→ Awaiting** and **✓ Done**; Awaiting cards have **→ Watching** and **✓ Done**; Completed cards have **→ Watching** to reactivate
- **Tab & Position in edit** — open any card’s edit form to change its tab (Now Watching, Awaiting, or Completed) and exact position in the list from dropdowns; no dragging required
- **Add shows** — type a name and pick from search results; all fields populate automatically; new shows are added to whichever tab is active
- **Edit shows** — update any field, including tab, position, and IMDb ID, with the ✏️ button
- **Delete shows** — remove individual shows with the 🗑️ button and a confirmation prompt
- **Filter by network** — filter your list by any network or streaming service, independently per tab
- **Starts empty** — the app opens with a clean slate so you build your own personal list

### 🔀 Drag to Reorder

- **Desktop** — drag any card using the **⠿ grab handle** in the top-right to reorder it within the tab; browser ghost image is suppressed so only the CSS effect is shown
- **iPad / iPhone** — tap and hold the **⠿ grab handle**, then drag to reorder; uses non-passive touch events so dragging doesn’t scroll the page
- **Visual feedback** — the card being dragged fades and desaturates; the drop-target card bounces with an animation to show exactly where the card will land; a gold gradient bar appears at the insertion point
- Card order and color assignments are saved automatically

### 💾 Data Management

- **Auto-saved** — every change is saved to browser `localStorage` automatically
- **Save Data** — opens a modal with two options: **Download as File** (best for desktop) or **Copy to Clipboard** (best for iPad/iPhone); both save everything including tab assignments, card order, and all show data
- **Upload Data** — opens a modal with two options: **Upload from File** (select a saved `.json`) or **Paste from Clipboard** (paste text copied from Save Data); both methods fully restore your watchlist
- **Clear All** — wipe your entire watchlist with a confirmation prompt and a reminder to save first

### 🔍 View Controls

- **Zoom** — − / 100% / + bar in the view toolbar to zoom the whole page from 60% to 150%; click the percentage to reset to 100%
- **Full Screen** — enters fullscreen using the browser API (desktop Chrome, Firefox, Safari 16.4+); falls back to CSS fixed-viewport fullscreen for Chrome on iOS and older browsers that block the API; button label updates to reflect state

### 📱 Design & Accessibility

- **Mobile & tablet friendly** — responsive grid layout works on phone, tablet, and desktop
- **Large readable text** — Inter font at comfortable sizes optimized for all screen sizes
- **Sticky toolbar** — tabs and network filter bar stay at the top while you scroll
- **Zero dependencies** — single `.html` file, no build step, no server, no npm

-----

## 🚀 Getting Started

### Option A — GitHub Pages (recommended)

1. Fork or clone this repository
1. Rename the file to `index.html` in the root of your repo (if not already)
1. Go to **Settings → Pages → Source → Deploy from branch → main**
1. Your app will be live at `https://yourusername.github.io/your-repo-name` within a minute

### Option B — Run locally

Double-click `tv-watchlist.html` (or `index.html`) in any modern browser — Chrome, Firefox, Safari, or Edge. No web server, no setup, no internet required (except for TVmaze show lookups).

### Option C — Share the file directly

Send the HTML file to anyone. They open it in their browser and it works immediately. Their watchlist is saved in their own browser, completely separate from yours.

-----

## 📋 How To Use

|Action                              |How                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
|**Switch tabs**                     |Click **Now Watching**, **Awaiting**, or **Completed** at the top                                                            |
|**Change a card’s color**           |Click any of the 12 color swatches in the **Card Color** row at the bottom of the card                                       |
|**Move a show between tabs**        |Watching cards: **→ Awaiting** or **✓ Done** · Awaiting cards: **→ Watching** or **✓ Done** · Completed cards: **→ Watching**|
|**Reorder cards (desktop)**         |Drag the **⠿** handle on any card to reorder; target card bounces to show landing position                                   |
|**Reorder cards (iPad/iPhone)**     |Touch and hold the **⠿** handle, then drag; same bounce animation shows drop target                                          |
|**Change tab or position precisely**|Click ✏️ edit — Tab dropdown (Now Watching / Awaiting / Completed) and Position are at the top of the form                    |
|**Add a show**                      |Click **+ ADD SHOW**, type a name — local results appear instantly, internet results load automatically                      |
|**Show found online**               |Results labeled **Found Online 🌐** pull live data from TVmaze                                                                |
|**Show not found anywhere**         |Click “None of these — enter manually”                                                                                       |
|**Duplicate show**                  |App warns you and points to the edit button instead                                                                          |
|**View show on IMDb**               |Click the yellow **IMDb** button below the show title — it looks up the correct page via TVmaze and opens it directly        |
|**View a recommended show on IMDb** |Click any show name in the “If you like this, also watch” section                                                            |
|**Set a custom IMDb ID**            |Click ✏️ edit — enter a title ID (e.g. `tt0944947`) or paste a full IMDb URL                                                  |
|**Edit a show**                     |Click the ✏️ pencil icon on any card                                                                                          |
|**Delete a show**                   |Click the 🗑️ trash icon and confirm                                                                                           |
|**Filter by network**               |Click any network pill in the sticky toolbar (per tab)                                                                       |
|**Zoom in/out**                     |Use − / 100% / + in the view toolbar; click 100% to reset                                                                    |
|**Full Screen**                     |Click **⛶ Full Screen** in the view toolbar                                                                                  |
|**Save Data**                       |Click 💾 **Save Data** — choose **Download File** (desktop) or **Copy to Clipboard** (iPad/iPhone)                            |
|**Upload Data**                     |Click 📂 **Upload Data** — choose **Upload from File** or **Paste from Clipboard**                                            |
|**Clear All**                       |Click 🗑️ **Clear All** — removes all shows after confirmation                                                                 |
|**Learn more**                      |Click 📖 **More About App** in the header                                                                                     |

-----

## 📂 Three Tabs — Now Watching, Awaiting, Completed

The three tabs let you organize your entire TV viewing history in one place.

**Now Watching** — shows currently airing that you follow week to week. New shows are added here by default.

**Awaiting** — shows between seasons, renewed but not yet back, or ones you plan to start when they return.

**Completed** — shows you’ve finished watching, whether they ended naturally or you’re done with them. Great for your viewing history.

**Moving shows between tabs:**

|From        |Buttons available                         |
|------------|------------------------------------------|
|Now Watching|**→ Awaiting** (blue) · **✓ Done** (gold) |
|Awaiting    |**→ Watching** (green) · **✓ Done** (gold)|
|Completed   |**→ Watching** (green) to reactivate      |

Three ways to move a show:

1. Use the tab buttons on the card for a one-tap move
1. Open ✏️ edit and change the **Tab** dropdown — also set the exact **Position** at the same time
1. Drag the card to reorder within the same tab (cross-tab moves use the button or edit form)

-----

## 🌐 Internet Show Lookup

When you type a show name that isn’t in the built-in database, the app automatically searches the internet via the [TVmaze API](https://www.tvmaze.com/api) after a short pause. Results appear in a **“Found Online 🌐”** section with a blue **WEB** badge.

Selecting an internet result auto-fills:

- Show title and network/streaming service
- Air day and time
- Current status (Airing, Ended, In Production, etc.)
- Show description
- **3 similar show recommendations** generated automatically from the show’s genre tags using a built-in 27-genre map covering Drama, Crime, Comedy, Thriller, Sci-Fi, Fantasy, Mystery, Western, Medical, Legal, Espionage, Religion, War, and more
- **IMDb ID** — TVmaze returns the verified IMDb title ID, so the IMDb button and any clicked recommendation tags link directly to the correct IMDb pages

The “Next Season” field is left for you to fill in, since TVmaze doesn’t track future season dates.

-----

## 🗄️ Built-in Show Database

The built-in database includes 65 popular shows across all major networks and streaming services. Searching these is instant and fully offline.

**Broadcast:** ABC, CBS, NBC, FOX  
**Streaming:** Netflix, Prime Video, Hulu, Max, Paramount+, Apple TV+, Disney+, Peacock, FX / Hulu

For any show not in the database, the live TVmaze search covers essentially every TV show ever broadcast or streamed anywhere in the world.

-----

## 💾 Data Management

Your watchlist saves automatically to browser `localStorage` on every change. The data toolbar provides three additional controls:

**💾 Save Data** — opens a modal with two options:

- **📁 Download as File** — downloads a dated `.json` file (e.g. `tv-watchlist-2026-05-22.json`) directly to your device. Works best on desktop browsers. On iPad/iPhone the browser may block downloads — use Copy instead.
- **📋 Copy to Clipboard** — copies the full watchlist as JSON text. Paste into Notes, Messages, or any app to keep a backup. Use **Paste from Clipboard** in Upload Data to restore it later. A scrollable text area is also shown for manual select-all-and-copy if the clipboard API is blocked.

**📂 Upload Data** — opens a modal with two options:

- **📁 Upload from File** — opens a file picker to select a previously downloaded `.json` file. Works best on desktop.
- **📋 Paste from Clipboard** — paste JSON text you previously copied from Save Data into a text area, then tap **Load from Pasted Text**. Best option for iPad/iPhone.

**🗑️ Clear All** — removes every show after a two-step confirmation with a reminder to save first.

> **Tip:** Before switching browsers or clearing your list, use **Save Data → Copy to Clipboard** (iPad/iPhone) or **Download as File** (desktop) first. Tab assignments, card order, IMDb IDs, and all show data are preserved in the backup.

-----

## 🔒 Privacy

- **Your watchlist data never leaves your device** — stored only in your browser’s `localStorage`
- No analytics, no tracking, no cookies, no ads
- No account, no login, no email address required
- Show **search queries** go to the free [TVmaze API](https://www.tvmaze.com/api) — no personal data included, no account needed
- Clearing your browser’s site data will reset the watchlist to empty

-----

## 🛠️ Technical Details

|Item               |Detail                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|Stack              |Vanilla HTML + CSS + React 18 (via CDN)                                                                                                                   |
|JSX transpilation  |Babel Standalone (via CDN)                                                                                                                                |
|Storage            |Browser `localStorage` (auto-save + manual export/import)                                                                                                 |
|Fonts              |Google Fonts — Inter + Bebas Neue                                                                                                                         |
|Show database      |65 hardcoded shows with full metadata                                                                                                                     |
|Internet search    |[TVmaze API](https://www.tvmaze.com/api) — free, no key required, CORS-enabled                                                                            |
|Recommendations    |27-genre built-in map for genre-matched suggestions                                                                                                       |
|Tabs               |Now Watching / Awaiting / Completed — stored as `tab` field per show, persisted in localStorage                                                           |
|Card colors        |Stored as `_colorIdx` per show in localStorage; assigned at load time; user-selectable via 12-swatch picker on each card                                  |
|Drag & drop        |HTML5 drag with blank canvas `setDragImage` override (suppresses browser ghost) + non-passive touch events on ⠿ handle; `@keyframes` bounce on drop target|
|Fullscreen         |Real Fullscreen API (desktop) + webkit prefix + CSS fixed-viewport fallback (iOS Chrome)                                                                  |
|iOS save           |Copy-to-clipboard modal fallback when browser blocks file downloads                                                                                       |
|Tab & Position edit|Dropdowns in edit form for precise tab switching and list positioning                                                                                     |
|Zoom               |CSS `zoom` property, 60%–150% in 10% steps                                                                                                                |
|IMDb links         |TVmaze `singlesearch` API used on click to get verified `externals.imdb` ID; cached per show after first lookup; rec tags use same lookup                 |
|External calls     |Google Fonts (cosmetic only) + TVmaze API (show search only) + IMDb (opens in new tab on click)                                                           |
|File size          |~107 KB (single file, everything included)                                                                                                                |
|Browser support    |Chrome, Firefox, Safari, Edge (any modern browser)                                                                                                        |
|Starts with        |Empty list — users build their own from scratch                                                                                                           |

-----

## 📄 License

MIT License — see [License Text](#-license-text) below.

This software is provided **“as is”**, without warranty of any kind. You are free to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies for any purpose.

-----

## 👨‍💻 About the Developer

**David Fliesen** — *SunTzu* — Sole Proprietor, **Cibola Studios**  
Summerville, South Carolina

David is a Hybrid Generative AI Multimedia Developer with a background spanning U.S. Navy Combat Camera photojournalism, 20+ years in multimedia production, and DoD simulation and virtual agent development. He completed Purdue Online / Simplilearn’s Applied Generative AI Specialization and actively builds AI-powered applications across web, mobile, and immersive platforms.

**Background & Skills**

- 🎖️ U.S. Navy Combat Camera — photojournalism and visual media
- 🎮 DoD simulation & virtual agents — Army Research Lab, Sonalysts (MEDATAR, Sim Wars, Project MOSES, MMOWGLI)
- 🤖 Generative AI development — LangChain, LangGraph, Groq, OpenAI, Anthropic
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
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```