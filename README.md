# Ceasar Riko — Portfolio

Personal portfolio of **Ceasar Riko Priyo Susantio**, a Visual Communication Design (DKV) student based in Surabaya, Indonesia — graphic designer, photographer, and content editor.

Neo-brutalist single-page site with a retro desktop / collage aesthetic: taped polaroid strips, floating OS folders, case-study modals, and an interactive CV.

## Live site

> **Belum deploy.** Setelah aktifkan GitHub Pages, ganti baris ini dengan URL-nya,
> contoh: `https://username.github.io/portofolio-riko-priyo/`

## Upload checklist (GitHub web, tanpa Git)

- [ ] Repo baru dibuat, visibility **Public**
- [ ] Semua 10 file di-upload ke **root** repo (jangan dalam subfolder)
- [ ] `index.html` ada di root
- [ ] **Settings → Pages** → Source: *Deploy from a branch* → `main` / `(root)` → **Save**
- [ ] URL `https://<username>.github.io/<repo>/` sudah dibuka dan gambar tampil

## Features

- Single-file site (`index.html`) — no build step, no dependencies to install
- Sticky brutalist navbar with smooth-scroll sections
- Filterable "Featured Works" cards (FTIRS ITS & Andrewarna Advertising)
- Case-study modal with per-project details, impact, and tools
- Interactive CV modal + print / save-as-PDF support
- Fully responsive (mobile → desktop)
- Photo fallbacks via `onerror` so layout never breaks if an image is missing

## Tech

| Layer | Used |
|---|---|
| Styling | [Tailwind CSS](https://tailwindcss.com) via CDN + custom config (colors, fonts, brutal shadows) |
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
- Colors, fonts, and shadow presets live in the `tailwind.config` block at the top of `index.html`.
- Polaroid thumbnails are fixed to a `4:5` frame; portrait sources fit perfectly, landscape sources are cropped with `object-cover` (or letterboxed with `object-contain`).

## Contact

- Email — rikopriyo58@gmail.com
- Phone — 089695976479
- Instagram — [@softmodification](https://instagram.com/softmodification)
- Location — Surabaya, Indonesia
