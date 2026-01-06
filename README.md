# 💳 Credit Card Fraud Detection: 51% Recall with K-Means
[![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-blue.svg)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
[![Python](https://img.shields.io/badge/Python-3.8+-yellow.svg)](https://www.python.org/)
[![Status](https://img.shields.io/badge/Status-Project%20Completed-green.svg)]()

## 📝 Project Overview
This project implements an **Unsupervised Machine Learning** pipeline to identify fraudulent credit card transactions. The primary challenge is the extreme class imbalance, where frauds represent only 0.17% of the total dataset.

The solution leverages **K-Means Clustering** to model normal behavior and detect frauds as outliers (anomalies), enhanced by a business rule based on transaction value (*Amount*).



## 🎯 Impact Results
| Metric | Baseline (Top 0.2%) | Final Hybrid Model | Improvement |
| :--- | :--- | :--- | :--- |
| **Recall (Caught Frauds)** | 24.4% | **45.9%** | **+88%** |
| **Saved Frauds** | 120 | **226** | **+106 frauds** |
| **Est. Financial Impact** | $60,000 | **$113,000** | **+$53,000** |

## 🚀 Technical Pipeline
The project was structured into 4 critical phases to ensure risk precision:

1.  **Exploratory Data Analysis (EDA):** Identified patterns showing that 99.8% of legitimate transactions are below $500, while frauds often exhibit atypical spending behaviors.
2.  **Preprocessing:** Data normalization using `StandardScaler` and **PCA (Principal Component Analysis)** for dimensionality reduction (essential for visualization and algorithm performance).
3.  **K-Means Algorithm:** Grouped transactions into 7 distinct clusters to define the "norm" of user behavior.
4.  **Hybrid Anomaly Detection:** Optimized the Euclidean distance threshold combined with a risk-based filter for transactions over $500.



## 💡 Key Insights
* **Risk Visualization:** PCA confirmed that frauds do not follow a time-based pattern but rather a "distance" pattern from the average behavioral centroids.
* **Operational Efficiency:** The hybrid model captures nearly half of all frauds while flagging only 0.24% of the total transaction volume for manual review, significantly reducing operational overhead.

## 🛠️ Tech Stack
* **Python:** Pandas, NumPy.
* **Scikit-Learn:** KMeans, PCA, StandardScaler.
* **Visualization:** Matplotlib, Seaborn.

## 📁 Repository Structure
* `/notebooks`: Contains the `.ipynb` file with the full end-to-end code.
* `/visuals`: PCA scatter plots and recall evolution charts.

---
**Author:** José Carriço  
**LinkedIn:** [linkedin.com/in/josé-carriço](https://www.linkedin.com/in/josé-carriço)  
**Kaggle:** [kaggle.com/joscarrio](https://www.kaggle.com/joscarrio)  
**Goal:** Transitioning to Data & AI Analyst | Focused on Risk Management & Fintech.
