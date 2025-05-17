# 📊 Customer Segmentation Using RFM and K-Means

This project applies unsupervised machine learning to perform customer segmentation using **RFM analysis (Recency, Frequency, Monetary)** and **K-Means clustering**. It helps identify distinct customer personas to support data-driven marketing, retention, and upselling strategies.

---

## 📁 Dataset

**Source**: [UCI Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)  
The dataset contains transactional data for a UK-based online retail store from 2010–2011.

---

## 🔧 Methodology

1. **Data Cleaning**
   - Removed rows with missing `CustomerID` and canceled invoices.
   - Created `TotalPrice = Quantity × UnitPrice`.

2. **Feature Engineering**
   - Calculated RFM metrics per customer:
     - `Recency`: Days since last purchase
     - `Frequency`: Count of unique invoices
     - `Monetary`: Total amount spent

3. **Normalization & Clustering**
   - Scaled RFM features using `StandardScaler`.
   - Used the **Elbow Method** and **Silhouette Score** to choose `k = 4`.

4. **PCA & Visualization**
   - Applied Principal Component Analysis for 2D plotting of clusters.
   - Created bar plots for RFM distributions by segment.

---

## 📊 Segment Definitions

| Cluster | Segment Name           | RFM Traits                                               |
|---------|------------------------|-----------------------------------------------------------|
| 2       | **Best Customers**     | Recent, frequent, and extremely high spend               |
| 0       | **Loyal High-Spending**| Active and consistent spenders                           |
| 3       | **Potential Loyalists**| Moderately recent, low frequency, average spend          |
| 1       | **At-Risk**            | Inactive, low frequency, low monetary value              |

---

## 📈 Visualizations

- 📌 **RFM Bar Chart by Segment**
- 📌 **2D PCA Cluster Projection**
- 📌 Elbow Curve and Silhouette Scores for `k` selection

---

## 💼 Business Implications

- 🎯 **Best Customers**: Prioritize with loyalty rewards and VIP offers.
- 📬 **Loyal Spenders**: Encourage via bundled deals and engagement incentives.
- 🔁 **Potential Loyalists**: Target with personalized recommendations and win-back emails.
- ⚠️ **At-Risk Customers**: Launch reactivation or feedback campaigns.

---

## 🧰 Tools & Libraries

- `Python`, `pandas`, `matplotlib`, `seaborn`
- `scikit-learn` (KMeans, StandardScaler, PCA)

---

## 🚀 How to Run

1. Clone the repo  
2. Install dependencies:  
   ```bash
   pip install pandas scikit-learn matplotlib seaborn
