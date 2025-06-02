# MIS-451
Machine Learning for Business
# Credit Card Default Prediction

**Final Project for MIS 451 – Machine Learning for Business**

This project aims to predict credit card default risk using the UCI "Default of Credit Card Clients" dataset. We built and compared several classification models, including traditional machine learning and deep learning methods.

---

## 🔍 Overview

- **Dataset**: [UCI Default of Credit Card Clients](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)
- **Records**: 30,000
- **Features**: 23 (demographics, billing, payment history)
- **Target**: Default payment next month (1 = yes, 0 = no)

---

## 📊 Steps in the Project

### 1. Exploratory Data Analysis (EDA)
- Checked class imbalance (23% default, 77% non-default)
- Visualized demographic distributions
- Heatmap showed strong correlations with recent repayment behavior (`PAY_0`, `PAY_2`, etc.)

### 2. Data Cleaning & Transformation
- Handled invalid values in `EDUCATION`, `MARRIAGE`
- One-hot encoding for categorical fields
- Feature engineering: `TOTAL_BILL_AMT`, `TOTAL_PAY_AMT`
- Feature selection using `SelectKBest`
- Scaled features using `StandardScaler`
- Used SMOTE to handle class imbalance

### 3. Model Development
| Model                 | Accuracy | Default F1-score | AUC     |
|----------------------|----------|------------------|---------|
| Logistic Regression  | 64%      | 0.44             | 0.7089  |
| Random Forest        | 78%      | 0.50             | 0.7356  |
| SVM (RBF Kernel)     | 77%      | 0.52             | 0.7469  |
| MLP Neural Network   | **80%**  | **0.52**         | **0.7572**  |

---

## 📌 Key Insights
- **Most important predictors**: Recent repayment statuses (`PAY_0`, `PAY_2`, `PAY_3`)
- Demographic variables (e.g., age, gender) were weak predictors
- Deep learning model (MLP) performed best overall

---

## 👨‍👩‍👧‍👦 Team Members (Group 4 Pieces)
| Name                  | Role                          |
|-----------------------|-------------------------------|
| Bùi Gia Tuệ           | Coding, Slide Design          |
| Nguyễn Thanh Giang    | Model Selection, Data Prep    |
| Bùi Thị Thanh Thảo    | Feedback, Presenter           |
| Trần Tiến Thảo Hiếu Ngân | Final Edits, Process Improvement |

---

## 💻 Tools Used
- Python (Google Colab)
- Scikit-learn
- Pandas / NumPy / Matplotlib / Seaborn
- Keras (for MLP)

---

## 📂 Repository Structure
├── data/ # Raw dataset
├── notebooks/ # Colab notebooks for EDA & Modeling
├── images/ # Plots & visualizations
├── report.pdf # Final project report
└── README.md # This file

---

## 📚 References
- UCI ML Repository: [Default of Credit Card Clients](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)
