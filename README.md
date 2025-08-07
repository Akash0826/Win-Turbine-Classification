# 🌬️ Wind Turbine Health Classification using Machine Learning

[![Made with Python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)
[![Machine Learning](https://img.shields.io/badge/Machine%20Learning-GradientBoosting-brightgreen)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 💡 Project Overview

This repository contains a complete end-to-end **machine learning case study** focused on predicting the **operational health of wind turbines** using historical sensor data.

> ✅ **Binary Classification**  
> 🎯 **Goal**: Predict whether a wind turbine is in a **Normal (2)** or **Abnormal (0)** state  
> 🧠 **ML Techniques**: Ensemble Learning (Gradient Boosting, XGBoost), Outlier Treatment, Imbalanced Data Handling

---

## 📁 Dataset Description

The dataset consists of monthly aggregated features per turbine:
- `WTGID`: Wind Turbine ID (categorical)
- `Loc`: Location (categorical)
- `MonthStartDate`: Date (datetime)
- `F1-F6`: Sensor-based numerical features
- `Target`: Binary class label (0 = Abnormal, 2 = Normal)

---

## ⚙️ Workflow

### 1. 🧹 Data Preprocessing
- Handled missing values (none found ✅)
- Outlier detection & treatment (`z-score`, `log`, and `median imputation`)
- Feature extraction from date

### 2. ⚖️ Class Imbalance Handling
- Applied **upsampling** to address skewed class distribution

### 3. 📊 Exploratory Data Analysis
- Correlation heatmaps
- Feature distributions
- Class balance visualizations

### 4. 🤖 Model Training & Evaluation
- Models Used:
  - Logistic Regression
  - SVM
  - KNN
  - Decision Tree
  - Random Forest
  - **Gradient Boosting**
  - **XGBoost**
- Evaluation Metrics:
  - Accuracy
  - F1 Score
  - Precision / Recall
  - ROC-AUC Curve

### 5. 🏆 Best Model Performance (Gradient Boosting)
| Metric       | Score |
|--------------|-------|
| Accuracy     | 93%   |
| F1 Score     | 0.93  |
| ROC-AUC      | 0.92  |

---

## 📌 Key Learnings

- Boosting techniques outperform bagging in most structured data scenarios
- Feature engineering + outlier treatment dramatically improves model quality
- Class imbalance is critical in binary classification — **upsampling worked well**
- Gradient Boosting models are interpretable and production-ready

---

## 📁 Repository Structure

```bash
.
├── data/
│   └── data.csv
├── notebooks/
│   └── Wind_Turbine_Data.ipynb
├── reports/
│   └── Wind Turbine - Case Study.pdf
├── images/
│   └── visuals & plots
├── README.md
└── requirements.txt
