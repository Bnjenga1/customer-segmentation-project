# 🧑‍🤝‍🧑 UK Customer Segmentation Project

This project performs customer segmentation on a UK-based online retailer using RFM (Recency, Frequency, Monetary) analysis and K-Means clustering. It is based on transaction data between December 2010 and December 2011.

The goal is to identify distinct customer groups based on purchasing behavior and generate business insights for targeted marketing strategies.

---

## 📁 Dataset

- Source: [UCI Machine Learning Repository / Kaggle](https://archive.ics.uci.edu/ml/datasets/Online+Retail)
- Records: 541,909 transactions
- Key fields: `InvoiceNo`, `StockCode`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

---

## 🧪 Project Steps

1. **Data Wrangling**
   - Removed canceled orders and missing customer IDs
   - Filtered out rows with non-positive quantity or unit price
   - Converted date fields

2. **Feature Engineering**
   - Created RFM metrics for each unique customer:
     - `Recency`: Days since last purchase
     - `Frequency`: Number of purchases
     - `Monetary`: Total amount spent

3. **Preprocessing**
   - Log transformation and standardization
   - PCA for dimensionality reduction (optional)

4. **Clustering**
   - K-Means clustering with `k=3` (chosen via Silhouette + Elbow methods)
   - Assigned cluster labels to each customer

5. **Visualization**
   - PCA scatter plot of clusters
   - Boxplots of RFM values by cluster
   - Heatmap of average RFM per cluster
   - Country-level customer distribution using Plotly

6. **Insights**
   - Identified 3 segments:
     - 💎 Lapsed VIPs (high spend, inactive)
     - 🧊 One-Time Buyers (low spend, many)
     - ⏳ Mid-Tier Customers (moderate potential)

---

## 🧠 Business Implications

- **Cluster 0**: Re-engage high spenders who’ve gone quiet
- **Cluster 1**: Nurture new buyers into regulars
- **Cluster 2**: Encourage repeat purchases with cross-selling

---

## 🛠️ Tools Used

- Python (pandas, seaborn, matplotlib, plotly)
- Scikit-learn (PCA, KMeans, Pipelines)
- Jupyter Notebook

---

## 📓 Notebook

View the full notebook here:  
👉 [uk_customer_segmentation.ipynb](./uk_customer_segmentation.ipynb)

---

## 📌 Author

**Brian Njenga Mwaura**  
[www.brianmwaura.com](https://www.brianmwaura.com)
