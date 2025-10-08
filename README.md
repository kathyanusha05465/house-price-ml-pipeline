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

## ⚙️ How to Run

Follow these steps to reproduce the results or explore the notebook:

1. **Clone this repository** (download the project)
   ```bash
   git clone https://github.com/kathyanusha05465/house-price-ml-pipeline.git
   cd house-price-ml-pipeline

## 📊 Visual Results

### 🔹 Exploratory Data Analysis
| Visualization | Description |
|----------------|--------------|
| ![Boxplot of House Price per Unit Area](Reports/Boxplot%20of%20House%20Price%20per%20Unit%20Area.png) | Distribution of house price per unit area, showing spread and outliers. |
| ![Boxplots of all numerical variables](Reports/Boxplots%20of%20all%20numerical%20variables.png) | Comparison of feature distributions before preprocessing. |
| ![Correlation Heatmap](Reports/Correlation%20heatmap.png) | Correlation matrix highlighting relationships between numerical variables. |

---

### 🔹 Model Insights
| Visualization | Description |
|----------------|--------------|
| ![Feature Importance - Random Forest](Reports/Feature%20Importance%20-%20Random%20Forest.png) | Key features influencing house price predictions (Random Forest model). |
| ![Decision Tree Structure Visualization](Reports/Decision%20Tree%20Structure%20Visualization.png) | Structure of the Decision Tree model used for interpretability. |

---

### 🔹 Model Evaluation
| Model | Actual vs Predicted | Residuals Distribution |
|--------|----------------------|------------------------|
| **Linear Regression** | ![Actual vs Predicted - Linear Regression](Reports/Actual%20vs%20Predicted%20Prices%20-%20Linear%20Regression.png) | ![Residuals Distribution - Linear Regression](Reports/Residuals%20Distribution%20-%20Linear%20Regression.png) |
| **K-Nearest Neighbors** | ![Actual vs Predicted - KNN](Reports/Actual%20vs%20Predicted%20Prices%20-%20K-Nearest%20Neighbors.png) | ![Residuals Distribution - KNN](Reports/Residuals%20Distribution%20-%20K-Nearest%20Neighbors.png) |
| **Random Forest** | ![Actual vs Predicted - Random Forest](Reports/Actual%20vs%20Predicted%20Prices%20-%20Random%20Forest.png) | ![Residuals Distribution - Random Forest](Reports/Residuals%20Distribution%20-%20Random%20Forest.png) |
| **Decision Tree** | ![Actual vs Predicted - Decision Tree](Reports/Actual%20vs%20Predicted%20Prices%20-%20Decision%20Tree.png) | — |

---

> 🧩 *Each visualization above was generated from the pipeline notebooks to analyze model performance, feature impact, and prediction accuracy.*

## 💡 Demo
For full exploration:
- Open `01_data_cleaning_and_models.ipynb` → for manual pipeline
- Open `02_data_preparation_pandasAI.ipynb` → for PandasAI-assisted prep
- Open `03_decision_tree_pandasAI.ipynb` → for automated Decision Tree



