# 🏡 House Price Prediction — End-to-End ML Pipeline

> **Predicting house price per unit area** using **Linear Regression, Random Forest, KNN, and Decision Tree** models.  
> A complete, reproducible pipeline demonstrating **data preprocessing, model tuning, and evaluation metrics (RMSE, MAE, MAPE, R²)** — built with **Python, scikit-learn, and matplotlib**.

---

## 🎯 Project Overview

This end-to-end machine learning project predicts real estate prices based on housing features such as age, location coordinates, and proximity to MRT stations.  
The pipeline includes **data cleaning, outlier handling, feature selection, and model comparison** to determine the most accurate predictor.

**Best Model:** Random Forest (lowest RMSE & MAE).

---

## 🚀 Try It in Google Colab

| Notebook | Description | Open in Colab |
|-----------|--------------|---------------|
| **01_data_cleaning_and_models.ipynb** | ✅ Main reproducible ML pipeline with all visuals | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kathyanusha05465/house-price-ml-pipeline/blob/main/Notebooks/01_data_cleaning_and_models.ipynb) |
| **02_data_preparation_pandasAI.ipynb** | ⚠️ Experimental PandasAI-assisted data preparation (requires OpenAI API key) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kathyanusha05465/house-price-ml-pipeline/blob/main/Notebooks/02_data_preparation_pandasAI.ipynb) |
| **03_decision_tree_pandasAI.ipynb** | ⚠️ AI-assisted Decision Tree modeling (requires OpenAI API key) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kathyanusha05465/house-price-ml-pipeline/blob/main/Notebooks/03_decision_tree_pandasAI.ipynb) |

> 💡 **Note:** Only the first notebook (`01_data_cleaning_and_models.ipynb`) runs fully in Colab.  
> The other two are provided for reference (AI-assisted workflows using PandasAI).

---

## 🔍 Key Highlights

- **Preprocessing:** Outlier removal, percentile capping, column normalization, feature engineering  
- **Models Implemented:** Linear Regression, Random Forest, KNN, Decision Tree  
- **Hyperparameter Tuning:** GridSearchCV for Random Forest and KNN  
- **Evaluation Metrics:** RMSE, MAE, MAPE, R²  
- **Visualization Outputs:**
  - Correlation Heatmap  
  - Feature Importance Plot  
  - Decision Tree Visualization  
  - Actual vs Predicted Scatterplots  
  - Residuals Distribution  

---

## 🧠 Model Performance

| Model | RMSE ($) | MAE ($) | MAPE (%) | R² | Notes |
|-------|-----------|---------|-----------|----|-------|
| Linear Regression | 7.6140 | 5.8800 | 16.60 | 0.89 | Baseline model |
| **Random Forest** | **5.7360** | **4.4204** | **12.90** | **0.93** | ✅ Best performance |
| KNN | 6.9516 | 5.5362 | 16.27 | 0.90 | Tuned via GridSearchCV |
| Decision Tree | 7.5989 | 5.6497 | 10.00 | 0.88 | Interpretable but less accurate |

---

## 📊 Visual Insights

| Visualization | Description |
|----------------|--------------|
| **Correlation Heatmap** | Relationships among numerical features |
| **Feature Importance Plot** | Shows key drivers of price in the Random Forest model |
| **Decision Tree Visualization** | Displays interpretable decision tree structure |
| **Actual vs Predicted Scatterplots** | Compare predicted vs actual house prices |
| **Residuals Distribution** | Shows model fit and bias patterns |

_All plots are saved in the_ **`Reports/`** _folder._

---

## 📁 Repository Structure

| Folder/File | Description |
|--------------|-------------|
| `Data/` | Raw dataset (`real_estate.csv`) |
| `Notebooks/` | Source notebooks (EDA, preprocessing, modeling, PandasAI) |
| `Reports/` | Visualizations and model comparison charts |
| `References/` | Project slides and final report |
| `Requirements.txt` | Python dependencies |
| `README.md` | This documentation |

---

## ⚙️ How to Reproduce (Locally)

> You don’t need to run anything to see the results — everything is visualized above.  
> But if you want to reproduce locally:

```bash
# 1️⃣ Clone the repository
git clone https://github.com/kathyanusha05465/house-price-ml-pipeline.git
cd house-price-ml-pipeline

# 2️⃣ (Optional) Create and activate a virtual environment
python -m venv venv
source venv/bin/activate       # macOS/Linux
venv\Scripts\activate          # Windows

# 3️⃣ Install dependencies
pip install -r Requirements.txt

# 4️⃣ Run the main notebook
jupyter notebook Notebooks/01_data_cleaning_and_models.ipynb
