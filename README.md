# Supplier Risk Scoring System Using Machine Learning

## Overview
This project develops a machine learning-based supplier risk assessment framework for procurement and supply chain operations. The system predicts delivery delay risk using historical supplier behavior and operational metrics, and further extends the prediction into a multi-factor supplier scoring system.

The project combines predictive analytics with operational evaluation to support data-driven supplier selection and procurement decision-making.

---

## Problem Statement
Supplier delays and inconsistent vendor performance can disrupt procurement operations, increase operational costs, and negatively impact supply chain efficiency.

Traditional supplier evaluation methods generally rely on static metrics such as pricing or transaction volume, which often fail to capture dynamic supplier behavior patterns.

This project addresses the problem by building a predictive supplier evaluation system capable of identifying high-risk suppliers using machine learning and historical procurement data.

---

## Objectives
- Predict supplier delivery delay risk using machine learning
- Engineer temporal and behavioral supplier features
- Develop a multi-factor supplier scoring framework
- Categorize suppliers into operational risk groups
- Support procurement decision-making using predictive analytics

---

## Dataset
The project uses procurement and vendor transaction datasets containing supplier purchase records, delivery timelines, invoice information, payment records, and pricing details.

### Primary Files Used
- `purchases.csv`
- `purchase_prices.csv`

### Important Variables
- VendorNumber
- PurchasePrice
- Quantity
- PODate
- ReceivingDate
- InvoiceDate
- PayDate

---

## Methodology

### 1. Data Preprocessing
- Converted date columns into datetime format
- Removed irrelevant variables
- Validated delivery date consistency
- Handled missing values
- Calculated delivery duration

### 2. Feature Engineering
Key engineered features include:
- Previous supplier delay
- Rolling average delivery performance
- Recent delay frequency
- Payment delay
- Processing delay
- Temporal indicators (month, weekday)

Special attention was given to preventing data leakage by ensuring all behavioral features used only historical information.

### 3. Machine Learning Models
Two classification models were implemented:
- Logistic Regression
- Random Forest Classifier

Random Forest produced the best performance due to its ability to capture non-linear supplier behavior patterns.

---

## Model Performance
### Random Forest Performance
- Accuracy: ~86%
- Balanced precision and recall
- Effective classification across both delayed and non-delayed deliveries

---

## Supplier Risk Scoring Framework
The machine learning prediction output was extended into a multi-factor supplier scoring system.

### Final Score Components
- Delivery delay risk probability
- Operational efficiency
- Supplier stability
- Pricing consistency
- Sustainability proxy based on delivery efficiency

### Supplier Categories
- Preferred
- Moderate
- Risky

---

## Key Findings
- Historical supplier behavior was the strongest predictor of future delays
- Recent delivery performance carried higher predictive importance than static variables such as price or quantity
- Suppliers with repeated recent delays demonstrated significantly higher future operational risk
- Operational processing delays moderately influenced supplier reliability

---

## Business Applications
The proposed system can support:
- Supplier risk identification
- Vendor selection optimization
- Procurement planning
- Supply chain risk reduction
- Performance monitoring

---

## Tools and Technologies
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Google Colab

---

## Project Structure

```text
supplier-risk-scoring-project/
│
├── supplier_risk_model.ipynb
├── Supplier_Risk_Paper.pdf
└── README.md