## 🧠 Customer Segmentation & Predictive Modeling (RFM Analysis)

This project demonstrates an end-to-end customer segmentation pipeline using **RFM analysis**, combining **SQL**, **Python**, and **scikit-learn**. It simulates a real-world marketing use case—identifying distinct customer segments and predicting high-value users—valuable for companies like **Loyal Guru**.

---

### 🔧 Tools & Technologies

* **SQL** – Data extraction, cleaning (filtered cancellations, nulls)
* **Python (Pandas, NumPy)** – Data wrangling & analysis
* **Scikit-learn** – StandardScaler, KMeans, RandomForestClassifier
* **Matplotlib / Seaborn** – Visualizations (2D/3D plots, pairplots)

---

### 📊 Workflow Summary

**1. Data Cleaning & Feature Engineering**

* Extracted transactional data via SQL; filtered invalid entries.
* Calculated RFM metrics:

  * **Recency** = Days since last purchase
  * **Frequency** = Total purchase events
  * **Monetary** = Total spend

**2. RFM Table & Normalization**

* Created RFM table per customer.
* Scaled features using `StandardScaler()` for clustering.

**3. Clustering with KMeans**

* Identified **5 optimal clusters** using the Elbow Method & Silhouette Score.
* Labeled customers and profiled segments based on average RFM values.

**4. Data Visualization**

* 2D & 3D scatterplots, bubble charts, and pairplots to explore cluster separation and behavior.

**5. Predictive Modeling (Supervised)**

* Trained a **Random Forest classifier** using cluster labels as targets to predict customer segment from raw RFM data.
* Achieved **100% accuracy** on test data.

---

### 📌 Segment Summary (RFM Clustering Results)

| Cluster | Recency | Frequency | Monetary (€) | Customers | Description             |
| ------- | ------- | --------- | ------------ | --------- | ----------------------- |
| 0       | 43.3    | 3.9       | €1,191       | 2,932     | 😊 Moderate but Stable  |
| 1       | 246.1   | 1.9       | €491         | 1,044     | ⚠️ At-Risk/Churned      |
| 2       | 5.8     | 92.8      | €55,470      | 20        | 💰 High-Value Loyalists |
| 3       | 12.6    | 21.0      | €7,784       | 318       | 🔁 Loyal & Engaged      |
| 4       | 3.0     | 64.7      | €241,137     | 3         | 🏆 Elite VIPs           |

---

### 💡 Strategic Recommendations

* **Cluster 4 (Elite VIPs):** White-glove treatment, concierge services, priority support.
* **Cluster 2 (High-Value Loyalists):** Retain with exclusive offers, early access to products.
* **Cluster 3 (Loyal & Engaged):** Reward loyalty, upsell with bundles or subscriptions.
* **Cluster 0 (Moderate but Stable):** Build engagement via loyalty points or seasonal promos.
* **Cluster 1 (At-Risk):** Launch reactivation campaigns (discounts, reminders, feedback loops).

---

### 🔍 Predictive Modeling Highlights

| Metric    | Value |
| --------- | ----- |
| Accuracy  | 1.00  |
| Precision | 1.00  |
| Recall    | 1.00  |
| F1-Score  | 1.00  |

> 🌟 Perfect classification suggests RFM features hold strong predictive value for customer lifetime segments.

---

### 🚀 Business Value

* **Customer understanding:** Clear personas for targeting, retention, and upselling.
* **Scalable segmentation:** Automatically tag new customers via ML.
* **Data-driven campaigns:** Personalized marketing with higher ROI.
