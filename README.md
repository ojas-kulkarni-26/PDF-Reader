# 📖 Folio — PDF Reader

A beautiful, mobile-first PDF reader that dynamically loads books directly from this GitHub repository. No server, no backend — just open the HTML file and read.

---

## ✨ Features

| Feature | Details |
|---|---|
| 📚 **Dynamic Library** | Auto-fetches all PDFs from the repo root via GitHub API |
| 🔖 **Bookmarks** | Add, view & delete bookmarks per book — stored locally |
| 💾 **Last Page Memory** | Remembers exactly where you left off for every book |
| ▶️ **Continue Reading** | One-tap shortcut to resume your last opened book |
| 🔍 **Search** | Instantly filter books by title |
| 🌙 **Dark & Light Mode** | Toggle between themes, preference saved locally |
| 🔎 **Zoom Controls** | Pinch-friendly zoom buttons + Fit/Wide presets |
| 📍 **Jump to Page** | Skip directly to any page number |
| 👆 **Swipe Navigation** | Swipe left/right to turn pages on mobile |
| ⌨️ **Keyboard Shortcuts** | Arrow keys to navigate, `+`/`-` to zoom, `Esc` to go back |
| 📊 **Progress Bar** | Visual reading progress per book in the library grid |
| 🖼️ **Cover Thumbnails** | Auto-generates cover previews from the first page |

---

## 🚀 How to Use

### 1. Add PDFs to this repo
Upload your PDF files **directly to the root** of this repository (not in any subfolder).

### 2. Open the reader
Open `pdf-reader.html` in any modern browser (Chrome, Safari, Firefox).

> **Tip:** Host it on GitHub Pages for a permanent URL — just enable Pages in repo Settings and point it to the `main` branch root.

---

## 📱 Mobile Optimized
- Fully responsive layout (2-column grid on phones, more on tablets)
- Touch-friendly tap targets
- Swipe left/right to turn pages
- No zoom lock — use pinch gestures naturally
- Bottom navigation for easy one-thumb use

---

## 🗂️ File Structure

```
PDF-Reader/
├── pdf-reader.html       ← The entire app (single file)
├── README.md
├── YourBook.pdf          ← Add PDFs here
├── AnotherBook.pdf
└── ...
```

---

## 💡 GitHub Pages Setup

1. Go to **Settings → Pages**
2. Set Source to `Deploy from a branch` → `main` → `/ (root)`
3. Your reader will be live at:  
   `https://ojas-kulkarni-26.github.io/PDF-Reader/pdf-reader.html`

---

## 🔧 Configuration

To point the app to a different repo, edit these lines near the top of `pdf-reader.html`:

```js
const GITHUB_USER = 'ojas-kulkarni-26';
const GITHUB_REPO = 'PDF-Reader';
const GITHUB_BRANCH = 'main';
```

---

## 📦 Tech Stack

- **PDF.js** (Mozilla) — PDF rendering engine
- **GitHub Contents API** — Dynamic file listing
- **LocalStorage** — Persists reading progress, bookmarks, and theme
- Vanilla HTML / CSS / JS — Zero dependencies, zero build step

---

## ⚠️ Notes

- The GitHub API has a rate limit of **60 requests/hour** for unauthenticated use. For personal use this is more than enough.
- PDFs are fetched via `raw.githubusercontent.com` — make sure the repo is **public**.
- Cover thumbnails are generated client-side; loading time depends on PDF size.

---

*Made with ❤️ using Folio PDF Reader*
