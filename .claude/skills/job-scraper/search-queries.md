# Search Queries for Job Scraper (North America edition)

Region defaults: **Canada (British Columbia first) and the United States.** Pay is shown in **CAD** for Canadian postings and **USD** for US postings.
Personal facts (work authorization, location tiers, salary floor) come from `profile/profile.local.md` when it exists.
Boards marked "verified" had a working public page when this file was written (Nov 2026). Re-check before relying on one.

## Search Sites

### General, Canada
- **ca.indeed.com**: broadest coverage of BC employers. Use `site:ca.indeed.com` queries, or the posting URL.
- **jobbank.gc.ca** (Job Bank Canada, verified): federal job board with BC land-survey and GIS technician postings and wage data.
  Not the same as the Danish `jobbank.dk` skill under `.agents/`.
- **linkedin.com/jobs**: filter Canada / British Columbia, or United States.
- **BC Public Service**: postings via `www2.gov.bc.ca/gov/content/careers-myhr/job-seekers/current-job-postings`
  (applications run through `bcpublicservice.hua.hrsmart.com`, verified). Eligible to work in Canada required to apply;
  permanent offers need citizenship or PR unless the posting says otherwise.
- **Municipal and regional employers** (City of Vancouver, Surrey, Burnaby, Delta, Metro Vancouver, TransLink): often post on their own career pages.
- **Government of Canada** (`jobs-emplois.gc.ca`): many roles are open to Canadian citizens first. Check "who can apply" on each posting.

### General, United States
- **indeed.com**, **linkedin.com/jobs**.
- **usajobs.gov** (federal jobs; US citizens only for most roles). Claim veterans' preference only if confirmed
  (see `profile/profile.local.md`). A USAJOBS résumé is longer than a private-sector résumé. See `docs/north-america.md`.

### Niche: geomatics, survey, GIS
- **gogeomatics.ca/jobs** (GoGeomatics Canada, free, verified): Canadian geomatics, GIS, survey and remote-sensing postings.
- **abcls.ca/page/careers** (Association of BC Land Surveyors, verified): employment opportunities page; its listings load dynamically, so may need a browser.
- **asprs.org** geospatial job opportunities page (verified): mostly US, small volume, academic-heavy.
- **Company career pages** (survey firms with BC offices, verified Nov 2026): McElhanney (`mcelhanney.com`), 360 Land Surveying (`360surveys.ca/careers`), Polaris Land Surveying (`plsi.ca/opportunities`).
- The Association of Canada Lands Surveyors (`acls-aatc.ca`) does not run a general job board. It only advertises its own staff roles.
- Other boards to try: GISjobs.com and the URISA job board (US GIS). Treat as unverified until a result is seen.

### Niche: metrology, calibration, quality
- **ncsli-jobs.careerwebsite.com** (NCSL International metrology jobs, verified): mostly US, includes calibration technician, CMM, metrology engineer, field service roles.
- Calibration and test-equipment company career pages (verify each for BC / Canada): Transcat, Trescal, Tektronix, Fluke, Keysight. These are example employers to search, not confirmed openings.
- ASQ job board (quality) as a secondary source. Unverified.

## Query Categories (ranked by fit)

Run priority 1 to 3 by default. Run all with "broad". Combine with a location term: `Vancouver`, `Burnaby`, `Surrey`, `Richmond`, `Lower Mainland`, `British Columbia`, `Canada`, or `remote`.
Each query is a pattern: swap in the site you are searching.

### Priority 1: Calibration / metrology technician
```
site:ca.indeed.com "calibration technician" Vancouver OR "British Columbia"
site:ca.indeed.com "metrology technician" OR "calibration lab" British Columbia
site:linkedin.com/jobs "calibration technician" Canada
site:ncsli-jobs.careerwebsite.com calibration technician
site:linkedin.com/jobs "metrology" OR "measurement" technician "United States" remote
```
Keywords: calibration, traceability, measurement uncertainty, ISO/IEC 17025, metrology, test and measurement, multimeter, torque, pressure, dimensional, CMM, gauge, GD&T, SPC.

### Priority 2: Survey / geomatics technician (field and office)
```
site:jobbank.gc.ca "land survey technician" OR "survey technologist" British Columbia
site:gogeomatics.ca/job survey OR geomatics British Columbia
site:ca.indeed.com "survey assistant" OR "survey crew" OR "party chief" British Columbia
site:ca.indeed.com "geomatics technician" Vancouver
site:linkedin.com/jobs "survey technician" OR "geomatics technician" Canada
```
Keywords: land survey, total station, GNSS, RTK, legal survey, topographic survey, construction layout, LST, survey assistant, party chief, field-to-finish, TDS, Trimble, Leica.

