# figma-recreation

Static interactive prototype recreating a Figma design — Home hub, Files, Resources, Calendar, Whiteboard, Editor, Recontextualiser, and Appearance Settings. Pure HTML/CSS/JS, no build step, no dependencies.

Live site (after enabling Pages): `https://lucky10-au.github.io/figma-recreation/`

## Pages

| File | Description |
|------|-------------|
| `home.html` | Hub — New File/Resource modal, recent docs, books grid, week strip |
| `files.html` | Search + expandable file rows with inline-editable notes |
| `resources.html` | Textbook cards + study links with expandable notes |
| `calendar.html` | Day/Week/Month/Year views, drag/resize events, create modal, filters, mini-calendar |
| `index.html` | Whiteboard canvas — draw, shapes, sticky notes, text, clipboard, undo/redo, pan |
| `editor.html` | Formatting bar — contenteditable title/body, fonts, size, B/I/U, bullets, align, indent |
| `recontextualiser.html` | Rewrite demo — mock mode + optional live API POST |
| `settings-appearance.html` | Every appearance control — accent, dark mode, text size, summaries, sync, plan |

See `WALKTHROUGH.md` for the full click-through demo script.

## Run locally

No build needed. Either:

```bash
# Option 1: just open
open home.html

# Option 2: serve (recommended, avoids any file:// quirks)
python3 -m http.server 8000
# then visit http://localhost:8000/home.html
```

Entry points: `home.html` (hub) or `index.html` (whiteboard).

## Deploy to GitHub Pages

1. Push to `main` on GitHub (public repo).
2. Repo → **Settings → Pages** → Source: **Deploy from a branch**, Branch: **main / (root)**, Save.
3. Site goes live at `https://lucky10-au.github.io/figma-recreation/` in ~1 min.

`.nojekyll` is included so Pages serves files as-is.

## Notes

- All state is in-memory — refresh resets pages.
- Recontextualiser demo mode needs no key. Live mode posts endpoint + key + model from the UI; nothing is hardcoded.
