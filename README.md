# 🛍️ Customer Segmentation Using K-Means Clustering

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat-square&logo=jupyter)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3+-green?style=flat-square&logo=scikit-learn)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)

---

## 📌 Project Overview

This project applies **K-Means Clustering** to segment mall customers into distinct groups based on their **Annual Income** and **Spending Score**. The goal is to help the mall's marketing team understand who their customers actually are, so they can stop running the same generic campaigns for everyone.

I built this as part of my AI/ML internship at SYNENT (Task 2). The dataset is small and clean, which made it a good starting point for learning unsupervised learning end to end — from raw data all the way to business-level recommendations.

---

## 🎯 Problem Statement

A shopping mall collected basic data about 200 customers — their age, gender, annual income, and a spending score assigned by the mall. The marketing team wants to know:

- Are there natural groups among these customers?
- Which customers are high-value?
- How should campaigns differ across groups?

There are no labels here — no one has pre-defined "segment A" or "segment B." This is a classic unsupervised learning problem, and K-Means is a straightforward and interpretable solution.

---

## 📊 Dataset Information

| Property        | Detail                                                                 |
|-----------------|------------------------------------------------------------------------|
| Source          | [Kaggle — Mall Customer Segmentation](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python) |
| File            | `Mall_Customers.csv`                                                   |
| Rows            | 200                                                                    |
| Columns         | 5 (CustomerID, Gender, Age, Annual Income, Spending Score)             |
| Missing Values  | None                                                                   |
| Target Variable | None (unsupervised)                                                    |

**Download the dataset from Kaggle and place `Mall_Customers.csv` inside the `dataset/` folder before running the notebook.**

---

## 🛠️ Technologies Used

| Library       | Purpose                            |
|---------------|------------------------------------|
| `pandas`      | Data loading and manipulation      |
| `numpy`       | Numerical operations               |
| `matplotlib`  | Base plotting                      |
| `seaborn`     | Statistical visualizations         |
| `scikit-learn`| KMeans, StandardScaler, metrics    |
| `plotly`      | Interactive 3D cluster plot        |

---

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/Lavkumarjha/synent-task2-customer-segmentation-lavkumar.git
cd synent-task2-customer-segmentation-lavkumar
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Download the dataset

- Go to: https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python
- Download `Mall_Customers.csv`
- Place it inside the `dataset/` folder

### 4. Launch the notebook

```bash
jupyter notebook customer_segmentation.ipynb
```

Run all cells top to bottom. No modifications needed.

---

## 🔄 Project Workflow

```
Load Data
    ↓
Inspect & Clean
    ↓
Exploratory Data Analysis (EDA)
    ↓
Feature Selection & Scaling
    ↓
Elbow Method → Find Optimal K
    ↓
Silhouette Score → Validate K
    ↓
K-Means Clustering (K=5)
    ↓
Visualize Clusters (2D + 3D)
    ↓
Profile Each Segment
    ↓
Business Recommendations
```

---

## 📈 Results

The Elbow Method and Silhouette Score both pointed to **K = 5** as the optimal number of clusters.

| Cluster | Label              | Avg Income | Avg Spending | Count | Priority     |
|---------|--------------------|------------|--------------|-------|--------------|
| C0      | Average            | ~$55k      | 50/100       | ~81   | Retention    |
| C1      | Careful Spenders   | ~$88k      | 17/100       | ~23   | Upsell       |
| C2      | Top Customers ⭐   | ~$87k      | 82/100       | ~22   | VIP Care     |
| C3      | Budget Shoppers    | ~$26k      | 21/100       | ~22   | Value Deals  |
| C4      | Young Spenders     | ~$26k      | 79/100       | ~35   | Brand Loyalty|

**Silhouette Score at K=5: ~0.55** — indicates reasonably well-separated clusters.

---

## 💡 Key Insights

1. Annual income and spending score are nearly uncorrelated (~0.01). Earning more does not mean spending more here.
2. Cluster 1 (high income, low spending) is the biggest untapped opportunity — 23 customers who *could* spend more but don't.
3. Cluster 2 is the smallest group but likely generates the most value per customer.
4. Young customers in Cluster 4 spend enthusiastically despite modest income — strong candidates for brand loyalty programs.
5. Gender alone is not a reliable predictor of spending behavior in this dataset.

---

## 🎓 Learning Outcomes

- Understood when and why to use unsupervised learning
- Applied the full K-Means workflow: scaling → elbow → fit → visualize
- Learned that StandardScaler is not optional — distance-based algorithms are scale-sensitive
- Practiced converting model outputs into business-level language
- Built interactive visualizations with Plotly for richer cluster exploration

---

## 🔮 Future Scope

- Test DBSCAN for noise-resilient clustering
- Try Hierarchical Clustering and compare dendrograms
- Add purchase frequency and product category data for richer segmentation
- Build a Flask API for real-time customer classification
- Integrate with a Streamlit dashboard for business-user access

---

## 👤 Author

**Lavkumar Jha**  
B.Tech — Artificial Intelligence & Machine Learning

- 📧 Email: [lavkumarjha88official@gmail.com](mailto:lavkumarjha88official@gmail.com)
- 🐙 GitHub: [github.com/Lavkumarjha](https://github.com/Lavkumarjha)
- 💼 LinkedIn: [linkedin.com/in/lavkumarjha](https://www.linkedin.com/in/lavkumarjha)

---

## 📄 License

This project is licensed under the MIT License. Feel free to use it for learning purposes.

---

*Internship Task 2 | SYNENT AI/ML Program*
