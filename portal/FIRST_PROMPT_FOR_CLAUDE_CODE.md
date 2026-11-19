# First prompt to paste into Claude Code

(Start a session at claude.ai/code with `nbqpyatra-web/FarmerSamriddhi-Makhana` selected.)

---

Read CLAUDE.md, WORKFLOW.md and tracker/README.md first.

Build a static web portal in the `portal/` folder for the Farmer Samriddhi – Makhana programme, deployable on GitHub Pages. Requirements:

1. Data: read `tracker/activities.csv` and `tracker/journey.csv` at load time (no hard-coded data). Columns are defined in tracker/README.md.
2. Views:
   - **Project journey** (top of page) — read `tracker/journey.csv`; show a horizontal timeline grouped by phase (Origins, Engagement, Next). Rows without a date show as stages with a status badge only, never with an invented date. Each item links to its `source` when it is a repo path.
   - **Gantt chart** — rows grouped by lead board (PPID, NBQP, PADD, SPD, TCB, NDIE) and then workstream; bars coloured by status; milestones as diamonds; a "today" line.
   - **Tracker table** — sortable, with filters for board, workstream, status and owner.
   - **Summary cards** — total activities, completed, in progress, delayed, overall % complete.
3. Click any activity to open a detail panel showing all columns, including remarks and a clickable evidence_link.
4. Plain HTML/CSS/JS with no build step; at most one charting library loaded from a CDN.
5. Header: "Farmer Samriddhi – Makhana | QCI–DoH Bihar Programme Tracker", with a "Last updated" date taken from the latest last_updated value.
6. Add a GitHub Actions workflow to publish `portal/` (plus the `tracker/` CSV files) to GitHub Pages on every push to main.
7. Only create or modify files in `portal/` and `.github/`. Do not edit `documents/`, `notes/` or the contents of `tracker/activities.csv`.

Commit to main and tell me the Pages URL and any GitHub settings I need to switch on.
