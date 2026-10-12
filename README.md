# retail-uci: Customers Like You

5020 Mini-Project. Product recommendations and customer groups for GiftLane (a fictional UK gift-ware retailer), built with Truncated SVD on the UCI **Online Retail II** dataset.

**Team:** Margarita Kholostova, working alone, so both roles: Data Engineer (DE1–DE5) and ML Engineer (ML1–ML6).

## Success targets (J1)

1. **Much smaller:** the stored factors are far smaller than the full customer x product matrix.
2. **Fast:** fitting the model and recommending for all test customers takes seconds, so it fits a nightly job.
3. **Better than best sellers:** the hit rate at 10 on held-out purchases beats recommending the 10 best-selling products.
4. **Nameable groups:** the customer map shows 3–6 groups marketing can name from their products and countries.

## Data

The raw data is not stored in this repository (the file is ~45 MB).

1. Download `online_retail_II.xlsx` from the UCI Machine Learning Repository:
   https://archive.ics.uci.edu/dataset/502/online+retail+ii
2. Put it here:

```
data/raw/online_retail_II.xlsx
```

Row count after loading both sheets: **1,067,371** rows.

## How to run

```
pip install -r requirements.txt
jupyter lab
```

Open `work.ipynb` and run **Kernel → Restart & Run All**. The notebook rebuilds everything from the raw file. The train/test files, the sparse matrix (`A_train.npz`) and the index maps are written to `data/processed/`, which is not committed.

## Deliverables

| File | What it is |
|---|---|
| `work.ipynb` | The full analysis: DE1–DE5 (data) and ML1–ML6 (model, recommendations, PCA comparison, customer map) |
| `memo.pdf` | One-page memo for Sarah (J2) |
| `reflection.docx` | Individual reflection |
| Slides | 5-minute presentation (J3), submitted on Canvas |

## Contribution log (C2)

I worked alone, so every task is owned by me. The peer evaluation form (C3) does not apply to an individual (peer factor 1.00, Section 7.1).

| Date | Task | Owner | Evidence (commit) | Status |
|---|---|---|---|---|
| 2026-10-09 | Repository, `.gitignore` for raw data | Margarita Kholostova | `1f6cddc` | Done |
| 2026-10-09 | DE1: load both sheets, data profile | Margarita Kholostova | `5ab3af5` | Done |
| 2026-10-10 | DE2: cleaning and cleaning log | Margarita Kholostova | `cc4b402`, `e091960` | Done |
| 2026-10-10 | DE3: time split and held-out test purchases | Margarita Kholostova | `7e91576` | Done |
| 2026-10-10 | DE4–DE5: sparse matrix, index maps, matrix report | Margarita Kholostova | `6d0db6a` | Done |
| 2026-10-10 | ML1–ML2: method decision, SVD for k = 10–200, chosen k | Margarita Kholostova | `223caa3` | Done |
| 2026-10-11 | ML3: similar products and customer recommendations | Margarita Kholostova | `ac005f2` | Done |
| 2026-10-11 | ML4: hit rate vs best-seller baseline, popularity bonus; J1 targets, README, requirements | Margarita Kholostova | `7a65132` | Done |
| 2026-10-11 | ML5: PCA vs SVD comparison table | Margarita Kholostova | `d04a8da` | Done |
| 2026-10-11 | ML6: customer map and named segments | Margarita Kholostova | `4d5a84a` | Done |
| 2026-10-11 | R4 cleanup (no customer IDs) and notebook tidy | Margarita Kholostova | `0e0f262` | Done |
| 2026-10-11 | J2: memo for Sarah | Margarita Kholostova | `776650a`, `dd244fa` | Done |
| 2026-10-11 | J3: slides | Margarita Kholostova | Canvas | Done |
| 2026-10-12 | DE6 decision note (Stretch, skipped) and reflection | Margarita Kholostova | `689127f` | Done |
| — | DE6 & ML7 (Stretch, optional for individuals) | — | — | Not done |

Signed: Margarita Kholostova
