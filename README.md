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

### Rocket Reading Flashcards (Grades 4–5)

On the **Grade 4** and **Grade 5** curriculum pages there's a 🚀 **Rocket Reading
Flashcards** launcher. It's the full 52-week vocabulary spine (10 words/week, 520
words/grade) from the Rocket Reading PDFs, built as a spaced-repetition study app:

- **Spaced review (Leitner boxes).** Mark a word **“Got it”** and it's hidden for
  longer each time (1 → 3 → 7 → 16 → 45 days). **“Review soon”** brings it back this
  session. Pick a specific week to study, or **“All due now”** to review what's come back.
- **Word profiles without fabrication.** Each card pulls real pronunciation, part of
  speech, definition, example, synonyms & antonyms live from the free
  [Dictionary API](https://dictionaryapi.dev) (no key; cached after first load).
  Names/multi-word terms fall back to a "write your own / look it up" card.
- **Student sentence** field saved per word.
- **Notes & Links** panel (📝 in the flashcard bar): a notepad + saved URL bookmarks,
  with Export/Import backup.

The word list lives in the `VOCAB` object in `index.html`. Progress, notes, and links
are stored in `localStorage`.

> ⚠️ **Storage is per-device.** Flashcard progress, the student's sentences, notes, and
> links are saved in that one browser only — they are **not** uploaded, synced, or shared
> between devices/students. Use the **Export backup** button to save or move them. True
> multi-device/multi-student accounts would require a backend (e.g. Supabase).

### Verified free resource links (Grades 4–5)

The Grade 4 and Grade 5 curriculum pages already list every assigned reading and
unit text as a clickable item. Clicking one opens its resource pop-up — and for
grades 4–5 those pop-ups now link straight to a **verified, lawful, free** copy on
the source site (Core Knowledge unit PDFs, Project Gutenberg, Folger, Poets.org)
instead of the generic Core Knowledge homepage. Commercial/unverified items
(e.g. Wordly Wise, Phantom Tollbooth) keep the default "find a copy" behavior —
they are intentionally **not** linked until a lawful free copy is confirmed.

The mapping lives in the `VERIFIED_LINKS` array in `index.html` (keyed by a keyword
in the item title) and is applied by `verifiedLink()` inside `openResourceModal()`.
Sourced from a Grade 4–5 link audit.

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
