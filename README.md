# Hi-Light — Project Page

A static project page for **Hi-Light: A Path to High-fidelity, High-resolution Video Relighting With A Refined Evaluation Paradigm**.

## What's inside

```
.
├── index.html          # the page (single self-contained file, all CSS inline)
├── assets/             # figures extracted from the paper
│   ├── fig1_teaser.jpg     # demo: sunset gull / aurora woman
│   ├── fig2_capcut.jpg     # CapCut filters vs. Hi-Light
│   ├── fig3_framework.jpg  # overall architecture
│   ├── fig4_labdf.jpg      # LAB-DF detail
│   ├── fig5_qualitative.jpg
│   ├── fig6_plot.jpg       # SSIM vs. S_LS scatter
│   └── fig7_frequency.jpg  # frequency / temporal analysis
└── .nojekyll          # tells GitHub Pages to skip Jekyll processing
```

No build step. No dependencies. Just open `index.html`.

## Deploy to GitHub Pages

### Option A — dedicated repo (recommended)

1. Create a new repo, e.g. `hi-light-page` (or use the existing `Hi-Light` repo).
2. Push everything in this folder to the repo's default branch (`main`).
3. On GitHub: **Settings → Pages → Build and deployment**
   - **Source**: *Deploy from a branch*
   - **Branch**: `main` &nbsp;/&nbsp; **Folder**: `/ (root)`
   - Save.
4. After ~30 seconds the page is live at `https://<your-username>.github.io/<repo-name>/`.

### Option B — serve the page from inside the existing `Hi-Light` repo

If you'd rather host the page from your `lxrswdd/Hi-Light` code repo:

- **As the repo's main page** — copy `index.html` and the `assets/` folder into the repo root and follow the steps above. The page lives at `https://lxrswdd.github.io/Hi-Light/`.
- **As a `/docs` subfolder** — drop everything into a `docs/` folder, then in Settings → Pages choose **Branch: main / Folder: /docs**.
- **As a separate `gh-pages` branch** — `git checkout --orphan gh-pages`, copy the page files in, commit, push. In Settings → Pages set **Branch: gh-pages**.

### Option C — quick local preview

```bash
# any of these will do
python3 -m http.server 8000
# or
npx serve .
```

Open http://localhost:8000.

## Customising

- **Update the paper PDF link.** In `index.html`, find the "Paper" button and replace `href="#abstract"` with the URL to your PDF (e.g. an arXiv link).
- **Add a video demo.** Drop an `mp4`/`webm` into `assets/` and replace the hero `<img>` with a muted, autoplaying `<video>` element.
- **Tweak colours.** All theming lives in CSS variables at the top of `index.html` under `:root` — the warm accent is `--amber: #e89657`.
- **Fonts.** Display: *Fraunces* · body: *Instrument Sans* · mono: *JetBrains Mono*. Loaded from Google Fonts.

## License

Page template — feel free to reuse and adapt. Figures © the paper authors.
