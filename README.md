# Public Information Satisfaction Analysis

This repository contains a Machine Learning analysis to evaluate community satisfaction with Public Information Services in West Kalimantan Province. The project uses clustering and explainable AI to provide actionable insights for service improvement.

## 🚀 Project Overview
This analysis focuses on processing survey data from the Communication and Informatics Office (Diskominfo). By utilizing unsupervised learning, we segment the public based on their satisfaction levels and identify the key drivers behind their feedback.

## 🛠️ Methodology

### 1. Data Preprocessing
* **Standardization**: Applying `StandardScaler` to normalize survey features (Q1-Q15).
* **Data Cleaning**: Handling missing values and removing non-essential columns for the model.

### 2. Clustering (K-Means)
The model segments respondents into 3 distinct groups:
* **Cluster 0 (Satisfied)**: High satisfaction ratings across most indicators.
* **Cluster 1 (Neutral)**: Moderate or mixed satisfaction levels.
* **Cluster 2 (Dissatisfied)**: Low satisfaction ratings, indicating areas for urgent improvement.

### 3. Model Interpretability (SHAP)
Using **SHAP (SHapley Additive exPlanations)** with a Random Forest classifier to explain the clustering results:
* **Global Importance**: Identifying which survey questions (features) have the biggest impact on the final satisfaction score.
* **Feature Analysis**: Understanding the specific reasons why a respondent falls into the "Dissatisfied" cluster.

## 📊 Key Findings
Based on the SHAP values, the most influential factors are:
1. **Q10**: Accessibility of information systems (e.g., SIKEDIP).
2. **Q15**: Staff ethics and responsiveness.
3. **Q5**: Information accuracy and updates.

## 💻 Requirements
To run the notebook, you will need:
* Python 3.x
* Pandas & NumPy
* Scikit-learn
* Matplotlib & Seaborn
* SHAP

```bash
pip install pandas numpy scikit-learn matplotlib seaborn shap
