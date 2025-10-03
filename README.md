# 📈 Ecommerce Customer Churn & LTV Prediction

[![Python](https://img.shields.io/badge/Python-3.12-blue)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-1.3.0-green)](https://scikit-learn.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-1.7-orange)](https://xgboost.readthedocs.io/)

This project implements a **two-phase ML pipeline** for predicting customer churn and lifetime value (LTV) in ecommerce.

---

## 🔹 Features

### 1️⃣ Customer Churn Classification
- Predicts high-risk customers using **RFM features** (Recency, Frequency, Monetary)  
- **Gradient Boosting Classifier** used for robust churn prediction  
- Achieved **~92% AUC** (example metric)

### 2️⃣ Customer Lifetime Value (LTV) Regression
- Predicts future sales of active customers using **Gradient Boosting Regressor**  
- Handles **skewed revenue** via log-transformed targets  
- Achieved **~49% R² in log-space**

---

## 🗂️ Data

- Place your dataset in: `data/data.csv`  
- Required columns:  
  - `CustomerID`  
  - `InvoiceDate`  
  - `Quantity`  
  - `UnitPrice`  

> ⚠️ Example dataset not included due to privacy, but dummy data can be used for testing.

---

## ⚙️ Setup

```bash
git clone <repo-url>
cd ecommerce-churn-ltv
pip install -r requirements.txt


