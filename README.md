💰 E-Commerce Customer Churn & Lifetime Value Predictor (CLV)
Project Overview
This project is an ML pipeline using RFM analysis and XGBoost/BG/NBD models to predict customer churn and lifetime value (CLV). It identifies High-Value, High-Risk customers, enabling targeted retention campaigns and optimized marketing spend for profit growth.

🚀 Features
RFM Feature Engineering: Calculates Recency, Frequency, and Monetary value for each customer from raw transaction data.

Dual Modeling Approach:

Churn: Uses an advanced classification algorithm (XGBoost) to predict the binary churn outcome.

CLV: Utilizes probabilistic models (e.g., Beta-Geometric / Negative Binomial Distribution - BG/NBD) for purchase probability and the Gamma-Gamma model for monetary value, common in non-contractual e-commerce settings.

Actionable Insights: Outputs a ranked list of customers based on their churn probability and predicted CLV for targeted marketing actions.

ML Pipeline: Structured source code for data processing, model training, evaluation, and prediction.

📁 Repository Structure
├── README.md               <-- This file.
├── requirements.txt        <-- Python dependencies.
├── .gitignore              <-- Standard Git ignore file for Python/ML projects.
├── notebooks/              <-- Jupyter notebooks for EDA, visualization, and experimentation.
│   ├── 01_EDA_and_RFM.ipynb
│   └── 02_Model_Training.ipynb
├── data/
│   ├── raw/                <-- Original, untouched data files (e.g., `ecom_transactions.csv`).
│   └── processed/          <-- Cleaned, aggregated RFM data used for training.
├── src/                    <-- Source code for the production pipeline.
│   └── model_pipeline.py   <-- Main script for data processing, training, and prediction.
└── models/                 <-- Saved model artifacts (e.g., `churn_model.pkl`, `clv_model.pkl`).

🛠️ Getting Started
Prerequisites
You need Python 3.8+ installed on your system.

1. Environment Setup
It is highly recommended to use a virtual environment.

# Create a virtual environment
python -m venv venv

# Activate the virtual environment (Linux/macOS)
source venv/bin/activate

# Activate the virtual environment (Windows)
.\venv\Scripts\activate

2. Installation
Install all required packages using pip:

pip install -r requirements.txt

3. Data Preparation
Place your raw transactional data (e.g., a CSV file with CustomerID, InvoiceDate, SalesAmount) into the data/raw/ directory.

4. Running the Model Pipeline
The main script handles data preparation, model training, and generates prediction reports.

python src/model_pipeline.py --mode=train

To run predictions on new data:

python src/model_pipeline.py --mode=predict --input_file=new_customer_data.csv

📊 Model & Metrics
Churn Prediction (Classification)
Algorithm

Key Features

Primary Metric

XGBoost Classifier

RFM, Tenure, Customer Demographics

AUC-ROC (for class imbalance), Recall @ Top 10%

CLV Prediction (Probabilistic)
Model

Approach

Primary Metric

BG/NBD + Gamma-Gamma

Probabilistic Survival Model

RMSE (Root Mean Squared Error) on holdout CLV

🤝 Contributing
Contributions are welcome! Please open an issue first to discuss the feature or bug fix.

Fork the repository.

Create a new branch (git checkout -b feature/AmazingFeature).

Commit your changes (git commit -m 'Add some AmazingFeature').

Push to the branch (git push origin feature/AmazingFeature).

Open a Pull Request.
