# Customer Segmentation and Personalized Loyalty Campaign

This project showcases the application of **customer segmentation** and the design of **personalized loyalty campaigns** using retail transaction data. It simulates the kind of work a data analyst might do at a retail-focused company like **Loyal Guru**.

---

## Project Overview

The goal of this project is to:
- Analyze historical transaction data
- Segment customers based on their purchasing behavior using **RFM (Recency, Frequency, Monetary)** analysis
- Apply **K-Means clustering** to group customers into meaningful segments
- Design **tailored loyalty campaigns** for each customer group

---

## Dataset

The dataset comes from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/online+retail) (also available on Kaggle) and contains ~540,000 retail transactions made by a UK-based online retailer from 2010 to 2011.

**Main columns used:**
- `InvoiceNo`: Unique identifier for transactions
- `CustomerID`: Unique identifier for customers
- `InvoiceDate`: Timestamp of purchase
- `Quantity`: Number of items bought
- `UnitPrice`: Price per item
- `Country`: Customer location

---

## Technologies & Libraries

- Python (3.9+)
- Pandas
- NumPy
- scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook

---

## Methodology

### 1. Data Cleaning
- Removed missing `CustomerID`s and cancelled transactions (negative quantities)
- Converted date columns to datetime format

### 2. RFM Feature Engineering
- **Recency**: Days since the last purchase
- **Frequency**: Number of purchase events
- **Monetary**: Total amount spent

### 3. Data Scaling
- Used `StandardScaler` to normalize features before clustering

### 4. Customer Segmentation
- Applied **K-Means** clustering
- Used the **Elbow Method** to determine the optimal number of clusters
- Visualized results with dimensionality
