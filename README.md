# Public Information Satisfaction Analysis (Diskominfo)

Analysis of community satisfaction with Public Information Services using K-Means Clustering and SHAP Explainability.

## 🚀 Data Science Pipeline
This project follows a structured 10-stage pipeline to ensure data integrity and model interpretability:

1. **Data Acquisition**: Importing raw survey datasets regarding public service satisfaction.
2. **Exploratory Data Analysis (EDA)**: Visualizing score distributions and identifying initial patterns across Q1-Q15.
3. **Data Cleaning**: Handling missing values and filtering out non-essential administrative features.
4. **Feature Engineering**: Selecting specific dimensions of public information for targeted analysis.
5. **Data Scaling**: Implementing `StandardScaler` to normalize the feature range for distance-based algorithms.
6. **Optimal Cluster Selection**: Utilizing the **Elbow Method** and **Silhouette Analysis** to determine the best number of segments.
7. **K-Means Clustering**: Segmenting the community into distinct satisfaction groups (e.g., Satisfied vs. Dissatisfied).
8. **Supervised Learning**: Training a **Random Forest** classifier to validate and predict cluster membership.
9. **Explainable AI (SHAP)**: Generating SHAP values to identify which factors (like SIKEDIP accessibility) drive satisfaction.
10. **Strategic Insights**: Formulating data-driven recommendations for government policy improvement.

## 🛠️ Tech Stack
* **Language**: Python
* **Libraries**: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, SHAP
* **Environment**: Google Colab / Jupyter Notebook

## 📊 Key Results
* **Optimal Clusters**: 3 Distinct Community Segments.
* **Top Satisfaction Driver**: Q10 (Ease of access to information systems like SIKEDIP).
* **Secondary Driver**: Q15 (Staff ethics and responsiveness).

## 💻 Installation
To replicate this analysis, install the required dependencies:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn shap
