# 🏡 House Price Prediction: End-to-End ML Pipeline

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kathyanusha05465/house-price-ml-pipeline/blob/main/Notebooks/01_data_cleaning_and_models.ipynb)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange.svg)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Predicting house price per unit area** using **Linear Regression, Random Forest, KNN, and Decision Tree** models.  
> Built end-to-end with **Python, scikit-learn, and matplotlib**.  
> Demonstrates **data preprocessing, model tuning, evaluation metrics (RMSE, MAE, MAPE, R²)**, and visualization.

---

## 🎯 Project Overview

This project predicts real estate prices based on features such as **house age, location coordinates, and proximity to MRT stations**.  
The pipeline covers **data cleaning, outlier handling, feature selection, and model comparison** to identify the most accurate predictor.

**🏆 Best Model:** Random Forest (lowest RMSE & MAE).

---

## 🚀 Try It in Google Colab

| Notebook | Description | Open in Colab |
|-----------|--------------|---------------|
| **01_data_cleaning_and_models.ipynb** | ✅ Main reproducible ML pipeline with all visuals | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kathyanusha05465/house-price-ml-pipeline/blob/main/Notebooks/01_data_cleaning_and_models.ipynb) |
| **02_data_preparation_pandasAI.ipynb** | ⚠️ Experimental PandasAI-assisted data preparation (requires OpenAI API key) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kathyanusha05465/house-price-ml-pipeline/blob/main/Notebooks/02_data_preparation_pandasAI.ipynb) |
| **03_decision_tree_pandasAI.ipynb** | ⚠️ AI-assisted Decision Tree modeling (requires OpenAI API key) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kathyanusha05465/house-price-ml-pipeline/blob/main/Notebooks/03_decision_tree_pandasAI.ipynb) |

> 💡 **Note:** Only `01_data_cleaning_and_models.ipynb` runs fully in Colab.  
> The other two are included for reference (AI-assisted workflows using PandasAI).

---

## 🔍 Key Highlights

- **Preprocessing:** Outlier removal, percentile capping, column normalization, feature engineering  
- **Models:** Linear Regression, Random Forest, KNN, Decision Tree  
- **Tuning:** GridSearchCV for Random Forest and KNN  
- **Metrics:** RMSE, MAE, MAPE, R²  
- **Visuals:** Correlation heatmap, feature importance, decision tree, actual vs predicted, residuals  

---

## 🧠 Model Performance

| Model | RMSE | MAE | MAPE (%) | R² | Notes |
|-------|------|-----|-----------|----|-------|
| Linear Regression | 7.614 | 5.880 | 16.6 | 0.89 | Baseline model |
| **Random Forest** | **5.736** | **4.420** | **12.9** | **0.93** | ✅ Best performer |
| KNN | 6.951 | 5.536 | 16.2 | 0.90 | Tuned via GridSearchCV |
| Decision Tree | 7.598 | 5.649 | 10.0 | 0.88 | Interpretable but less accurate |

---

## 📊 Visual Insights

| Visualization | Description |
|----------------|--------------|
| Correlation Heatmap | Relationship among numeric variables |
| Feature Importance | Top drivers of house price |
| Decision Tree | Interpretable tree structure |
| Actual vs Predicted | Model fit visualization |
| Residual Distribution | Error distribution after prediction |

_All visuals are saved in the `Reports/` folder._

---

## 📁 Repository Structure

| Folder/File | Description |
|--------------|-------------|
| `Data/` | Raw dataset (`real_estate.csv`) |
| `Notebooks/` | Source notebooks (EDA, preprocessing, modeling, PandasAI) |
| `Reports/` | Visualizations and model outputs |
| `References/` | Slides and final report |
| `Requirements.txt` | Python dependencies |
| `README.md` | This documentation |
| `LICENSE` | [MIT License](LICENSE) |

---

## ⚙️ How to Reproduce (Locally)

```bash
# Clone the repository
git clone https://github.com/kathyanusha05465/house-price-ml-pipeline.git
cd house-price-ml-pipeline

# (Optional) Create and activate a virtual environment
python -m venv venv
source venv/bin/activate       # macOS/Linux
venv\Scripts\activate          # Windows

# Install dependencies
pip install -r Requirements.txt

# Run the main notebook
jupyter notebook Notebooks/01_data_cleaning_and_models.ipynb

```
---

## 👩‍💻 Author

**Kathy Anusha Felix**  
🎓 Data Analyst & ML Enthusiast  
📍 Humber College, Toronto, Canada  
🔗 [LinkedIn](https://linkedin.com/in/kathy-anusha-felix-586977218)  
💻 [GitHub](https://github.com/kathyanusha05465)  
📧 [Email](mailto:kathyanusha05465@gmail.com)

---

## 🌟 Summary

This repository demonstrates a **complete end-to-end ML pipeline**, including:

- Real-world data cleaning and feature engineering  
- Multiple regression models with comparison  
- Visual storytelling and documentation  
- Optional AI-assisted PandasAI exploration  

> 🏆 **Final Verdict:** Random Forest achieved the best predictive accuracy and interpretability balance.

---

## 🪪 License  
Licensed under the [MIT License](LICENSE).
