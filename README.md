# 🏛️ Egypt Wonders

A high-end, cinematic travel discovery website showcasing Egypt's most
remarkable landmarks across 9 geographic regions. Built with **pure
HTML5, CSS3, and vanilla JavaScript** — zero frameworks, zero build tools.

---

## 🚀 Getting Started

### Prerequisites

| Tool | Purpose | Check |
|------|---------|-------|
| **Python 3** | Local development server | `python3 --version` |
| **Modern browser** | Chrome, Firefox, or Edge | — |
| **Git** | Version control | `git --version` |

> **Why a server?** The project uses `fetch()` to load JSON data at
> runtime. Browsers block `fetch()` on `file://` URLs for security
> reasons, so you **must** serve the files over HTTP.

 
### 1. Start the Local Server

Because this project uses the native `fetch()` API to load JSON data, you **must** serve the files over an HTTP server. Browsers block `fetch()` on local `file://` paths for security reasons.

**Start a Python Server (Standard)**
```bash
# Start a local server on port 8000
python3 -m http.server 8000
```

**Alternative Servers (If Python is unavailable)**
```bash
# Node.js (via npx)
npx -y serve . -l 8000

# PHP
php -S localhost:8000
```

### 3. View the Project
Once the server is running, open your web browser and navigate to:
[http://localhost:8000](http://localhost:8000)

---

## 📁 Project Structure

```
project/
│
├── index.html              # Home page — hero video + 9 region cards
├── region.html              # Region page — dynamic landmark grid (loaded via ?id=)
├── landmark.html            # Landmark detail — gallery, description, sidebar
├── blog.html                # Blog page (static)
├── contact.html             # Contact page with form (static)
├── color-demo.html          # Design system color palette demo
│
├── css/
│   ├── global.css           # Design system — variables, nav, footer, utilities
│   ├── home.css             # Home page styles — hero, region cards, sidebar
│   ├── landmarks-grid.css           # Region page styles — landmark grid, modal
│   └── landmark.css         # Landmark detail styles — gallery, metadata sidebar
│
├── js/
│   ├── nav.js               # Shared — navigation, dark mode toggle, active links
│   ├── region.js            # Region page — fetch landmarks, build cards, modal
│   ├── landmark.js          # Landmark detail — fetch data, populate gallery/sidebar
│   └── reveal.js            # Shared — IntersectionObserver scroll-in animations
│
├── assets/
│   ├── data/
│   │   ├── regions.json     # 9 regions with metadata
│   │   └── landmarks.json   # 90+ landmarks, pre-sorted by importance
│   ├── images/              # Landmark photographs organized by folder
│   └── videos/
│       └── hero-bg.mp4      # Compressed hero background video
│
| 
└── .gitignore
```

---

## 🎨 Design System

| Token | Value | Purpose |
|-------|-------|---------|
| `--bg-body` | `#F4EFE6` (light) / `#121212` (dark) | Page background with SVG noise texture |
| `--accent` | `#D4AF37` (metallic gold) | Buttons, tags, active links |
| `--font-heading` | Playfair Display | Headings — elegant editorial serif |
| `--font-body` | Inter | Body text — modern readable sans-serif |
| `--radius-lg` | 16px | Card corners |
| `--transition` | 0.25s ease | Hover and toggle animations |

Each region overrides `--accent` with its own color (e.g., Cairo uses
terracotta `#B85C3A`, Alexandria uses Mediterranean blue `#2266AA`).

---

## ✨ Key Features

- **Cinematic Hero** — Full-screen autoplay video with staggered fade-in text
- **9 Region Cards** — Portrait cards with cinematic hover reveals (description slides up, image zooms)
- **Dynamic Landmark Grid** — 3-column grid populated from `landmarks.json` via `fetch()`
- **Quick Preview Modal** — Native `<dialog>` with `fadeInUp` animation, centered on screen
- **Landmark Detail Page** — Image gallery, sticky metadata sidebar, breadcrumb navigation
- **Dark Mode** — One-click toggle, persisted in `localStorage`, smooth CSS transitions
- **Desert Paper Texture** — SVG noise background generated in pure CSS (zero image files)
- **Giant Watermark Typography** — Faint background text that fills empty margins
- **Scroll Reveal Animations** — Elements fade and glide up via `IntersectionObserver`
- **Per-Region Accent Colors** — Automatic color theming based on `data-region` attribute

---
 
| # | Stage | What It Covers |
|---|-------|---------------|
| 0 | Design Decisions | Approved color palette, typography, layout architecture |
| 1 | Project Setup | Folder structure, empty files, git init |
| 2 | Global CSS | Design system: variables, fonts, dark mode, nav, footer |
| 3 | Home Page | `index.html` + `home.css` — hero section, geographic groups |
| 4 | Region Page | Dynamic landmark grid, modal, pre-sorted JSON data |
| 5 | Landmark Detail | Gallery, sticky sidebar, parallel fetch |
| 6 | Blog & Contact | Static pages, form semantics |
| 7 | Polish | Local server setup, responsive tweaks, testing checklist |
| 8 | Video Hero | `ffmpeg` compression, HTML5 video attributes, CSS `object-fit` |
| 9 | Cinematic Animations | CSS transitions & keyframes, cubic-bezier, card reveals |
| 10 | Background Polish | SVG noise textures, scroll reveals, watermark typography |

---

## 📝 Tech Stack

| Layer | Technology | Notes |
|-------|-----------|-------|
| Structure | HTML5 | Semantic elements, `<dialog>`, `aria-*` attributes |
| Styling | CSS3 | Custom properties, Grid, Flexbox, `clamp()`, keyframes |
| Logic | Vanilla ES6+ JS | `fetch()`, `IntersectionObserver`, `localStorage` |
| Data | JSON | `regions.json`, `landmarks.json` — no database needed |
| Server | Python 3 `http.server` | Development only — any static server works |
| Fonts | Google Fonts | Playfair Display + Inter |

 
