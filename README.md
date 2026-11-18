# Hopkins v2 county MMR data: checks

A short note comparing the Johns Hopkins county kindergarten MMR data (v2 release) with independent sources, for Wisconsin, Kentucky, Indiana and Idaho. It backs the questions we sent to the Hopkins team.

- **Note:** `hopkins_v2_evidence.qmd` (Quarto, R). The rendered `hopkins_v2_evidence.html` is self-contained, with the code folded under each result.
- **Render it:** `quarto render hopkins_v2_evidence.qmd`. It needs R with the `tidyverse` and `knitr` packages, and internet access, because every input is read by URL.

## Data

| File | What it is | Source |
|---|---|---|
| Hopkins v2 county data (not copied here) | County kindergarten MMR coverage, 2017-18 to 2024-25 | Read directly from [enshengdong/MMR_data](https://github.com/enshengdong/MMR_data) at commit `219427a3` (`mmr_data_us_counties_v2.csv`) |
| `data/cdc_schoolvaxview_kindergarten_mmr.csv` | State kindergarten MMR coverage, survey type and footnotes | CDC SchoolVaxView, data.cdc.gov dataset `ijqb-a7ye`; snapshot of 2026-11-07 |
| `data/wisconsin_dhs_kindergarten_county.csv` | Wisconsin county kindergarten coverage, all required vaccines (every year) and MMR (from 2023-24) | Wisconsin DHS, [`p01892.xlsx`](https://www.dhs.wisconsin.gov/publications/p01892.xlsx), tab "By County", reshaped to one row per county and year; percentages as published (whole numbers, ">95" kept as text) |
| `data/kindergarten_enrollment_county.csv` | Kindergarten enrollment by county and school year for Idaho, Indiana, Kentucky and Wisconsin, used as weights | NCES Common Core of Data (public schools, grade-0 count) plus Private School Survey (kindergarten count weighted by `PFNLWT`), schools assigned to counties by location; Private School Survey off-years interpolated |

Contact: Bevin Manuelpillai, Emory University.
