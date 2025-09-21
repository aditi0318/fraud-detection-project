# Fraud Detection using Machine Learning 🚨

This project demonstrates how machine learning can be applied to detect fraudulent financial transactions.  
The dataset used contains over 6 million records, with only a small fraction marked as fraudulent.  
The main challenge was handling the class imbalance while ensuring high accuracy in fraud detection.

---

## 📂 Project Workflow

1. **Data Loading & Exploration**
   - Loaded `Fraud.csv` dataset (6.3M rows).
   - Performed Exploratory Data Analysis (EDA) to understand data distribution and fraud ratio.

2. **Data Cleaning**
   - Removed duplicate records.
   - Checked for missing values (none found).
   - Identified numeric and categorical features.

3. **Feature Engineering**
   - Defined `isFraud` as the target variable.
   - Used transaction details (amount, type, balances, etc.) as features.

4. **Handling Class Imbalance**
   - Fraud cases (~0.1%) were extremely rare.
   - Created a balanced dataset by keeping all fraud cases and sampling non-fraud cases.

5. **Model Training**
   - Logistic Regression (baseline model).
   - Random Forest Classifier (stronger model).

6. **Model Evaluation**
   - Metrics: Precision, Recall, F1-score, and ROC-AUC.
   - Logistic Regression → ROC-AUC ~ 0.95  
   - Random Forest → ROC-AUC ~ 0.998 (selected as best model).

7. **Explainability**
   - Applied **Permutation Importance** to identify key features influencing fraud detection.
   - Top signals included:
     - Transaction Amount  
     - Transaction Type (TRANSFER, CASH_OUT)  
     - Balance behaviors (old and new balances)

---

## 📊 Results & Insights

- Random Forest significantly outperformed Logistic Regression.  
- Fraud detection is highly influenced by **transaction type** and **amount**.  
- Accounts with unusual or zero balances are strong indicators of suspicious activity.  

---

## 📂 Dataset

- **Fraud_sample.csv** (included in this repository under `/data`) → A small sample of 5,000 rows for quick testing.  
- **Full dataset** (6.3M rows) is too large to upload on GitHub.  
  You can download it from **[Google Drive Link](https://drive.google.com/your-link-here)** (replace with your actual link).  

---

## 🛠 Tools & Libraries

- **Python**  
- **Pandas, NumPy** → Data handling  
- **Matplotlib, Seaborn** → Visualization  
- **Scikit-learn** → ML models, metrics, and feature importance  

---

## ⚙️ Installation

Clone the repository and install dependencies:

```bash
pip install -r requirements.txt
