# Workflow — Cowork ↔ GitHub ↔ Claude Code

```
 Claude Cowork  ──(files)──▶  GitHub repo  ◀──(code)──  Claude Code
 drafting, MoU, notes,        single source              builds & updates
 tracker updates              of truth                   the portal only
```

## Who does what
| Tool | Used for | Writes to |
|---|---|---|
| **Cowork** (main workspace) | MoU, letters, concept notes, financial proposal, RoD, research, and **updating tracker rows** | `documents/`, `notes/`, `tracker/activities.csv` |
| **Claude Code** (portal only) | Building and changing the live tracker / Gantt portal | `portal/` only |
| **GitHub** | Stores everything; hosts the portal (GitHub Pages) | — |

Rule: Claude Code never edits `documents/` or `tracker/activities.csv` content; Cowork never edits `portal/`. The CSV is the hand-off between the two.

## Day-to-day loop
1. Work in Cowork. When an activity moves (status, dates, % done), ask Cowork to update `tracker/activities.csv`.
2. Get the changed files into GitHub (see "Bridge" below).
3. The portal reads the new CSV automatically — no Claude Code session needed for routine updates.
4. Open Claude Code only to change how the portal looks or works.

## Bridge — getting Cowork files into GitHub
- **Option A (recommended): link your computer.** Clone the repo to your computer (GitHub Desktop is easiest), open Cowork in the Claude desktop app, and connect that folder. Cowork then saves and commits/pushes directly using your own GitHub login.
- **Option B: manual upload.** Cowork gives a file/zip → GitHub → Add file → Upload files → Commit.

## Visibility
GitHub Pages on a **public** repo makes the portal public to anyone with the link. Keep the repo **private** (portal on Pages from a private repo needs a paid GitHub plan), or keep DoH letters out of the repo and publish only tracker data.
