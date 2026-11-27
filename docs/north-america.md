# North America edition

Defaults for searching and applying in **Canada (British Columbia first) and the United States**.
Verified against public pages in November 2026. Boards and rules change, so re-check before relying on one.

## What the upstream project assumed, and what changed

| Upstream assumption | Where | Change |
|---------------------|-------|--------|
| Danish job market and portals (Jobindex, Jobnet, Jobdanmark, Akademikernes Jobbank) | `README.md`, `job-scraper/SKILL.md`, `search-queries.md`, `setup.md`, `SETUP.md` | North American boards are the default. Danish CLIs under `.agents/skills/` stay, marked optional. Note: `jobbank-search` is `jobbank.dk` (Denmark), not Job Bank Canada (`jobbank.gc.ca`). |
| A4 paper | `cv/main_example.tex`, `05-cv-templates.md` | `letterpaper` by default. `a4paper` only on request. The cover-letter class already uses the article default (US Letter in most TeX installs). |
| Commute-distance location model; relocation is a deal-breaker | `job-scraper`, `04-job-evaluation.md` | Location tiers in the profile, plus a work-authorization gate and a clearance/licence check. |
| Salary index data in DKK (`salary_lookup.py`, `salary_data.json`) | `04-job-evaluation.md`, `tools/` | Marked as not a North American wage source. Use Job Bank Canada wage reports (CAD) and BLS OEWS (USD) plus the posting's range. Code is untouched. |
| Cover-letter language: Danish or English; closings and date format | `apply.md`, `06-cover-letter-templates.md` | English default, French for Quebec/federal bilingual roles. `Month D, YYYY` dates. |
| Review sites such as Jobindex | `04-job-evaluation.md` | Glassdoor, Indeed reviews. |
| Danish-style CV extras (photo, birth date) | Not present in the templates. | Added an explicit "do not include" rule: no photo, date of birth, marital status, nationality line. |
| Personal data goes into tracked files via `/setup` | `CLAUDE.md`, `01-candidate-profile.md`, ... | For a public fork, use gitignored `profile/profile.local.md`. `/setup` now warns when the repo is public. |
| EUR/GBP, StepStone, Europass, visa-sponsorship wording | Not present in this repo (no UK/EU-specific text found). | Nothing to remove. |

## Résumé format (private sector)
- No photo, date of birth, age, marital status, nationality line, or full street address.
- US Letter. One to two pages. Month/year dates. Results-first bullets.
- Work authorization: add a short line only if the posting asks or if it removes doubt. Use the exact facts in the profile.
- Only list certifications and licences actually held. P.Eng, BCLS, CLS and PLS are licences, not skills.

## Public-sector and special cases
- **BC Public Service:** apply through the Career Centre. You must be eligible to work in Canada. Permanent offers require Canadian citizenship or PR unless the posting says otherwise. The résumé should show start and end month/year for each role and mirror the listed qualifications. Source: gov.bc.ca "Eligibility to apply for a position".
- **Government of Canada:** many postings give preference to Canadian citizens. Check "who can apply".
- **USAJOBS:** most roles need US citizenship. Résumés are longer and ask for hours per week, supervisor and salary. Veterans' preference: sign in, add military service under Profile > Experience, select preference when applying. 5-point preference generally needs the DD-214 (honourable or general discharge). 10-point also needs an SF-15 or a VA letter. **Preference is unconfirmed for this user. Do not claim it until the DD-214 is checked.** Source: USAJOBS help centre.
- **Security clearance:** none assumed. Filter out roles that require an active clearance.

## Boards

| Board | Region | Use | Status |
|-------|--------|-----|--------|
| Indeed Canada / Indeed US | CA, US | Broad | Standard |
| LinkedIn Jobs | CA, US | Broad | Standard |
| Job Bank Canada (`jobbank.gc.ca`) | CA | Land-survey and GIS technician postings with wage data | Verified |
| BC Public Service | BC | Provincial government roles | Verified |
| USAJOBS | US | Federal roles (NIST, USGS, NOAA, etc.) | Standard |
| GoGeomatics Canada (`gogeomatics.ca/jobs`) | CA | Geomatics, GIS, survey, remote sensing | Verified |
| ABCLS employment page (`abcls.ca/page/careers`) | BC | Survey firms | Verified (dynamic page) |
| ASPRS geospatial jobs | US | Photogrammetry, lidar, GIS | Verified (low volume) |
| NCSL International metrology jobs (`ncsli-jobs.careerwebsite.com`) | US mainly | Calibration, metrology, CMM, field service | Verified |
| ACLS (`acls-aatc.ca`) | CA | No general job board | Verified, not useful for job search |

## Pay examples seen in public postings (Sep to Nov 2026, for orientation only)
- Survey CAD technician or technologist, Vancouver: C$30 to 40 per hour (360 Land Surveying careers page).
- Survey assistant, Vancouver: C$24 to 28 per hour (same page).
- Mapping technician, City of Delta: C$39.85 to 46.90 per hour (GoGeomatics posting, closed Oct 2026).
- Land survey technician, Burnaby: about C$40 per hour (Job Bank).
- Metrology and quality inspector roles in Arizona: US$42,000 to 115,000 per year depending on level (NCSLI board).

## Target role families (ranked by fit for the profile in this fork)
See `.claude/skills/job-scraper/search-queries.md`. The ranking is a starting point. Reorder in `profile/profile.local.md`.
