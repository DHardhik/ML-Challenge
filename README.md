# ML-Challenge

# 🏥 Medical Equipment Transport Cost Prediction Challenge

This repository contains my complete work for the **Medical Cost Prediction Challenge (Ck 1)**.  
The goal of this project is to predict the **transport cost of medical equipment** based on features such as equipment type, supplier reliability, dimensions, and delivery details.  
All experiments were performed using multiple machine learning models, evaluated, and compared systematically.

---

## 📂 Repository Structure


---

## 🧠 Models Implemented

| Model | With GridSearchCV | Without GridSearchCV |
|:------|:-----------------:|:--------------------:|
| Linear Regression | ✅ | ✅ |
| Polynomial Regression | ✅ | ✅ |
| Ridge Regression | ✅ | ✅ |
| Lasso Regression | ✅ | ✅ |
| Elastic Net Regression | ✅ | ✅ |
| Random Forest Regressor | ✅ | ✅ |
| XGBoost Regressor | ✅ | ✅ |
| AdaBoost Regressor | ✅ | ✅ |

---

## ⚙️ Key Features

- Complete **data preprocessing pipeline** using `ColumnTransformer`  
- Feature extraction from **date columns** (delivery duration, weekends, cyclic encoding)  
- **Model comparison** based on R², MAE, and RMSE  
- **GridSearchCV hyperparameter tuning** for performance optimization  
- Automated **CSV submission file generation** for Kaggle leaderboard  
- Final report summarizing the findings and scores

---

## 📊 Results Summary

| Model | R² Score | RMSE | Remarks |
|-------|-----------|------|----------|
| **ElasticNet (GridSearch)** | 0.295 | 39,540 | ✅ Best performing model |
| SVR | 0.390 | 36,782 | Competitive but less stable |
| Kernel Ridge | 0.036 | 46,250 | Underperformed |
| Other models | — | — | See report for details |

Final leaderboard score was achieved using **ElasticNet Regression (GridSearch)**.

---

## 🧩 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/Medical-Cost-Prediction-Challenge.git
   cd Medical-Cost-Prediction-Challenge
