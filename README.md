# Ombri — Design Explorations

Static showcase site for **Ombri**, an iOS finance app with a time-of-day shifting home screen and weather-aware ambient states.

Two explorations, stitched into one scrollable page:

1. **Time of Day** — four variants (morning · afternoon · evening · night)
2. **Weather** — ambient weather-state variants

## Live site

Served via GitHub Pages. See the repo's Pages settings for the current URL.

## Run locally

No build step. Open `index.html`, or serve the folder:

```sh
python3 -m http.server 8000
# → http://localhost:8000
```

## Structure

```
.
├── index.html           # scrollable wrapper — loads both mockups as auto-sized iframes
├── home-redesign.html   # 2×2 time-of-day grid (self-contained React via Babel standalone)
└── home-weather.html    # weather-state grid with CSS animations
```

The mockups are self-contained — each is a complete HTML doc with its own styles and scripts. The wrapper `index.html` embeds them as same-origin iframes and auto-sizes them to content height using `ResizeObserver` + `MutationObserver`.

---

*The broader design + build plan for the site lives in the app repo as `WEBSITE_CONSTITUTION.md`.*
