# Mobile-First Defects in Local Home-Services Websites: A Rendered Audit of 21 Sites (October 2026)

**DOI: 10.5281/zenodo.23710476** — https://zenodo.org/records/23710476 (published v1.0.2, Zenodo)

Author: Derek Jamieson (Website Rescue)

## Title
Mobile-First Defects in Local Home-Services Websites: A Rendered Audit of 21 Small-Business Sites (October 2026)

## Authors
Derek Jamieson (Website Rescue) — identity/attribution per Derek's choice

## Abstract
We report the results of rendered mobile audits of 21 websites belonging to independently owned local home-services businesses (plumbing, electrical, HVAC, roofing, remodeling, general contracting) in Northeast Ohio and the Denver metropolitan area, conducted October 2026. Each site was loaded at mobile viewport (390x844, Chromium), captured full-page, and cross-checked at the source level (form elements, tel: hrefs, viewport meta) with an independent fetch. We found that 4 of 21 sites (19%) were unreachable or serving error content at their primary URL, 5 (24%) carried invalid TLS certificates, and at least 8 (38%) presented a contact-capture defect: a promised form that does not exist, no functioning tap-to-call path, or calls-to-action resolving to error pages. Two sites served template placeholder content. We provide a reproducible 25-point scoring rubric and publish our anonymized data. The prevalence of basic, mechanically fixable defects suggests that significant lead loss in this sector stems from unmonitored website breakage rather than from sophisticated conversion optimization failures.

## 1. Introduction
Local home-services businesses acquire customers through maps listings, referrals, and search, all of which terminate at the business website on a mobile device. While conversion-rate literature focuses on sophisticated optimization, field observation suggests many small-business sites fail at elementary level: the site loads, the phone number is tappable, the form exists. We present structured audit data quantifying the prevalence of such elementary failures.

## 2. Method
- Device emulation: Chromium mobile viewport 390x844, full-page captures.
- Source checks: count of <form> elements and input/iframes; tel: href inventory; viewport meta presence.
- Cross-validation: each defect observed in the browser was cross-checked via independent server-side fetch where possible.
- Dating: every finding recorded with inspection date; re-verification performed for entries entering publication.
- Scoring: 25-point rubric (business basics /10, visibility & mobile gaps /10, fit & feasibility /5); bands 20-25 top priority, 14-19 good, 8-13 watchlist, <8 skip.
- Ethics: business identities withheld; findings shared privately with each business; benchmark published anonymized (P01-P21).
- Limitations: small n; two regions; audits measure defect presence, not traffic or revenue causality; no latency measurements were performed.

## 3. Results (n = 21)
| Category | Count | Share |
|---|---|---|
| Site unreachable / error at primary URL | 4 | 19% |
| TLS certificate invalid or mismatched | 5 | 24% |
| Contact-capture defect (no form where promised / no tel: / non-functional CTA path) | 8+ | 38%+ |
| Calls-to-action resolving to 404 | 3 | 14% |
| Template placeholder / demo content live | 2 | 10% |
| Staleness signals (copyright 2011-2022) | 4 | 19% |
| Malformed tel: href | 1 | 5% |
Notes: categories overlap; sites may exhibit several defects. Full anonymized dataset in the companion benchmark sheet.

## 4. Case patterns (anonymized)
- P03 (HVAC): entire domain served 404 on root, www, and legacy contact path across three independent checks on two dates.
- P02 (plumbing): emergency-repairs page titled for a different trade and served from a wrong path; three conversion CTAs 404.
- P01 (plumbing): live WordPress installation still serving theme demo copy with placeholder personnel.
- P04 (electrical): contact page instructing users to use a form that does not exist (0 form elements), with no viewport meta and zero tap-to-call links.
- P21 (roofing, Denver): sole tap-to-call affordance embedded in a rotating hero slider; no persistent call affordance anywhere; no forms on the homepage.

## 5. Discussion
The dominant failure mode is unmonitored decay: sites that once worked now 404, carry expired certificates, or lose their forms after migrations. Because these defects are mechanically detectable, we propose rendered audits as a first-line diagnostic for any lead-generation intervention, prior to conversion optimization.

## 6. Data availability
Anonymized dataset: companion Google Sheet "Local Home-Services Website Defect Benchmark (2026 audit)" plus the scoring rubric in the public repository github.com/djbiz/awesome-contractor-speed-to-lead.

## 7. References
Minimal; methodological references to be added at upload (rendered-testing practice, TLS guidance, A2P 10DLC compliance overview).

---
CITATION: DOI 10.5281/zenodo.23710476. Published as repo release v1.0.2 via Zenodo-GitHub integration.
