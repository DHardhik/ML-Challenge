# ML-Challenge

# 🏥 Medical Equipments Cost Prediction Challenge

### 📘 AIT 511 — Machine Learning | IIIT Bangalore

This project predicts **transportation costs** for delivering medical equipment to hospitals using machine learning techniques.  
It was developed as part of the **Kaggle Challenge: [Medical Equipments Cost Prediction](https://www.kaggle.com/competitions/Medical-Equipments-Cost-Prediction-Challenge)**.

---

## 📂 Repository Structure


---

## 🚀 Project Overview

The goal is to **predict the transport cost** of medical equipment deliveries using data such as equipment size, supplier reliability, shipping method, and order details.  
We applied several regression techniques and compared their performance using **R²**, **MAE**, and **Kaggle leaderboard scores**.

---

## 🧮 Machine Learning Workflow

1. **Data Preprocessing**
   - Handled missing values with `SimpleImputer`
   - Scaled numerical features with `RobustScaler`
   - Encoded categorical variables using `OneHotEncoder`
   - Engineered date-based cyclic features (sine/cosine encoding)

2. **Feature Engineering**
   - Created new features such as:
     - Delivery days
     - Cyclic weekday/month encoding
     - Weekend indicators

3. **Model Training**
   - Models used:
     - Linear Regression  
     - Polynomial Regression  
     - Lasso Regression  
     - Ridge Regression  
     - Elastic Net Regression  
     - Random Forest Regressor  
     - AdaBoost Regressor  
     - XGBoost Regressor  

4. **Hyperparameter Tuning**
   - Used `GridSearchCV` for:
     - Ridge, Lasso, AdaBoost, XGBoost, ElasticNet, and RandomForest

---

## 🧠 Model Comparison

| Model                         | Leaderboard Score ↓ |
|-------------------------------|--------------------:|
| **Elastic Net (CV)**          | **3,985,281,371.543** |
| Elastic Net (Fixed)           | 4,523,090,717.491 |
| Linear (2 Features)           | 5,376,252,785.576 |
| AdaBoost (GridSearch)         | 6,240,594,182.929 |
| Ridge Regression (GridSearch) | 6,387,594,703.305 |
| Lasso Regression (GridSearch) | 6,510,598,453.306 |
| Ridge Regression (Fixed)      | 6,513,573,403.475 |
| Lasso Regression (Fixed)      | 6,515,160,094.766 |
| Linear Regression             | 6,515,164,682.050 |
| Polynomial Regression         | 9,309,575,885.102 |
| AdaBoost (Fixed)              | 11,090,862,349.089 |
| Random Forest (Fixed)         | 17,212,452,660.530 |
| XGBoost (GridSearch)          | 19,417,933,355.693 |
| Random Forest (GridSearch)    | 20,906,750,713.724 |
| XGBoost (Fixed)               | 24,642,928,711.251 |

> ✅ **Best Model:** Elastic Net Regression  
> It achieved the **lowest leaderboard score** and best generalization performance.

---

## ⚙️ Technologies Used

- **Python 3.10+**
- **Libraries:**
  - `pandas`, `numpy`, `matplotlib`, `seaborn`
  - `scikit-learn`
  - `xgboost`
- **Kaggle API** for data access and submission

---

## 📈 Key Insights

- Feature engineering for date variables improved performance significantly.
- Elastic Net provided the best trade-off between complexity and generalization.
- AdaBoost and Ridge performed decently but tended to overfit with too many estimators.
- Random Forest and XGBoost required heavy tuning but were less effective for this dataset.

---

## 👩‍💻 Team Members

| Name | Roll No | Role |
|------|----------|------|
| **Katakam Shashidhar Sai** | IMT2023567 | Team Leader |
| Mohit Jagini | IMT2023528 | Member |
| Hardhik Dhavala | IMT2023579 | Member |

📧 Contact: [katakam.shashidhar@iiitb.ac.in](mailto:katakam.shashidhar@iiitb.ac.in)

---

## 📎 References

1. Kaggle Challenge — [Medical Equipments Cost Prediction](https://www.kaggle.com/competitions/Medical-Equipments-Cost-Prediction-Challenge)
2. Project Repository — [GitHub Link](https://github.com/DHardhik/ML-Challenge)

---

## 🏁 Final Output

The final model (`ElasticNetCV`) was saved and used to generate the submission file:














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
| Linear Regression |  | ✅ |
| Polynomial Regression |  | ✅ |
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

which achieved the **best leaderboard score** on Kaggle.

---

### ⭐ If you found this repository helpful, consider giving it a star on GitHub!


## 🧩 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/Medical-Cost-Prediction-Challenge.git
   cd Medical-Cost-Prediction-Challenge
2. Open Medical Cost prediction challenge Jupyter Notebook
3. Change the train and test data set file paths for Data Processing arc and Model Training Arc too.
