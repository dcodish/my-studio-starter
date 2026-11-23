# Project rules for Claude

This folder belongs to a first-year student at a voluntary evening Claude Code workshop
(BGU, Industrial Engineering & Management). The student is a beginner: use plain words.

## Project documents
These files are the source of truth. Read them before changing anything, and keep them current.

| File | What it holds | Who owns it |
|---|---|---|
| `docs/REQUIREMENTS.md` | "In my words" (the student's raw idea), goal, users, numbered requirements (R1, R2...) each with an acceptance test, nice to have, out of scope | The student. Never change a requirement without asking; propose the change instead. |
| `docs/ARCHITECTURE.md` | Parts of the page, what data is saved and where, key decisions with reasons | Claude writes it; the student approves |
| `docs/PLAN.md` | Numbered build steps with checkboxes; each step names the requirement it serves | Claude writes it; the student approves |
| `CHANGELOG.md` | One line per change, newest first: date, what changed, which requirement | Claude |
| `README.md` | What the app is, the public link, how to open it | Claude |
| `index.html` | The app itself | Claude |

## Rules for the documents
- At the start of every chat, read `docs/REQUIREMENTS.md`, `docs/PLAN.md` and `docs/ARCHITECTURE.md` first.
- Never edit the "In my words" section of `docs/REQUIREMENTS.md`. The student writes it.
- No code before every must-have in `docs/REQUIREMENTS.md` has an acceptance test,
  and `docs/PLAN.md` exists and the student has approved it.
- Every plan step and every new feature names a requirement (R1...). If a new feature fits
  no requirement, ask whether to add one. A small cosmetic change (a color, a word) needs only
  a `CHANGELOG.md` line.
- After each change: tick the step in `docs/PLAN.md`, add a line to `CHANGELOG.md`, update
  `docs/ARCHITECTURE.md` if the structure or the saved data changed, then tell the student
  which acceptance tests to run. Do not mark tests as passed yourself: the student runs them.
- Found a bug? First add or fix its acceptance test in `docs/REQUIREMENTS.md`, then fix the code.
- When the app is published, put the public link in `README.md` and replace the starter note there.
- Keep every document to one screen, in plain words.

## Technical rules
- Build ONE self-contained file: `index.html`, with all CSS and JavaScript inside it.
  This keeps the page easy to publish as a Claude artifact or on Netlify Drop.
- No frameworks, no build step, no npm, no API keys, no paid services.
- No images or files from the internet. Draw graphics with SVG, `<canvas>`, CSS or emoji.
  If the user picks their own photo, read it in the browser (FileReader); never upload it anywhere.
- If the student connected a service (Calendar, Drive...), you may read it with the connector and
  copy what is needed (dates, a few photos) into `index.html`. The page itself never calls that
  service, and nothing private goes in without the student's OK.
- Must work by double-clicking `index.html`, and look good on a phone.
- Hebrew text is right-to-left (`dir="rtl"`); English is fine too.
- If the page saves data, use localStorage only, and describe it in `docs/ARCHITECTURE.md`.

## How to work with me
- Build the smallest working version first, then improve in small steps.
- After each change, tell me in 2-3 sentences what changed and how to check it.
- Never delete files without asking.
