# 🛒 SmartCart Customer Segmentation using Unsupervised Machine Learning

Customer segmentation system for an e-commerce platform, built using clustering algorithms to uncover hidden behavioural patterns and support data-driven, personalised marketing.

## 📌 Problem Statement

**SmartCart** is a growing e-commerce platform serving customers across multiple countries. The company has collected extensive customer data consisting of **2,240 customer records** and **22 attributes**, covering demographics, purchase behaviour, website activity, and campaign response.

Currently, SmartCart relies on **generic marketing and engagement strategies** applied uniformly across its entire customer base, without a clear understanding of the different behavioural patterns that exist within it. This results in:

- Inefficient marketing spend
- Missed opportunities to retain high-value customers
- Delayed identification of churn-prone / disengaged users

This project builds an **intelligent customer segmentation system** using **unsupervised machine learning**, analysing historical transaction and engagement data to group customers into meaningful clusters based on purchasing behaviour, engagement levels, and loyalty indicators — enabling targeted, data-driven marketing and retention strategies.

## 📊 Dataset

The dataset contains 2,240 customer records with 22 attributes, grouped into four categories:

| Category | Example Features |
|---|---|
| **Demographics** | Year_Birth, Education, Marital_Status, Income, Kidhome, Teenhome, Dt_Customer |
| **Spending Behaviour** | MntWines, MntFruits, MntMeatProducts, MntFishProducts, MntSweetProducts, MntGoldProds |
| **Purchase Frequency** | NumDealsPurchases, NumWebPurchases, NumCatalogPurchases, NumStorePurchases, NumWebVisitsMonth |
| **Feedback & Response** | Recency, Complain, Response |

## 🎯 Objective

1. Clean and preprocess raw customer data (handle missing values, encode categorical features, remove outliers).
2. Engineer meaningful features — **Age**, **Customer Tenure**, **Total Spending**, **Total Kids**, **Living Situation**.
3. Reduce dimensionality with **PCA**, and determine the optimal number of clusters using the **Elbow Method** and **Silhouette Score**.
4. Apply and compare **K-Means** and **Agglomerative (Hierarchical) Clustering**.
5. Profile each customer segment and translate results into **actionable business recommendations**.

## 🔍 Methodology

```
Raw Data → Data Cleaning → Feature Engineering → Outlier Removal
        → One-Hot Encoding → Feature Scaling → PCA (dimensionality reduction)
        → Optimal K selection (Elbow + Silhouette) → Clustering (K-Means / Agglomerative)
        → Cluster Profiling → Business Insights
```

## 🧭 Customer Segments Identified

| Segment | Income | Spending | Age | Kids | Living Situation | Web Visits | Campaign Response |
|---|---|---|---|---|---|---|---|
| **Cluster 0 — Budget Conscious** | Low–Moderate | Low–Moderate | Slightly younger | More children | With partner | High | Poor |
| **Cluster 1 — Premium Loyalists** | High | High | Slightly older | Fewer children | With partner | Low | Average |
| **Cluster 2 — Low Engagement** | Low | Low | Slightly younger | More children | Alone | High | Average |
| **Cluster 3 — High-Value Independents** | Moderate–High | High | Slightly older | Fewer children | Alone | Low | **Best** |

## 💡 Key Business Recommendations

- **Premium Loyalists & High-Value Independents (Clusters 1 & 3):** Prioritise loyalty programs, early access offers, and personalised catalog/in-store experiences — these customers spend the most and respond best to campaigns, despite lower website engagement.
- **Budget Conscious & Low Engagement (Clusters 0 & 2):** Target with deal-driven, discount-based campaigns and web retargeting, since these segments are price-sensitive but highly active on the website.
- **Retention Watch:** Cluster 0's combination of high web activity and poor campaign response flags it as a strong candidate for win-back and re-engagement campaigns.
- **Cross-sell Opportunity:** Since Clusters 1 and 3 differ mainly in living situation and channel preference, cross-channel promotions between catalog and in-store offers could unlock incremental revenue.

## 🛠️ Tech Stack

- **Language:** Python
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn, kneed
- **Techniques:** One-Hot Encoding, StandardScaler, PCA, K-Means, Agglomerative Clustering, Elbow Method, Silhouette Score

## 📁 Repository Structure

```
├── smartcart_customer_segmentation.ipynb   # Full analysis notebook (EDA → Clustering → Insights)
├── smartcart_customers.csv                 # Raw dataset (2,240 records, 22 attributes)
└── README.md                               # Project overview
```

## 🚀 How to Run

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn kneed
   ```
3. Open and run `smartcart_customer_segmentation.ipynb` in Jupyter Notebook / JupyterLab

## 📈 Results

Using **PCA** for dimensionality reduction followed by the **Elbow Method** and **Silhouette Score** to determine the optimal number of clusters, the model segmented SmartCart's customer base into **4 distinct, business-meaningful clusters** — enabling targeted marketing strategies instead of a one-size-fits-all approach.

---

*This project was built as part of a data science portfolio to demonstrate unsupervised machine learning applied to real-world customer segmentation problems.*
