---
title: "The Chitta Pandemic — Punjab's Drug Crisis, 2010–2026"
description: "A data-driven, evidence-graded research showcase on the Punjab drug epidemic: consumption, crime, politics, money flows, prices and deaths, 2010 to 2026."
---

# The Chitta Pandemic 🪔

> A standalone, single-file research page dissecting the drug pandemic in Punjab, India — and what its numbers mean for the people, politics and money behind it.

**Live site:** publish [`index.html`](index.html) as-is via GitHub Pages (Jekyll auto-builds it).

## The questions this page answers

| # | Question | Section |
|---|---|---|
| 1 | **What** is the size of the crisis? | Consumption, cases, seizures, deaths, addicts |
| 2 | **Who** are the actors and how proven is each link? | Convicted / charged / alleged, tiered |
| 3 | **Why** did it explode, and why did governments fail? | Structural causes + 10 failure modes |
| 4 | **Who** are the parties that came to power and what do the records say? | SAD-BJP, Congress, AAP — with legal links |
| 5 | **Where** does the money go? | Price ladder, money flows, black economy |
| 6 | **How** much does it cost? | Per addict, per year, per government |

## Method

- **Sources (primary first):** NCRB data via MHA's written answers in Parliament (Rajya Sabha Q.1987, Lok Sabha Q.2597, Dec 2025); Punjab Opioid Dependence Survey (PODS) 2015; PGIMER 2022 surveys; court affidavits; Vigilance ED chargesheets (incl. ~40,000-page Majithia file, Oct 2026).
- **Method (secondary):** investigative press (Indian Express, Frontline, The Wire, The Hindu, Tribune, Al Jazeera, Livemint, IndiaSpend, Rediff), academic reviews (Discover Public Health, Springer, 2025), field studies (CRRID).
- **Confidence grading:** `HIGH` (official/auditable), `MEDIUM` (research or press citing official records directly), `LOW` (estimates/allegations — clearly labelled), `GAP` (no reliable data exists; treated as a finding).

## Key figures (as of November 2026)

- **2.33 lakh** opioid-dependent · **8.6 lakh** opioid users (PODS 2015)
- **~₹7,500 cr** annual drug-consumption market (PODS 2015; heroin alone ~₹6,500 cr)
- **9,025–12,442** NDPS cases registered per year (NCRB/MHA)
- **106** certified overdose deaths in 2024 — the highest in India that year
- **₹6,830/month** average spend per addict (field survey 2022) ≈ **₹82,000/year**
- **₹2.96 cr** central treatment funding vs. **~₹7,500 cr** of consumption → a **2,500 : 1** ratio

## License

All content is research commentary — cite sources as listed in the page's footer; do not present the page as an official document.

## Deploy

```yaml
# .github/workflows/pages.yml
name: Deploy static site to Pages
on:
  push:
    branches: [ main ]
  workflow_dispatch:
permissions:
  contents: read
  pages: write
  id-token: write
jobs:
  deploy:
    runs-on: ubuntu-latest
    environment: github-pages
    steps:
      - uses: actions/checkout@v4
      - uses: actions/configure-pages@v5
      - uses: actions/upload-pages-artifact@v3
        with:
          path: .
      - uses: actions/deploy-pages@v4
```
