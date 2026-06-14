# The Buy-or-Wait Dilemma — Thesis Code

Explainable machine learning vs. econometric forecasting of B2B chemical
procurement prices (epoxy resin). Companion code for the MSc thesis
(Huong Thao Bui, 639485, Rotterdam School of Management).

## Contents
- `Code_clean.ipynb` — full analysis pipeline, runs top-to-bottom.
- `Full Data.xlsx` — monthly procurement prices and 14 macro indicators
  (2011–2026). *Add this file to the repo or note access here.*

## How to run
1. Place `Full Data.xlsx` in the same folder as the notebook.
2. Install dependencies: `pip install -r requirements.txt`
3. Open the notebook and run `Kernel → Restart & Run All`.

## Notebook structure
1. **Setup** — install + consolidated imports.
2. **Data loading and preprocessing** — uniform first-differencing
   (`load_and_preprocess_uniform`) → `df_diff`.
3. **Exploratory data analysis (Ch. 3)** — descriptive statistics,
   price/divergence figures, correlation heatmaps, unit-root tests (App. J).
4. **Model and analysis functions** — all model/SHAP function definitions
   (run before Results).
5. **Results (Ch. 4)** — 4.1 baseline, 4.2 cross-learning, 4.3 SHAP,
   4.4 robustness (OLS interactions, pre-COVID).
6. **Appendices** — K (XGBoost tuning), L (VAR/VECM), M (significance tests).

## Methods
OLS / Ridge / Lasso / ARIMAX baselines vs. tuned and relaxed XGBoost, all on
first-differenced series; SHAP for driver attribution; Pesaran–Timmermann,
Diebold–Mariano (HLN-corrected), and Johansen/VAR/VECM as significance and
complementary checks.