### Priority 3: GIS / CAD technician
```
site:ca.indeed.com "survey CAD" OR "CAD technician" OR "survey technologist" Vancouver
site:gogeomatics.ca/job "mapping technician" OR "GIS technician" British Columbia
site:linkedin.com/jobs "Civil 3D" technician OR designer British Columbia
site:jobbank.gc.ca GIS technician British Columbia
```
Keywords: Civil 3D, AutoCAD, survey CAD, mapping technician, GIS technician, ArcGIS Pro, QGIS, LandXML, point cloud, ReCap, drone / UAV, LiDAR processing, photogrammetry (Metashape, Pix4D).

### Priority 4: Field service / instrument technician
```
site:ca.indeed.com "field service technician" instrumentation OR "test equipment" British Columbia
site:linkedin.com/jobs "field service engineer" OR "field service technician" "British Columbia" OR Vancouver
site:linkedin.com/jobs "instrument technician" OR "electronics technician" Vancouver
```
Keywords: field service, installation, preventive maintenance, oscilloscope, soldering, troubleshooting, repair, RMA, survey instruments, sonar / marine electronics, sensors, calibration of customer equipment.

### Priority 5: Network / systems / devops (bridge income, higher pay)
```
site:ca.indeed.com "network administrator" OR "systems administrator" Vancouver Juniper
site:linkedin.com/jobs "Juniper" network engineer OR administrator "British Columbia" OR Canada remote
site:linkedin.com/jobs devops OR "site reliability" "Canada" remote contract
site:ca.indeed.com "IT support" OR "systems analyst" survey OR geomatics OR engineering firm Vancouver
```
Keywords: Juniper, Junos, Linux, Ubuntu, CI/CD, GitHub Actions, Docker, PowerShell, Hyper-V, Python, infrastructure, startup.
Treat contract and short-term roles as in scope for this family.

### Priority 6: QA / measurement / inspection
```
site:ca.indeed.com "quality technician" OR "quality inspector" OR "QA technician" Vancouver OR "Lower Mainland"
site:linkedin.com/jobs "dimensional inspector" OR "metrology inspector" OR "CMM" Canada OR "United States"
```
Keywords: inspection, CMM, GD&T, SPC, FAIR, PPAP, non-conformance, quality system, ISO 9001.

### Wildcard: survey-software support and automation
```
site:linkedin.com/jobs "Civil 3D" OR "MicroSurvey" OR "Carlson" implementation OR "technical support" OR "application specialist" Canada
site:ca.indeed.com "survey software" OR "CAD customization" OR "CAD automation" British Columbia
```
This is where survey knowledge, scripting and tool-building (Python, Rust, C#) meet. Pay is often above plain CAD technician pay.

## Location Filter
Use the tiers in `profile/profile.local.md`. Defaults when it is absent:
- **Ideal:** Metro Vancouver and the Lower Mainland (on-site or hybrid).
- **Acceptable:** elsewhere in British Columbia; Canada-wide remote.
- **Check first:** US remote roles. Many US employers cannot hire a BC resident. Look for "open to Canada" language.
- **Relocation (only if the user says so):** other cities listed in the profile.

## Work Authorization Filter
- Flag postings that need **Canadian citizenship or PR** (federal public service, many BC Public Service permanent roles) unless the profile says he qualifies.
- Flag postings that need a **security clearance** (US: Secret/TS or public trust; Canada: Reliability, Secret). Profile says none active.
- Flag **US-only federal** roles that need US citizenship (fine for a US citizen) and note the location requirement.

## Exclusion Rules (skip, but still log in `seen_jobs.json` as skipped)
- Requires a **professional licence he does not hold**: P.Eng, BCLS, CLS, PLS, "commissioned land surveyor", "Registered Professional ...". LST / survey assistant roles are fine.
- Titles with **Engineer** where the posting requires an engineering degree and registration. Measurement, calibration and field service "engineer" roles that accept technologist experience are fine.
- **Senior, Director, Principal** (8+ years of leadership) with no path from his profile.
- **Commission-only, sales / BDR, MLM, "unpaid", staffing-agency spam**, and postings without a named employer.
- On-site outside the allowed location tiers (no remote option).
- Clearly **posted before the 14-day window**, or marked closed.
- Pay clearly under the floor in `profile/profile.local.md` (if set).

## Date Filter
Only include jobs posted in the last 14 days, or whose deadline has not passed. If the date cannot be found, include it and flag "date unknown".
Many municipal and public-service postings are open only 1 to 3 weeks. Show the closing date.

## Adapting Queries
If the user gives a focus area (for example `/scrape calibration`), run that category plus 2 or 3 custom queries.
For `broad`, run every category above.
