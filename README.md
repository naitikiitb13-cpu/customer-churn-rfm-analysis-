# Customer Lifetime Value Prediction: Online Retail I

## 📌 Project Overview

This project implements probabilistic models to predict **Customer Lifetime Value (CLV)** for a UK-based online gift retailer. Using the **Online Retail I** dataset, we model customer purchasing behavior to estimate future transaction volume and monetary value over a 12-month horizon.

The core objective is to distinguish between "active" and "churned" customers in a **non-contractual** retail environment.

## 📊 Dataset Description

The dataset contains transactions occurring between **2009 and 2011** for a UK-registered non-store online retail business.

* **Target:** Unique all-occasion gifts.
* **Customer Base:** A mix of individual retail consumers and high-volume wholesalers.
* **Source:** [UCI Machine Learning Repository - Online Retail II](https://archive.ics.uci.edu/ml/datasets/Online+Retail+II)

### Key Attributes:

* `InvoiceDate`: Used to calculate Recency, Frequency, and T (Age).
* `Quantity` & `UnitPrice`: Used to derive Monetary value.
* `CustomerID`: Unique identifier for longitudinal tracking.
* `InvoiceNo`: Used to filter out cancellations (codes starting with 'C').

## ⚙️ Methodology

We utilize a two-stage probabilistic approach:

1. **BG/NBD Model (Beta-Geometric/Negative Binomial Distribution):** To predict the expected number of transactions and the probability of a customer being "alive."
2. **Gamma-Gamma Sub-model:** To estimate the expected average monetary value per transaction, assuming independence between frequency and monetary value.
3. **Validation:** Models are validated using RMSE, MSE, and MAE across a holdout period.

## 📈 Key Findings

* **Wholesale Impact:** High-volume wholesalers significantly skew the distribution and require specialized outlier handling.
* **Model Comparison:** The repository compares **BG-NBD**, **Pareto-NBD**, and **MBG-NBD** variants.
* **Predictive Power:** The model successfully identifies top-tier "Whale" customers who contribute to ~80% of the predicted 12-month revenue.

## 🤝 Contributing

This is a Midway Report for [Your Course/Company Name]. Suggestions for improving the Gamma-Gamma independence assumption or incorporating seasonal features are welcome.
