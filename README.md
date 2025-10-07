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

## 🧠 Model Performance

| **Model** | **ME ($)** | **RMSE ($)** | **MAE ($)** | **MPE (%)** | **MAPE (%)** | **Notes** |
|------------|------------|--------------|--------------|--------------|--------------|------------|
| Linear Regression | 1.2256 | 7.6140 | 5.8800 | -1.4676 | 16.5966 | Baseline model |
| **Random Forest** | **0.2008** | **5.7360** | **4.4204** | **-2.8545** | **12.9027** | ✅ Best performance |
| KNN | 0.7322 | 6.9516 | 5.5362 | -3.0110 | 16.2728 | Tuned with GridSearchCV |
| Decision Tree | -3.7591 | 7.5989 | 5.6497 | -10.0000 | 10.0000 | PandasAI-generated |

**Summary:**  
Among all models tested, the **Random Forest Regressor** achieved the best performance with the lowest RMSE (5.736) and MAE (4.4204), indicating higher accuracy and robustness against outliers. Linear Regression and KNN performed reasonably well, while the Decision Tree model (PandasAI-based) showed slightly higher variability in predictions.


