# Cowork conversation log

Earlier Cowork chats (Aug–Nov 2026) cannot be exported as transcripts. Their decisions are captured in `notes/claude-memory-export.md` and `notes/project-context.md`. This file logs the Cowork session of 19 Nov 2026 and should be extended with a dated entry after each future session.

---

## 2026-11-19 — Repo set-up and Cowork ↔ Claude Code bridge

**Goal:** put all project files on GitHub (`nbqpyatra-web/FarmerSamriddhi-Makhana`) and connect Cowork (main workspace) with Claude Code (portal only).

1. **Push attempts.** Cowork in the browser could not push to GitHub: the session had no access to the repo (403 from the git proxy), even after the Claude GitHub App was given access. Repo access is fixed when a session starts. Decision: deliver the repo as a zip for manual upload; Claude Code at claude.ai/code (repo selected) is where pushes happen.
2. **Repo built** with README, `documents/`, `notes/`, `CLAUDE.md` (standing rules Claude Code reads automatically), `WORKFLOW.md`, `MISSING_FILES.md`.
3. **Workflow agreed:** Cowork = drafting, documents, tracker updates (`documents/`, `notes/`, `tracker/`). Claude Code = portal only (`portal/`, `.github/`). GitHub = single source of truth and portal hosting (GitHub Pages). The tracker CSV is the hand-off between the two. Saved to the Cowork project as `claude/Cowork_Code_GitHub_Workflow.md`.
4. **Automatic sync:** not possible from browser Cowork. Option offered: Claude desktop app + a local clone of the repo (GitHub Desktop) linked to Cowork, plus a project instruction to commit and push at the end of every task.
5. **Files added:** DoH Letters 3002 (29 Jul proceedings), 3064 (05 Aug proposal), 3703 (08 Oct proceedings); update note (08 Sep).
6. **Further uploads read and saved to memory:** SG deck (30 Jun), RoD (29 Jul), Project Charter (8 Sep), 1QCI deck (Sep), Draft MoU VF (16 Oct), QCI Data Points Doc (16 Oct).
   - Correction: **Dr. Pradeep Hazari is PMU Head, Directorate of Horticulture, Bihar** (not QCI).
   - MoU VF broadens scope to Bihar's horticulture value chains with makhana first; financial proposal after MoU execution (Art. 3).
   - Data Points Doc has no NDIE (WS-12) section — to confirm.
7. **Missing-files list** trimmed at Rachit's request to: originals of the six uploaded documents + the approved activity tracker Excel (needed for the portal).
8. **Initial Gantt chart (Dec 2025)** added as reference only — shows where the project started; its dates are not aligned and are not used in the tracker.
9. **Project journey** (`tracker/journey.csv`): Origins stages (no dates), dated milestones backed by documents, and next steps — shown at the top of the portal.
10. **Portal plan:** paste `portal/FIRST_PROMPT_FOR_CLAUDE_CODE.md` into Claude Code with the repo selected; enable GitHub Pages (Settings → Pages → Source: GitHub Actions). Free plan requires a public repo for Pages — consider privacy of DoH letters and MoU.

**Open items**
- Upload repo contents and original documents to GitHub.
- Send the approved activity tracker Excel → convert to `tracker/activities.csv`.
- Confirm date the MoU VF and Data Points Doc were sent to DoH.
- Confirm whether an NDIE (WS-12) data-points section is needed.
- Update field visit (18–20 Nov) outcome when done.
