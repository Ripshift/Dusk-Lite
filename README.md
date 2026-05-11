# Dusk — Campaign Compendium

A static site for the gothic roleplaying setting **Dusk**: a tabbed study guide ("Atlas Spread") plus a kit of printable / interactive handouts for the game-master's desk.

## Contents

```
index.html             # landing page
study-guide.html       # the Atlas Spread — tabbed, no scrolling, print-ready
handouts/
  light-clock.html     # interactive five-phase dial
  moon-tide.html       # 15-day lunar + 6-stage tidal reference
  lineage-paper.html   # printable Drow house writ
  blood-compact.html   # printable Coven bond with wax seal
  web-exposure.html    # five-tier Web visibility dossier
assets/
  dusk.css             # shared paper / gilt / wax styling
  bg-threepanel.png    # background plate
```

All pages are self-contained HTML — no build step, no JS framework. Fonts (IM Fell English, Cormorant Garamond) load from Google Fonts.

## Deploying to GitHub Pages

1. Push this folder to the root of a GitHub repository (or to any subdirectory — Pages can serve from `/`, `/docs`, or any branch).
2. In **Settings → Pages**, set the source to the branch you pushed (e.g. `main`) and the folder (`/` or `/docs`).
3. Wait for the green check. Your site is live at `https://<user>.github.io/<repo>/`.

### If you serve from `/docs`
Move the contents of this folder into a `docs/` directory at the repo root, commit, and select `/docs` in the Pages settings.

### If you want it at the user/org root site
Push to a repo named `<user>.github.io` and the site will be served at `https://<user>.github.io/`.

## Local preview

Any static server works. From this directory:

```
python3 -m http.server 8000
# or
npx serve .
```

Then open `http://localhost:8000/`.

## Printing

The Atlas Spread is set up to print at **tabloid landscape**; each tabbed panel becomes its own two-page spread. The handouts are set up at **US letter portrait**. Use your browser's print dialog (Cmd/Ctrl-P) and set "Background graphics" to on so the gilt, wax and parchment textures survive.

## Editing

Content lives directly in the HTML — no CMS, no markdown step. Open any file in your editor of choice; the structure is straightforward and the comments label each section.

To change colors, type, or the paper-and-gilt palette, edit the variables at the top of `assets/dusk.css`.
