# LinkedIn Idea Ledger

Standing record of every LinkedIn idea suggested by the idea generator. It's read before each run, so published, killed and in-progress ideas don't come back as new.

## Setup

Where everything lives, so the idea generator doesn't have to ask each run. Leave a line blank if it doesn't apply.

- **Voice guide:**
- **Offer and audience:**
- **Published and written posts:**
- **Stories (case studies, testimonials, project notes, scripts):**
- **Saved-for-later ideas:**
- **Published-posts record (export or list):**
- **Menus saved to:**
- **Dashboard:** (URL and UUID slug once set up; or "not now (date)" or "declined" if the offer was turned down)
- **Brand (for the dashboard):** (where it came from, main colours, font, logo file; or "neutral")

## How it works

**States:**
- `raised`: suggested in a menu, no decision yet. Logged automatically when a menu is saved. Fair game, but flagged "(raised before)" if it comes back.
- `exploring`: liked and being developed. Not suggested again as new; shown under "In progress" each run.
- `published`: actually went live on LinkedIn. Never suggested again.
- `killed`: rejected. Never suggested again, and neither is anything that would be rejected for the same reason.

**Columns:**
- **Source:** `new topic`, `new take`, `archive`, `trend` or `direct` (posted without coming from a menu), plus the specific source when known (e.g. `archive: event case study`).
- **Date:** the date of the last change.
- **Progress:** for `exploring` only: `no draft`, `drafted: <where>` or `stalled`. Blank for other states.
- **Reason / Note:** for `killed`, the actual reason it was rejected (this is what stops near-duplicates coming back). For other states, any useful context.

Decide in plain language during a session (`explore 3`, `publish 5`, `kill 7`), or on the dashboard, and the ledger is updated. Only mark `published` once a post has gone live, never for a draft.

Keep this file safe to share: no confidential client details or names of people being pitched. Describe private work by type ("a project for a car brand"), not by name.

## Ideas

| Slug | Idea | Source | State | Date | Progress | Reason / Note |
|------|------|--------|-------|------|----------|---------------|
