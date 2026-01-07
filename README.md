# Customer Churn Prediction using RFM Analysis

## 📌 Project Overview
This project analyzes customer purchasing behavior and predicts customer churn using transaction data from an online retail store.  
The analysis includes data cleaning, exploratory data analysis (EDA), RFM (Recency, Frequency, Monetary) analysis for customer segmentation, and a baseline predictive model for churn.

## 📂 Dataset Description
The dataset used in this project contains transactional data of a UK-based retail business selling unique items.  
It includes customer purchase records with attributes such as invoice number, product code, quantity, invoice date, unit price, and customer ID.

### Data Attributes
| Attribute | Description |
|-----------|-------------|
| `InvoiceNo` | Unique identification code for each transaction |
| `StockCode` | Item/product identifier |
| `Description` | Product description |
| `Quantity` | Quantity of items purchased |
| `InvoiceDate` | Date and time of the transaction |
| `UnitPrice` | Price per unit of product |
| `CustomerID` | Unique customer identifier |
| `Country` | Country of customer |

## 🧠 Methodology

### 1. Data Cleaning
- Removed transactions without valid customer IDs
- Filtered out cancellations (negative quantities)
- Converted invoice dates to datetime format

### 2. Exploratory Data Analysis (EDA)
- Visualized purchase patterns and distributions
- Identified important trends in customer behavior

### 3. RFM Analysis
- Calculated:
  - **Recency** — days since last purchase
  - **Frequency** — number of purchases
  - **Monetary** — total spend per customer
- Created RFM score and performed customer segmentation

### 4. Predictive Modeling
- Built a baseline churn prediction model using RFM features
- Evaluated basic performance metrics (e.g., classification results)

## 🛠 Tools & Libraries
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- Jupyter Notebook

## 📁 Repository Structure

customer-churn-rfm-analysis-/
├── notebooks/
│ └── customer_churn_rfm.ipynb # Complete analysis notebook
├── results/ # Any output files or figures
├── README.md # This project summary
└── requirements.txt # Python dependencies

## 📈 Summary
This project provides insights into customer purchasing patterns, segments customers by value using RFM analysis, and predicts churn based on customer behavior — helping businesses optimize retention strategies.

