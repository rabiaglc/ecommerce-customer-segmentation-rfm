# 🛒 E-Commerce Customer Segmentation & RFM Analysis (SQL + Power BI)

An end-to-end customer segmentation project utilizing RFM (Recency, Frequency, Monetary) analysis on transactional e-commerce data to identify high-value customer segments and reduce churn risk.

---

## 📌 Executive Summary
* **Total Transactions Analyzed:** 805,549 clean transactions across 5,878 unique customers.
* **Core Finding (Pareto Principle):** The **Champions** segment accounts for only ~15% of the total customer base but drives over **53% of total revenue ($269.7M / $504.4M)**.
* **Churn Alert:** High-spending customers in **At Risk** and **Can't Lose** segments represent a significant revenue recovery opportunity through targeted retention campaigns.

---

## 🛠️ Tech Stack & Workflow
* **SQL (DuckDB):** 
  * Data cleaning (filtering cancellations, zero/negative prices, missing customer IDs).
  * Feature engineering for Recency (days difference), Frequency (unique orders), and Monetary (total spend).
  * Metric quintile scoring (1–5) using **Window Functions (`NTILE(5)`)** and CTEs.
* **Python (Pandas, Matplotlib, Seaborn):** Segment validation, metric distributions, and aggregation summaries.
* **Power BI:** 
  * Star-schema dimensional modeling (1-to-Many relationship between customer profiles and transactions).
  * Dynamic DAX measures (`Total Revenue`, `AOV`, `Avg Recency`, `Revenue per Customer`).
  * Interactive executive dashboard with dynamic cross-filtering.

---

## 📊 Visualizations & Dashboard

### 1. Python Exploratory RFM Distribution
Distribution of customer volume vs. monetary value across identified segments:
![RFM Segment Distribution](rfm_segment_dagilimi.png)

---

### 2. Interactive Power BI Executive Dashboard
Dynamic cross-filtering dashboard tracking segmentation KPIs and high-value product preferences:
![Power BI Dashboard](dashboard_preview.png)
---


