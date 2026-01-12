
# Customer Segmentation with LRFM Analysis

This project performs customer segmentation using the **LRFM framework (Length, Recency, Frequency, Monetary)** combined with **K-Means clustering** on a UK online retail dataset from  **2009–2011** .
The objective is to uncover meaningful customer segments based on purchasing behavior and customer value to support  **marketing, retention, and engagement strategies** .

---

## Purpose

This project was developed as part of the **Portfolio Build assignment** in the Data Science Bootcamp at **Purwadhika Digital Technology School** (Module 2 – Data Analysis).

The main goals of this project are to:

* Apply LRFM analysis to real-world transactional data
* Perform customer segmentation using distance-based clustering
* Practice data cleaning, feature engineering, and exploratory analysis
* Translate analytical results into **actionable business insights**

---

## Methodology Overview

1. **Data Preparation**
   * Filtered valid transactions and non-null customer IDs
   * Handled cancellations and anomalies in transactional data
2. **LRFM Feature Engineering**
   * **Length** : Duration between first and last purchase
   * **Recency** : Days since last transaction (relative to analysis date)
   * **Frequency** : Number of unique transactions
   * **Monetary** : Total purchase value per customer
3. **Clustering Approach**
   * Applied logarithmic transformation on skewed features (Frequency, Monetary)
   * Standardized LRFM features prior to clustering
   * Used **Elbow Method** and **Silhouette Score** to determine the optimal number of clusters
   * Final segmentation performed using **K-Means with K = 3**
4. **Interpretation**
   * Cluster interpretation is based on **median LRFM values in raw scale** to maintain business interpretability

---

## Key Results

The clustering process identified  **three distinct customer segments** :

* **Inactive / At-Risk Customers**
  Long relationship history but low activity and value
* **Active Low-Value Customers**
  Recently active customers with low purchase frequency and spend
* **High-Value Active Customers**
  Highly engaged customers with frequent transactions and high monetary contribution

Each segment is accompanied by targeted strategic recommendations in the analysis notebook.

---

## Business Impact

The customer segmentation results can support data-driven business decisions in several practical ways:

* **More efficient marketing allocation**
  By distinguishing inactive, low-value, and high-value customers, marketing efforts can be focused on segments with the highest potential return, reducing wasted spend on low-impact audiences.
* **Improved retention and customer lifetime value**
  Identifying high-value active customers enables targeted retention strategies, helping to preserve revenue from the most profitable customer base.
* **Personalized engagement strategies**
  Different behavioral patterns across segments allow businesses to tailor communication, promotions, and product recommendations based on customer activity and value.

---

## What You’ll Learn

* How to compute and interpret LRFM metrics
* Practical handling of skewed transactional data
* Proper use of feature transformation and scaling for clustering
* Customer segmentation using K-Means
* Translating clustering results into business strategies
* Data visualization for exploratory and explanatory analysis

---

## Files

* `lrfm_analysis.ipynb`
  Jupyter Notebook containing the full analysis, visualizations, and segment interpretation
* `online_retail_II.xlsx`
  Dataset used for the analysis

---

## Related Article

A detailed explanation of the analysis and findings is available in the accompanying Medium article:

[Customer Segmentation with LRFM Analysis: Unlocking Insights from Retail Data (2009–2011)](https://medium.com/@alfriandocv/customer-segmentation-with-lrfm-analysis-unlocking-insights-from-retail-data-2009-2011-b3e1eb9e261f)

---

## Contributors

* [Alfriando C Vean](https://github.com/alfcvean)
* Bonifasius Sinurat

---

## Usage

Clone this repository and run the notebook locally:

```bash
git clone https://github.com/bonifasiusx/lrfm-analysis-online-retail-store.git
cd lrfm-analysis-online-retail-store
jupyter notebook lrfm_analysis.ipynb
```
