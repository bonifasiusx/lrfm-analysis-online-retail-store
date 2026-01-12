
# Customer Segmentation with LRFM Analysis

Customer segmentation using the **LRFM framework** and **K-Means clustering (K=3)** on a UK online retail dataset (**2009–2011**). The objective is to identify actionable customer segments for **targeting, retention, and lifecycle marketing**.

## At a Glance

- **Transactions:** 541,910
- **Customers:** 5,869
- **Total revenue:** £17.6M
- **Revenue concentration:** Top 1% customers (59) contribute **32.03%** of revenue; Top 5% (294) contribute **52.05%**
- **Segment leverage:** High-value segment (Cluster 2) covers **37.53%** of customers and contributes **85.96%** of revenue

---

## Methodology Overview

1. **Data Preparation**

   - Filtered valid transactions and non-null customer IDs
   - Handled cancellations and anomalies in transactional data
2. **LRFM Feature Engineering (Customer-Level)**

   - **Length (Tenure):** days since first purchase to **analysis date** (last transaction date + 1 day)
   - **Recency:** days since last transaction to **analysis date**
   - **Frequency:** number of **unique invoices** per customer
   - **Monetary:** total spend per customer (sum of TotalPrice)
3. **Clustering Approach**

   - Applied **log1p transformation** to skewed features (Frequency, Monetary)
   - Standardized LRFM features before clustering
   - Used **Elbow Method** and **Silhouette Score** to select **K=3**
   - Interpreted clusters using **median raw LRFM values** for business readability

---

## Key Results (K=3 Segments)

- **Segment 0: Inactive / At-Risk Customers**

  - Long tenure but low activity and low spend
- **Segment 1: Active Low-Value Customers**

  - Recent activity with low purchase frequency and spend
- **Segment 2: High-Value Recent Customers**

  - High-frequency, high-spend customers driving the majority of revenue

---

## Business Implications

- Prioritize **retention and VIP treatment** for Segment 2 due to strong revenue concentration.
- Use **low-cost win-back** tactics for Segment 0 to avoid inefficient incentives.
- Apply **bundling and cross-sell** strategies to move Segment 1 upward.

---

## Files

- `lrfm_analysis.ipynb` — Full analysis, visualizations, and segment interpretation
- `online_retail_II.xlsx` — Dataset

---

## Related Article

[Customer Segmentation with LRFM Analysis: Unlocking Insights from Retail Data (2009–2011)](https://medium.com/@alfriandocv/customer-segmentation-with-lrfm-analysis-unlocking-insights-from-retail-data-2009-2011-b3e1eb9e261f)

---

## Contributors

- [Alfriando C Vean](https://github.com/alfcvean)
- Bonifasius Sinurat

---

## Usage

```bash
git clone https://github.com/bonifasiusx/lrfm-analysis-online-retail-store.git
cd lrfm-analysis-online-retail-store
jupyter notebook lrfm_analysis.ipynb
```
