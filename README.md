### 📂 ML Challenge Repository

# 🏥 01_Medical Equipments Cost Prediction Challenge
This project predicts **transportation costs** for delivering medical equipment to hospitals using machine learning techniques.  
It was developed as part of the **Kaggle Challenge: [Medical Equipments Cost Prediction](https://www.kaggle.com/competitions/Medical-Equipments-Cost-Prediction-Challenge)**.

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

# 🅑 02_Multidimensional Personality Cluster Prediction  
**Assignment 2: Multinomial Classification**

## 🎯 Objective
To predict an individual's **personality cluster (A–E)** based on behavioral and lifestyle attributes.

## 📊 Dataset
- `train.csv`: **1,913 × 14**
- `test.csv`: **479 × 13**
- **Target:** `personality_cluster`

## 🧮 Feature Categories
- **Numerical:** age group, upbringing influence, focus intensity, consistency score  
- **Binary:** identity code, external guidance usage  
- **Categorical:** cultural background (numerically encoded)

## 🔬 Feature Engineering
- Focus squared  
- Log focus  
- Focus–consistency interaction  
- Activity strength  
- Stability mean  
- Guidance ratio  

## ⚙️ Preprocessing
- Scaling: Standard, Min–Max, Robust  
- Encoding: One-Hot & Label Encoding  
- Missing Values: None  

## 📊 EDA Highlights
- Strong positive correlation between **consistency score and Cluster E**
- Heavy class overlap → **non-linear decision boundaries**
- Most features show **low linear separability**

## 🤖 Models Implemented
- Support Vector Machine (RBF Kernel)
- Multi-Layer Perceptron (MLP) ✅ **Best**
- Logistic Regression
- Naive Bayes
- Neural Network K-Fold
- Ensemble Models

## 🏆 Best Model
- **MLP (256, 128, 64) with Label Encoding**
- **Best Leaderboard Score:** **0.627**

---
# 🅐 03_Start-up Founder Retention Prediction  
**Assignment 2: Binomial Classification**

## 🎯 Objective
To predict whether a **startup founder will stay with or leave** their startup based on personal, professional, and organizational attributes.

## 📊 Dataset
- `train.csv`: **59,611 × 24**
- `test.csv`: **14,900 × 23**
- **Target:** `retention_status`

## 🔍 Key Features
- Founder age, gender  
- Years with startup  
- Monthly revenue generated  
- Work-life balance rating  
- Funding rounds led  
- Education background  
- Startup stage  
- Leadership scope  
- Startup reputation  
- Founder visibility  

## ⚙️ Data Preprocessing
- **Numerical Missing Values:** Filled using **Median**
- **Categorical Missing Values:** Filled using **Mode / "Unknown"**
- **Scaling:** StandardScaler
- **Encoding:** One-Hot Encoding

## 📊 Exploratory Data Analysis
- Boxplots for outlier detection  
- Histograms for feature distribution  
- Violin plots for group comparison  
- Correlation heat maps for numeric relationships  

### Key Insight:
> Numeric features alone show **weak separation** between retention classes → retention is influenced by **multi-feature interactions**.

## 🤖 Models Implemented
- Logistic Regression  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN) ✅ **Best**
- Naive Bayes  
- XGBoost  
- Multi-Layer Perceptron (MLP)
- Stacking & Ensemble Methods  

## 🏆 Best Model
- **K-Nearest Neighbors (KNN)**
- **Best Kaggle Score:** **0.749**
- Feature-scaled input with optimized neighbors

# 🌴 Spatial Analysis of Tree Data Analysis

---

## 📎 References
Kaggle Links:
      - [Medical Equipments Cost Prediction](https://www.kaggle.com/competitions/Medical-Equipments-Cost-Prediction-Challenge)
      - [Start-up Founder Retention Prediction](https://www.kaggle.com/competitions/start-up-founder-retention-prediction)
      - [Medical Equipments Cost Prediction](https://www.kaggle.com/competitions/multidimensional-personality-cluster-prediction)
      - [Tree Dataset](https://www.kaggle.com/datasets/yashdogra/treeseu)
---
## 🧩 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/Medical-Cost-Prediction-Challenge.git
   cd Medical-Cost-Prediction-Challenge
2. Open chosen challenge Jupyter Notebook
3. Change the train and test data set file paths for Data Processing arc and Model Training Arc too.
