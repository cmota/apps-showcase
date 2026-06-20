# Apps — showcase site

A small landing page that showcases the apps, with a card for each one. Each card
links through to that app's own marketing site, which lives in its own subfolder.

Plain HTML/CSS, no build step. Designed for static hosting (e.g. GitHub Pages).

## Structure

```
.
├── index.html          # the showcase hub (cards for each app)
├── style.css           # hub styles (dark "studio" theme)
├── assets/             # hub-only assets (app icons, favicon, OG image)
├── robots.txt          # ← update the host if you deploy to a custom domain
├── sitemap.xml         # ← update <loc> entries if you deploy to a custom domain
│
├── matchday-26/        # Matchday 26 marketing site (self-contained)
│   ├── index.html
│   ├── privacy.html
│   ├── style.css
│   └── assets/
│
└── poolcast/           # PoolCast marketing site (self-contained, inline assets)
    ├── index.html
    └── privacy.html
```

- The hub card for **Matchday 26** links to `matchday-26/`.
- The hub card for **PoolCast** links to `poolcast/`.
- A third card is a placeholder for apps coming soon.

Each app site is fully self-contained and uses only relative links, so it works
both at the root of its own domain and from these subfolders.

## Sources

- `matchday-26/` was imported from the standalone Matchday marketing site (`cmota/apps-showcase`).
- `poolcast/` was imported from the `website/` folder of the PoolCast app project.

## Deploying

1. Push to a repo and enable GitHub Pages (serve from the branch root).
2. The default base URL assumed in `robots.txt` and `sitemap.xml` is
   `https://cmota.github.io/apps-website/`. If you use a different repo name or a
   custom domain, update those two files accordingly.

> Matchday 26 is an independent, unofficial fan app and is not affiliated with FIFA
> or any official organising body. All trademarks belong to their respective owners.
