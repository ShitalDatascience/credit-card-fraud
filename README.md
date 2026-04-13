# credit-card-fraud
Credit Card Fraud Detection


**Overview**

This project develops a machine learning solution to detect fraudulent credit card transactions using real-world transactional data. The dataset is highly imbalanced, making fraud detection a challenging classification problem. The objective is to accurately identify fraudulent transactions while minimizing false positives.

**Objectives**

- Detect fraudulent transactions from real-world data

- Handle imbalanced dataset using advanced techniques

- Perform feature engineering to improve model performance

- Evaluate models using appropriate metrics such as ROC-AUC

- Generate insights using data visualization


**Dataset**

**Source**: Kaggle Credit Card Fraud Detection Dataset

The dataset contains transaction-level information, including:

- Transaction amount (amt)

- Category (category)

- Customer location (lat, long)

- Merchant location (merch_lat, merch_long)

- Transaction timestamp (trans_date_trans_time)

- Target variable (is_fraud)


**Data Preprocessing**

- Handled missing values using median (numerical) and mode (categorical)

- Removed duplicate records

- Converted date columns to datetime format

- Converted categorical variables into numerical format using encoding techniques


**Feature Engineering**

- Extracted time-based features such as hour, day, and month

- Derived customer age from date of birth

- Calculated distance between customer and merchant locations using geographic coordinates

- Created distance-based categories to capture transaction behavior patterns


**Exploratory Data Analysis**

Key observations from the data:

- The dataset is highly imbalanced, with a very small proportion of fraud cases.

- Fraudulent transactions tend to occur at unusual or extreme transaction amounts

- Certain categories, particularly online transactions, show higher fraud rates.

- Fraud is more likely when the transaction occurs far from the customer’s location

- Higher fraud activity is observed during late-night hours


**Handling Class Imbalance**

- Applied Synthetic Minority Oversampling Technique (SMOTE) to balance the dataset

- Improved the model’s ability to detect minority class (fraud cases)


**Models**

The following models were implemented and compared:

- Logistic Regression (baseline model)

- Random Forest (ensemble tree-based model)

- XGBoost (gradient boosting model)


**Evaluation Metrics**

Models were evaluated using:

- Accuracy

- Precision

- Recall

- F1-score

- ROC-AUC Score

- Confusion Matrix


**Results**

- Logistic Regression provided a baseline for comparison

- Random Forest achieved strong performance and handled non-linear relationships effectively

- XGBoost delivered the best overall performance with the highest ROC-AUC score and improved fraud detection


**Visualizations**

The project includes visual analysis of:

- Fraud vs non-fraud distribution

- Transaction amount patterns

- Category-wise fraud distribution

- Distance-based fraud behavior

- Time-based fraud trends
  

**Key Insights**

- Fraud is rare but follows identifiable behavioral patterns

- Transaction amount and distance are strong indicators of fraud

- Online and remote transactions have higher fraud risk

- Time of transaction (especially late-night activity) plays a significant role in fraud detection

- Top features such as transaction amount, distance, and hour strongly influence fraud detection.


**Technology Stack**

- Python

- Pandas, NumPy

- Matplotlib, Seaborn

- Scikit-learn

- XGBoost

- Imbalanced-learn (SMOTE)


**Project Workflow**

Data Loading → Data Cleaning → Feature Engineering → EDA → Encoding → Scaling → SMOTE → Model Training → Evaluation → Insights


**How to Run**

- git clone <repository-url>

- cd credit-card-fraud-detection

- pip install -r requirements.txt

- jupyter notebook


**Conclusion**

This project demonstrates that machine learning models can effectively detect fraudulent transactions by learning behavioral patterns from transaction data. Feature engineering and class imbalance handling significantly contributed to improving model performance.

**Future Work**

Develop a real-time fraud detection system

Deploy the model using Flask or FastAPI
