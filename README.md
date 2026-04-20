# ArtFinance — Design Explorations

Static showcase site for the [ArtFinance](../artfinance) iOS app's home screen design work.

Two explorations, stitched into one scrollable page:

1. **Home Redesign v3** — four time-of-day variants (morning · afternoon · evening · night)
2. **Home Weather** — weather-aware ambient states

## Live site

Served via GitHub Pages. See the repo's Pages settings for the URL.

## Run locally

No build step. Just open `index.html`, or serve the folder:

```sh
python3 -m http.server 8000
# → http://localhost:8000
```

## Structure

```
.
├── index.html           # scrollable wrapper — loads both mockups as auto-sized iframes
├── home-redesign.html   # 4-frame time-of-day grid (self-contained React via Babel standalone)
└── home-weather.html    # weather-state grid with CSS animations
```

The mockups are self-contained — each is a complete HTML doc with its own styles and scripts. The wrapper `index.html` embeds them as same-origin iframes and auto-sizes them to content height.

> **Note:** "ArtFinance" is a working placeholder name. See `WEBSITE_CONSTITUTION.md` in the app repo for naming status and the broader showcase plan.
