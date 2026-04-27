# Public Information Satisfaction Analysis (Diskominfo)

*A Comprehensive Machine Learning Approach for Evaluating Community Satisfaction in West Kalimantan Province.*

## 📖 Research Background
This research aims to evaluate and map the level of community satisfaction regarding public information services provided by the Communication and Informatics Office (**Diskominfo**). In the era of digital governance, understanding user feedback is no longer enough; we need to identify the hidden patterns of dissatisfaction and the specific service dimensions that drive public trust.

Using a hybrid approach of **Unsupervised Learning** and **Explainable AI (XAI)**, this project segments respondents based on their real experiences and breaks down the "black box" of the model to provide actionable policy recommendations.

## 🚀 The 10-Stage Data Science Pipeline
This project follows a rigorous end-to-end pipeline to ensure data integrity and model reliability:

1.  **Data Acquisition**: Importing raw survey datasets (Q1-Q15) collected from public service platforms.
2.  **Exploratory Data Analysis (EDA)**: Profiling data distributions and analyzing correlations between different service dimensions.
3.  **Data Preprocessing**: Handling missing values, removing outliers, and filtering non-essential administrative metadata.
4.  **Feature Engineering**: Selecting relevant indicators that directly impact the Public Information Satisfaction Index.
5.  **Data Standardization**: Implementing `StandardScaler` to ensure all features contribute equally to the clustering distance.
6.  **Optimal Cluster Selection**: Utilizing the **Elbow Method** and **Silhouette Analysis** to mathematically determine the best number of segments (K).
7.  **Unsupervised Clustering**: Executing the **K-Means** algorithm to group the community into distinct satisfaction levels (e.g., Satisfied vs. Dissatisfied).
8.  **Model Training (Random Forest)**: Training a supervised classifier to validate the consistency and predictability of the identified clusters.
9.  **Explainable AI (SHAP Integration)**: Implementing **SHAP Values** to interpret the model’s logic and pinpoint the exact drivers of satisfaction.
10. **Actionable Insights & Reporting**: Translating model outputs into strategic recommendations for system modernization (e.g., SIKEDIP enhancements).

## 🛠️ Tech Stack
* **Language**: Python 3.x
* **Analysis**: Pandas, NumPy, Scikit-learn
* **Visualization**: Matplotlib, Seaborn
* **Interpretability**: SHAP (SHapley Additive exPlanations)
* **Platform**: Google Colab / Jupyter Notebook

## 📊 Key Findings
* **Optimal Segments**: The population was successfully divided into 3 distinct satisfaction clusters.
* **Primary Driver**: **Q10 (Digital Accessibility)**—The ease of accessing systems like **SIKEDIP** is the strongest predictor of public satisfaction.
* **Secondary Driver**: **Q15 (Staff Professionalism)**—The ethics and responsiveness of the information officers significantly impact the final index score.

## 💻 Installation & Usage
To replicate the analysis, install the required dependencies:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn shap
