# SIGNUM — Commissioned Golf Goods

A luxury identity brand expressed through golf. This is the brand site: one page, no build
step, no dependencies — pure HTML/CSS/JS with self-hosted fonts.

## Structure

- `index.html` — the entire site (styles and scripts inline by design)
- `assets/fonts/` — Cormorant Garamond variable fonts (self-hosted, no external requests)
- `PHOTOGRAPHY.md` — complete shot list + ready-to-paste image-generation prompts for every image slot
- `.github/workflows/pages.yml` — GitHub Pages deployment

## Publishing to GitHub Pages

1. Merge this branch to `main` (or point the workflow at your preferred branch).
2. In the repo: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. Push — the site deploys to `https://<owner>.github.io/signium-golf/`.

## Design system

- **Palette:** ivory `#F6F1E7`, parchment `#EFE8D8`, racing green `#26382E`, navy `#25314B`,
  espresso `#463729`, heritage gold `#B8902E`, antique brass `#9C7B41`
- **Type:** Cormorant Garamond (display + body), monospaced small-caps for eyebrows/labels
- **Imagery:** deliberately design-system-first. Every image slot is an art-directed material
  treatment today; see `PHOTOGRAPHY.md` for the drop-in photography plan.

## Wiring the forms

The commission form and email-capture form currently confirm in-page without sending data.
To make them live, point them at a form endpoint (Formspree, Basin, or your CRM) inside the
two `submit` handlers at the bottom of `index.html`.
