# awesome-contractor-speed-to-lead

Open-source, copy-paste fixes for the mobile conversion problems we find most often when auditing contractor websites (HVAC, plumbing, electrical, roofing, remodeling).

Maintained by [Website Rescue](https://websiterescue.cc) — we run rendered mobile audits of local home-services sites and publish what we find (anonymized) in our [defect benchmark](https://docs.google.com/spreadsheets/d/1BOAvWcA65d-HiTNXOQZ1L7TjskYiHzFSrUvt2vwO5zI/edit).

## Why this repo exists

From a 21-site rendered audit (October 2026, anonymized in the benchmark sheet):

- 4 of 21 sites were unreachable or serving error pages at their main URL
- 5 had broken TLS certificates (self-signed or hostname-mismatched)
- 5 had contact-capture defects (promised forms that do not exist, zero tap-to-call links)
- 3 had CTAs pointing at 404 pages
- 2 were still serving template placeholder / demo content
- Several carried copyright years from 2011-2022 with no updates since

Every finding above came from dated, rendered mobile inspections (390x844 Chrome) plus source-level checks.

## Contents

- [`snippets/sticky-tap-to-call.html`](snippets/sticky-tap-to-call.html) — accessible sticky call button that stays out of the way
- [`snippets/missed-call-text-back.md`](snippets/missed-call-text-back.md) — the missed-call text-back playbook (carriers + compliance notes)
- [`snippets/mobile-viewport-fix.md`](snippets/mobile-viewport-fix.md) — the one-line viewport fix and how to verify it
- [`snippets/form-sanity-check.md`](snippets/form-sanity-check.md) — how to verify your contact form actually exists and sends
- [`checklist/25-point-audit.md`](checklist/25-point-audit.md) — the 25-point audit rubric we score with

## Rules for this repo

1. Every snippet is plain HTML/CSS/JS — no frameworks, no tracking, no analytics by default.
2. Claims in this README cite our own dated audits only. We do not publish stats we did not measure.
3. PRs welcome — especially carrier-specific missed-call compliance notes per region.

## About

Website Rescue fixes contractor websites in a 10-business-day sprint. Start with a $297 Website Diagnostic (credited 100% toward the fix). websiterescue.cc · 311 E State St, Olean, NY 14760

## Presentation decks (HTML, self-hosted on Pages)

Five substantiated audit briefings — every number traces to the benchmark sheet, no third-party or invented stats:

1. [What Breaks on Contractor Websites — Rendered Audit 2026](decks/audit-briefing-1.html)
2. [Fix Mobile Tap-to-Call & Form Friction](decks/audit-briefing-2.html)
3. [Missed-Call Text-Back for Local Trades](decks/audit-briefing-3.html)
4. [The 4-Point Mobile Site Audit](decks/audit-briefing-4.html)
5. [Website Decay: Why Contractor Sites Break Silently](decks/audit-briefing-5.html)

## Research paper draft

Full paper draft: [audit-paper.md](paper/audit-paper.md) — methodology + findings (n=21). Published: DOI 10.5281/zenodo.23710476.

## Citation

Derek Jamieson (Website Rescue). *Mobile-First Defects in Local Home-Services Websites: A Rendered Audit of 21 Sites (October 2026).* Zenodo. DOI: [10.5281/zenodo.23710476](https://zenodo.org/records/23710476)
6. [Five website problems that cost contractors work](articles/five-website-problems.html) — research brief citing the published study
