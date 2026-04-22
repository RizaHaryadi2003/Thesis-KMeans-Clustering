# 🏛️ SIKEDIP Citizen Satisfaction Analysis & Clustering

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-f7931e?logo=scikit-learn&logoColor=white)
![Status](https://img.shields.io/badge/Status-Work%20in%20Progress-success)

> An end-to-end Machine Learning pipeline to analyze and segment public service satisfaction (IKM) for the *Sistem Kelola Daftar Informasi Publik* (SIKEDIP) using K-Means Clustering and Explainable AI (SHAP).

## 📌 Project Overview
This repository contains the full analytical pipeline for my research on public service evaluation. The primary goal is to discover underlying patterns in citizen feedback and segment users based on their satisfaction levels. By utilizing clustering algorithms and SHAP (SHapley Additive exPlanations), this project not only groups users but also explains *why* a specific user belongs to a certain cluster.

## ⚙️ Analytical Pipeline
The project follows a comprehensive 8-step Machine Learning lifecycle:

- [x] **1. Load & Rename:** Data ingestion and standardizing feature names.
- [x] **2. Cleaning & Drop:** Handling missing values and removing irrelevant columns.
- [ ] **3. Normalization:** Scaling features using `StandardScaler` to ensure distance-based algorithms work optimally.
- [ ] **4. Exploratory Data Analysis (EDA):** Visualizing data distributions and demographic insights.
- [ ] **5. K-Means Clustering:** Applying the core Unsupervised Learning algorithm to segment users.
- [ ] **6. Cluster Evaluation:** Determining the optimal *K* and validating clusters using Elbow Method and Silhouette Score.
- [ ] **7. Interpretation:** Profiling each cluster combined with user demographics.
- [ ] **8. SHAP / Explainability:** Identifying the most dominant features driving the satisfaction score in each cluster.

## 🛠️ Tech Stack
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn
* **Explainable AI:** SHAP
* **Visualization:** Matplotlib, Seaborn

## 🚀 How to Use
1. Clone this repository:
   ```bash
   git clone [https://github.com/UsernameKamu/NamaRepoKamu.git](https://github.com/UsernameKamu/NamaRepoKamu.git)
