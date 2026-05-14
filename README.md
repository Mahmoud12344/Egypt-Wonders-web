# 🏛️ Egypt Wonders

> *A cinematic travel discovery website showcasing Egypt's most remarkable landmarks across 9 geographic regions — built with pure HTML5, CSS3, and vanilla JavaScript. Zero frameworks. Zero build tools.*

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)  ![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

---

![Hero](./project_reedme/hero.png)

---

## ✨ Features

- **Cinematic hero** — fullscreen autoplay video with staggered fade-in text
- **9 Region cards** — hover reveals description, image zooms in
- **Dynamic landmark grid** — 90+ landmarks loaded from JSON via `fetch()`
- **Quick preview modal** — native `<dialog>`, no library needed
- **Landmark detail page** — image gallery, sticky sidebar, breadcrumb nav
- **Dark mode** — one-click toggle, persisted in `localStorage`
- **Desert paper texture** — SVG noise background, pure CSS, zero image files
- **Scroll reveal animations** — fade-in via `IntersectionObserver`
- **Per-region accent colors** — Cairo gets terracotta, Alexandria gets Mediterranean blue, etc.

---

## 🖼️ Screenshots

<table>
  <tr>
    <td><strong>Home — Region Cards</strong></td>
    <td><strong>Region Page — Light Mode</strong></td>
  </tr>
  <tr>
    <td><img src="./project_reedme/home.png"/></td>
    <td><img src="./project_reedme/gov.png"/></td>
  </tr>
  <tr>
    <td><strong>Region Page — Dark Mode</strong></td>
    <td><strong>Quick Preview Modal</strong></td>
  </tr>
  <tr>
    <td><img src="./project_reedme/cairo.png"/></td>
    <td><img src="./project_reedme/popup.png"/></td>
  </tr>
  <tr>
    <td colspan="2" align="center"><strong>Landmark Detail Page</strong></td>
  </tr>
  <tr>
    <td colspan="2" align="center"><img src="./project_reedme/deitals.png" width="80%"/></td>
  </tr>
</table>

---

## 🗺️ Regions

| Region | Landmarks |
|--------|-----------|
| Cairo | 22 |
| Giza & Pyramids | 12 |
| Luxor & Thebes | 12 |
| Aswan & Nubia | 10 |
| Sinai & Red Sea | 10 |
| Alexandria | 9 |
| Western Desert | 9 |
| Upper Egypt | 5 |

---

## 🚀 Running Locally

> You need a local server because the site uses `fetch()` to load JSON — browsers block that on `file://` URLs.

```bash
git clone https://github.com/Mahmoud12344/Egypt-Wonders-web.git
cd Egypt-Wonders-web
python3 -m http.server 8000
```

Then open **http://localhost:8000**

---

## 🛠️ Tech Stack

| | |
|-|-|
| Structure | HTML5 — semantic elements, `<dialog>`, `aria-*` |
| Styling | CSS3 — custom properties, Grid, Flexbox, keyframes |
| Logic | Vanilla ES6+ — `fetch()`, `IntersectionObserver`, `localStorage` |
| Data | JSON — `regions.json` + `landmarks.json`, no database |
| Fonts | Google Fonts — Playfair Display + Inter |

---

## 📁 Structure

```
├── index.html          # Home — hero + region cards
├── region.html         # Dynamic landmark grid (via ?id=)
├── landmark.html       # Gallery, sidebar, breadcrumbs
├── blog.html
├── contact.html
├── auth.html
├── css/
│   ├── global.css      # Design system, dark mode, nav
│   ├── home.css
│   ├── landmarks-grid.css
│   └── landmark.css
├── js/
│   ├── nav.js          # Dark mode toggle, active links
│   ├── region.js       # Fetch + render landmarks, modal
│   ├── landmark.js     # Fetch + render detail page
│   └── reveal.js       # Scroll animations
└── assets/
    ├── data/           # regions.json, landmarks.json
    ├── images/
    └── videos/hero-bg.mp4
```

---

<p align="center">Egypt Wonders · Fourth Semester Web Project · 2026</p>