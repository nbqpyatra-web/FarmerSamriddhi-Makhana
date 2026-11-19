# Tracker data — the single source for the portal

`activities.csv` holds every activity. The portal (built in Claude Code, in `portal/`) reads this file only — update the CSV and the Gantt/tracker updates. Open and edit it in Excel; save as CSV (UTF-8).

## Columns
| Column | Format / allowed values | Example |
|---|---|---|
| activity_id | Unique, never reused: `A-001`, `A-002`… | A-001 |
| workstream_id | `WS-01` … `WS-14` | WS-08 |
| intervention | Intervention name as in the SG pack mapping | [as per mapping sheet] |
| activity | What is being done | [activity] |
| lead_board | One of: PPID, NBQP, PADD, SPD, TCB, NDIE | PPID |
| supporting_boards | Semicolon-separated, same list | NBQP;PADD |
| owner | Person responsible | [name] |
| start_date / end_date | `YYYY-MM-DD` | 2026-12-01 |
| status | Not Started, In Progress, Completed, On Hold, Delayed | In Progress |
| percent_complete | 0–100 | 40 |
| depends_on | activity_ids, semicolon-separated | A-001;A-003 |
| milestone | `Yes` for a single-date milestone (start = end), else blank | Yes |
| remarks | Free text; flag open questions here | [awaiting DoH data] |
| evidence_link | Path in this repo (e.g. `documents/...pdf`) or URL | documents/DoH_Bihar_Letter_3703_2026-10-08_Meeting_Proceedings.pdf |
| last_updated | `YYYY-MM-DD` | 2026-11-19 |

Rows are filled from the approved activity tracker — do not invent activities or dates; use `[placeholder]` in remarks where unconfirmed.

## journey.csv — Project journey (shown above the Gantt)
Columns: `order, phase (Origins / Engagement / Next), title, date (YYYY-MM-DD or blank), status (Completed / In Progress / Scheduled / Upcoming), source`.
Origins rows come from the initial Gantt chart and deliberately have **no dates** (its dates are not aligned with the current plan). Dated rows must be backed by a document named in `source`.
