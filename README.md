# 💳 Credit Card Fraud Detection

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-black?style=flat)](https://xgboost.readthedocs.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📌 Overview
This project develops a machine learning solution to identify fraudulent credit card transactions. Given the highly imbalanced nature of fraud data, this solution focuses on sophisticated sampling techniques and ensemble modeling to maximize detection rates while minimizing false alarms.

---

## 🎯 Objectives
* **Detection:** Identify fraudulent patterns in real-world transactional data.
* **Imbalance Management:** Utilize SMOTE to handle the minority class (fraud).
* **Feature Engineering:** Derive behavioral insights from timestamps and geolocation data.
* **Performance:** Optimize the model for **ROC-AUC** and **Recall**.

---

## 📊 Dataset Breakdown
**Source:** [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/)

| Feature Type | Description |
| :--- | :--- |
| **Transaction Info** | Amount (`amt`), Category, and Timestamp |
| **Location Data** | Customer & Merchant coordinates (Lat/Long) |
| **Target** | `is_fraud` (Binary Classification) |

---

## 🛠️ Technology Stack
* **Language:** Python
* **Data Science:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn, XGBoost
* **Sampling:** Imbalanced-learn (SMOTE)

---

## 🚀 Project Workflow

1.  **Preprocessing:** Cleaned missing values and handled duplicates.
2.  **Feature Engineering:**
    * Extracted `Hour`, `Day`, and `Month` from timestamps.
    * Calculated **Haversine Distance** between customer and merchant.
    * Derived customer age from DOB.
3.  **EDA:** Identified that late-night transactions and extreme distances are high-risk indicators.
4.  **Balancing:** Applied **SMOTE** to address the class imbalance.
5.  **Modeling:** Compared Logistic Regression, Random Forest, and **XGBoost**.

---

## 📉 Results & Insights
* **Top Model:** **XGBoost** delivered the highest ROC-AUC score.
* **Key Drivers:** Transaction amount, distance to merchant, and hour of day were the strongest predictors of fraud.
* **Visualizations:** The project includes deep dives into transaction patterns and category-wise fraud distribution.

---

## ⚙️ How to Run

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/ShitalDatascience/credit-card-fraud.git](https://github.com/ShitalDatascience/credit-card-fraud.git)
    ```
2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Launch the analysis:**
    ```bash
    jupyter notebook credit-card-fraud-detection.ipynb
    ```

---

## 📂 Project Structure
```text
credit-card-fraud/
├── data/               # Dataset files
├── visualizations/     # Analysis plots (Fraud trends, Distance patterns)
├── credit-card-fraud-detection.ipynb  # Main analysis & modeling
├── requirements.txt    # Project dependencies
└── README.md           # Project documentation
