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

### Reading Library (Grades 4–5)

**Resources → Reading Library · 4–5** lists the assigned readings and unit texts
with links to **verified, lawful, free** copies on trusted sites (Core Knowledge,
Project Gutenberg, Folger, Poets.org). These links open on the source site — Strive
does not re-host them. Items tagged **"Add later"** are commercial or unverified and
are intentionally **not** linked until a lawful free copy is confirmed. The data
lives in the `LIBRARY` object in `index.html`. Sourced from a Grade 4–5 link audit.

> Links to third-party sites can rot. Re-check them periodically; a dead link just
> 404s on the source site, it won't break the dashboard.

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
