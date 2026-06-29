# Strive Academy — Curriculum Library

A public, password-gated dashboard where families and educators can explore the
Strive Academy program and **download the full curriculum**.

🔗 **Live site:** https://mindstorm-code.github.io/strive-academy-curriculum/
🔑 **Access code:** `ELJEFFE`

## What's here

- `index.html` — the Mission Control dashboard (single self-contained page).
- `curriculum/` — downloadable PDFs:
  - Comprehensive Overview, Adaptive Learning Protocol, Strive OS
  - 52-Week Adventure Curriculum, Vocab Reader, Character Psychology Bible
  - K–6 Grade Adaptive Blueprints
  - Mission Report templates (per-lesson, weekly, Week 1 assignments)

Open the dashboard and visit **Resources → Curriculum Downloads** to grab any file.

## ⚠️ About the access code

The `ELJEFFE` gate is a **soft, client-side deterrent** — it hides the dashboard
UI from casual visitors. It is **not** real security:

- The code is readable in the page source.
- Files in `curriculum/` are public and downloadable by direct URL **without** the code.

Do not put anything confidential in this repo. For genuine access control, host
behind a login (e.g. Netlify password protection or a Vercel-protected deploy).

## Updating

Edit `index.html` (the download list lives in the `DOWNLOADS` array), drop new
PDFs into `curriculum/`, then commit and push to `main`. GitHub Pages redeploys
automatically.
