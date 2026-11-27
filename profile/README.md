# profile/

Personal career facts live here, **outside the tracked workflow files**, so a public fork does not publish them.

| File | Tracked? | Purpose |
|------|----------|---------|
| `profile.example.md` | yes | Blank North American template with `[FILL IN]` markers |
| `profile.local.md` | **no (gitignored)** | Your real profile. Copy the example and fill it in |

## How it is used

`/scrape`, `/apply` and the job-fit evaluation read `profile/profile.local.md` first (if it exists) and treat it as the
source of truth for identity, work authorization, location tiers, salary floor and role priorities. Anything marked
`[FILL IN]` is unknown: the assistant must ask, never guess.

## Rules

1. Never invent employers, dates, degrees, certifications, clearances or licences. Leave `[FILL IN]`.
2. Do not put phone, email or street address in any tracked file. The CV `.tex` files for real applications
   (`cv/main_<company>.tex`) are already gitignored; contact details belong there or in `profile.local.md`.
3. If you run `/setup`, it writes into `CLAUDE.md` and `.claude/skills/job-application-assistant/*.md`, which ARE tracked.
   On a public fork, either keep those placeholders and answer from `profile.local.md`, or make the repo private first.
