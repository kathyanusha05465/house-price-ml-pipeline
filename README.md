# 🏠 House Price Prediction — End-to-End (Team Project)

Predicts house price per unit area using **Linear Regression, Random Forest, KNN, Decision Tree**.

## What’s here
- `data/` – raw dataset (`real_estate.csv`)
- `notebooks/` – original work (EDA, cleaning, models)
- `references/` – report + slides
- `artifacts/` – (created by notebook) trained model + metrics
- `reports/` – (created by notebook) plots: actual vs predicted, residuals

## How to run (notebook-first)
1. Open the main notebook in `notebooks/`.
2. Run all cells. It will:
   - clean the data (drop ID/date, remove 78/78.3/117.5, cap MRT @ 97th pct)
   - split 60:40
   - train LR/RF/KNN/DT (with RF + KNN tuned)
   - save: `artifacts/metrics.json`, `artifacts/best_model.joblib`
   - save plots to `reports/`

## My key contributions
- Data preprocessing pipeline (outliers, capping, feature prep)
- Random Forest + KNN implementation & tuning
- Evaluation (RMSE, MAE, MAPE) and result communication

