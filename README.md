# Ceasar Riko — Portfolio

[![Live site](https://img.shields.io/badge/live-rikopriyo.github.io-B8F256?style=flat-square)](https://rikopriyo.github.io/)

Personal portfolio of **Ceasar Riko Priyo Susantio**, a Visual Communication Design (DKV) student based in Surabaya, Indonesia — graphic designer and content editor.

Neo-brutalist single-page site with a retro desktop / collage aesthetic: taped polaroid strips, floating OS folders, case-study modals, and an interactive CV.

## Live site

**https://rikopriyo.github.io/**

Hosted with GitHub Pages (user site repo `rikopriyo.github.io`, branch `main`, folder `/ (root)`).

## Upload checklist (GitHub web, tanpa Git)

- [ ] Repo baru dibuat, visibility **Public**
- [ ] Semua 10 file di-upload ke **root** repo (jangan dalam subfolder)
- [ ] `index.html` ada di root
- [ ] **Settings → Pages** → Source: *Deploy from a branch* → `main` / `(root)` → **Save**
- [ ] URL `https://<username>.github.io/<repo>/` sudah dibuka dan gambar tampil

## Features

- Single-file site (`index.html`) — no build step, no dependencies to install
- Sticky brutalist navbar with smooth-scroll sections and scroll-spy active link
- Light / dark theme toggle in the navbar — animated circular reveal from the button, remembers the visitor's choice, defaults to the system preference, and updates the browser theme color
- Thin lime scroll-progress line along the bottom edge of the navbar
- Filterable "Featured Works" cards (FTIRS ITS & Andrewarna Advertising)
- Case-study modal with per-project details, impact, and tools
- School Projects grid with category filters (UI/UX, Photography, Motion Graphic, 3D Model, Graphic Design), click-to-open detail modal, zoomable photos, and arrow-key navigation
- Scroll-reveal, card press, and modal pop-in animations (respects `prefers-reduced-motion`)
- Keyboard-friendly details: skip-to-content link, visible focus rings, and a back-to-top button after scrolling
- Person structured data (JSON-LD) and social preview image alt text
- Custom neobrutalist cursor with contextual labels (`OPEN`, `DETAILS`, `ZOOM`) on desktop
- School Project cards tilt toward the pointer and zoom their image on hover
- Hero polaroid straightens and lifts on hover
- Infinite skills marquee strip between Featured Works and School Projects (pauses on hover)
- Live Surabaya (WIB) clock in the footer
- Interactive CV modal + print / save-as-PDF support
- Fully responsive (mobile → desktop)
- Photo fallbacks via `onerror` so layout never breaks if an image is missing

## Tech

| Layer | Used |
|---|---|
| Styling | [Tailwind CSS](https://tailwindcss.com) via CDN + custom config (CSS-variable theme colors, fonts, brutal shadows) |
| Icons | [Font Awesome 6.5](https://fontawesome.com) |
| Fonts | Google Fonts — Space Grotesk, Plus Jakarta Sans, JetBrains Mono, Caveat |
| Scripts | Vanilla JavaScript (filters, modals, clipboard, print) |

## Project structure

```
portofolio-riko-priyo/
├── index.html                          # whole site (markup + styles + scripts)
├── foto-ceasar-riko.jpeg               # hero portrait + CV modal photo
├── prof-priyo-suprobo.jpeg             # FTIRS polaroid
├── rector-award-prof-juwari.jpg        # FTIRS polaroid
├── clash-of-flavors.jpg                # FTIRS polaroid
├── proses-editing-konten-andrewarna.jpg # Andrewarna polaroid
├── foto-proses-laser-akrilik.jpg       # Andrewarna polaroid
├── survey-wahyu.jpg                    # Andrewarna polaroid
├── logo-affinity.png                   # Affinity by Canva skill icon
└── README.md
```

## School project photos

The **School Projects** section (between Featured Works and Skills) has 10 cards. Each card loads an image from this folder:

| Card | File name |
|---|---|
| Figma Project | `tugas-figma.jpg` |
| Photography | `fotografi.jpg` |
| After Effects Project | `tugas-after-effects.jpg` |
| Desain Baju | `tugas-baju.jpg` |
| 3D Project | `tugas-3d.jpg` |
| Nirmana Project | `nirmana-buaya.jpg` |
| Graphic Design — Kira Jojo | `kira-jojo.jpg` |
| Graphic Design — Rock | `rock-design.jpg` |
| Graphic Design — Raichu | `raichu-design.jpg` |
| Graphic Design — Yveltal | `yveltal-design.jpg` |

Click (or Tab + Enter) any card to open a detail modal with a short description, tool chips, and prev/next navigation. Click the photo inside the modal to zoom 200%, and press `Esc` to close.

The filter pills above the grid narrow the collection by category: **All**, **UI/UX**, **Photography**, **Motion Graphic**, **3D Model**, and **Graphic Design**. The project counter updates to the number of visible cards, and prev/next navigation inside the modal stays within the filtered set.

If a file is missing, the card falls back to a colored icon tile. Images are cropped to a 4:3 frame (`object-cover`), except poster and wide-strip images which use `object-contain`.

## Run locally

Just open `index.html` in a browser, or serve the folder:

```bash
# Python 3
python -m http.server 5500
# then open http://localhost:5500
```

```bash
# Node.js
npx serve .
```

## Deploy to GitHub Pages

1. Push this folder to a GitHub repository (public).
2. Go to **Settings → Pages**.
3. Under *Build and deployment*, choose **Deploy from a branch** → branch `main`, folder `/ (root)`.
4. Save. The site goes live at `https://<username>.github.io/<repo>/` within a minute or two.

## Editing tips

- Image files use kebab-case names (no spaces) so URLs stay clean across hosting providers.
- Theme colors are CSS variables: `:root` holds the light palette and `html.dark` overrides it with the dark palette. Change both if you add a new accent color.
- Fonts and shadow presets live in the `tailwind.config` block at the top of `index.html`.
- Polaroid thumbnails are fixed to a `4:5` frame; portrait sources fit perfectly, landscape sources are cropped with `object-cover` (or letterboxed with `object-contain`).

## Contact

- Email — rikopriyo58@gmail.com
- Phone — 089695976479
- Instagram — [@softmodification](https://instagram.com/softmodification)
- Location — Surabaya, Indonesia
