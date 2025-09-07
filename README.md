# 🏦 Banking Customer Retention Model  
*Classification modeling to predict customer churn and improve retention strategies in retail banking.*  

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)  
![pandas](https://img.shields.io/badge/pandas-EDA-green?logo=pandas)  
![numpy](https://img.shields.io/badge/numpy-Numerical-blue?logo=numpy)  
![matplotlib](https://img.shields.io/badge/matplotlib-Visualization-orange?logo=matplotlib)  
![seaborn](https://img.shields.io/badge/seaborn-EDA-blue?logo=python)  
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikit-learn)  
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)  
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)  

---

## 📌 Overview  
**Beta Bank** is losing customers steadily. Since it’s more cost-effective to retain customers than acquire new ones, the bank tasked us with building a machine learning model to predict which customers are at risk of leaving.  

The business requirement was to build a model with the **highest possible F1 score**, with a minimum passing threshold of **F1 ≥ 0.59**. Additionally, we evaluated the **AUC-ROC** metric to compare against F1 and validate overall model performance.  

---

## 📊 Dataset  
- **Source:** TripleTen Bootcamp (simulated banking dataset)  
- **Features:**  
  - Demographics: gender, age, geography  
  - Financial attributes: balance, credit score, tenure, products, estimated salary  
  - Account status: active membership flag  
- **Target:** `Exited` — binary flag indicating whether a customer churned  

---

## ⚙️ Methods & Tools  
- **Libraries:** pandas, NumPy, matplotlib, seaborn, scikit-learn  
- **Techniques:**  
  - Data cleaning and preprocessing (encoding categorical variables, scaling features)  
  - Train/validation/test split  
  - Addressing class imbalance with upsampling and class weights  
  - Model training & evaluation with:  
    - Logistic Regression  
    - Decision Tree  
    - Random Forest  
    - Dummy Classifier (baseline)  
  - Metrics: **F1 score (primary)**, **AUC-ROC (secondary)**  

---

## 📈 Results  
- **Dummy Classifier (baseline):** F1 ≈ 0.21 → confirmed imbalance problem.  
- **Logistic Regression:** Underperformed with F1 below 0.59 threshold.  
- **Decision Tree:** Improved results but still inconsistent across splits.  
- **Random Forest Classifier (best model):**  
  - F1 ≈ 0.61 on test set (above the 0.59 requirement)  
  - AUC-ROC ≈ 0.87, showing strong discriminatory power  
  - Balanced performance after applying class weights  

---

## 💡 Key Insights  
- **Random Forest Classifier** was the best-performing model, exceeding the required F1 threshold and producing strong AUC-ROC.  
- Proper handling of **class imbalance** (upsampling and class weights) was critical to boosting F1 without degrading ROC performance.  
- Beta Bank can use this model within its CRM to identify at-risk customers and target them with retention campaigns (e.g., tailored offers, personalized outreach).  

---

## 🗂 Repo Structure  
```
banking-customer-retention/
├── notebooks/ <- Final cleaned Jupyter notebook
├── notebooks_archive/ <- Raw unedited notebook
├── data/ <- Customer churn dataset
├── requirements.txt <- Dependencies
├── LICENSE <- MIT License
└── README.md <- This file
```

---

## 🚀 How to Run  
1. Clone the repo:  
   ```bash
   git clone https://github.com/Flamingo-Rocker/banking-customer-retention.git
   cd banking-customer-retention
2. Install dependencies
    ```bash
    pip install -r requirements.txt
3. Open the notebook in `/notebooks` to explore the analysis.

## 📦 Requirements
```
pandas==2.3.2
numpy==2.2.5
numpy-base==2.2.5            
numpydoc==1.9.0            
matplotlib==3.10.5           
matplotlib-base==3.10.5           
matplotlib-inline==0.1.6
seaborn==0.13.2
joblib==1.5.1
scikit-learn==1.7.1         
ipython==8.30.0
```

---

## 🙏 Acknowledgment
Developed as part of the TripleTen Data Science Bootcamp, applying machine learning classification models to predict churn, maximize F1 score, and guide customer retention strategies.
