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
