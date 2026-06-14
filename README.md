# BAM Thesis 2026 - H.T. Bui, 639485
# Thesis Code

Explainable machine learning vs. econometric forecasting of B2B chemical procurement prices (epoxy resin).
Companion code for the Master Thesis of Huong Thao Bui (639485).

## Contents
- `Code_clean.ipynb` — Full analysis pipeline, runs top-to-bottom.
- `Full Data.xlsx` — The dataset is not available for viewing due to confidentiality agreement with the data provider. Please contact the author of this repo through email 639485hb@student.eur.nl if access to the dataset is needed.

## Note
Due to the `Full Data.xlsx` not available on the repo, the codebook had been pre-run and all results are shown. To avoid running into errors when access to the data is not granted, please **don't run the code again**.

## Notebook structure
1. **Setup** — install + consolidated imports.
2. **Data loading and preprocessing** — uniform first-differencing
   (`load_and_preprocess_uniform`) → `df_diff`.
3. **Exploratory data analysis** — descriptive statistics, price/divergence figures, correlation heatmaps, unit-root tests (App. J).
4. **Model and analysis functions** — all model/SHAP function definitions (run before Results)
5. **Results** — 4.1 baseline, 4.2 cross-learning, 4.3 SHAP, 4.4 robustness (OLS interactions, pre-COVID).
6. **Appendix** — XGBoost tuning, VAR/VECM, significance tests.

## Methods
- OLS / Ridge / Lasso / ARIMAX baselines vs. tuned and relaxed XGBoost, all on first-differenced series
- SHAP for driver attribution
- Pesaran–Timmermann, Diebold–Mariano (HLN-corrected), and Johansen/VAR/VECM as significance and complementary checks.
