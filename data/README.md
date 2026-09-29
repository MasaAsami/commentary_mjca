# Data

## `raw/` — untouched source files (do not edit)

NIJ Recidivism Forecasting Challenge (Georgia Department of Community Supervision / Georgia Crime Information Center).
Individuals released from Georgia prisons to parole supervision, 2013-01-01 to 2015-12-31.

| File | Source URL | Downloaded (UTC) | Bytes | SHA-256 |
|---|---|---|---|---|
| `nij-challenge2021_full_dataset.csv` | https://nij.ojp.gov/sites/nij/files/media/document/nij-challenge2021_full_dataset.csv | 2026-09-29 | 6,340,524 | `2df247209bea3ad2d861ef1624461ef73b5b792f01593da0b6f18e3de1b72f5c` |
| `nij_codebook_appendix2.pdf` | https://nij.ojp.gov/funding/recidivism-forecasting-challenge-appendix-2-codebook.pdf | 2026-09-29 | 279,704 | `fe4438c510f949a344f3ea2637b64359af232333e6470bc41f32bcb7ddf7cf11` |

- Challenge page: https://nij.ojp.gov/funding/recidivism-forecasting-challenge
- Mirror of the same dataset: https://data.ojp.usdoj.gov/Courts/NIJ-s-Recidivism-Challenge-Full-Dataset/ynf5-u8nk
- The full dataset has 25,835 rows and 54 columns. It includes `Training_Sample` (the official train/test flag).
- The codebook PDF is dated 3/29/2021.

### Column-name notes (CSV vs. codebook)

The CSV uses abbreviated names. Four columns are anonymised as `_v1`–`_v4`; they map to the codebook by position:

| CSV column | Codebook position | Codebook name |
|---|---|---|
| `_v1` | 18 | `Prior_Arrest_Episodes_PPViolationCharges` |
| `_v2` | 26 | `Prior_Conviction_Episodes_PPViolationCharges` |
| `_v3` | 27 | `Prior_Conviction_Episodes_DomesticViolenceCharges` |
| `_v4` | 28 | `Prior_Conviction_Episodes_GunCharges` |

These are renamed only in derived data (`processed/`); the raw file is unchanged.

## `processed/` — derived data

Created by `notebooks/nij_georgia_analysis.ipynb`. See `plans/nij_georgia_analysis.md` for variable definitions.
