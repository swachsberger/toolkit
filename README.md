# Sam / Toolkit

A personal hub page linking to small self-contained web tools, deployed with GitHub Pages.

**Live:** https://swachsberger.github.io/toolkit/

## Structure

```
.
├── index.html          # the hub page (edit the `apps` array to add a tile)
├── dice-roller/        # two-dice roller — animation + Web Audio clicks
│   └── index.html
├── countdown/          # Countdown numbers game — solver, validator, scoring
│   └── index.html
└── README.md
```

Each tool is a single static `index.html` with no build step and no external
runtime dependencies — everything runs client-side, so it works directly on
GitHub Pages.

The **Wall Planner** tile links out to its own repo/site
(https://swachsberger.github.io/wall-planner/), which is maintained separately.

## Adding a new tool

1. Create a folder with an `index.html` (e.g. `my-tool/index.html`).
2. Add an entry to the `apps` array in the root `index.html`:
   ```js
   { name: "My Tool", code: "HTML", desc: "One line.", url: "my-tool/", online: true }
   ```
   Add `external: true` for a tool hosted on another site (opens in a new tab).
3. Commit and push to `main`; GitHub Pages redeploys automatically.

## Local preview

```bash
python3 -m http.server 8010 --directory .
# then open http://localhost:8010/
```
