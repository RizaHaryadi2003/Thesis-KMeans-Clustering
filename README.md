from weasyprint import HTML

# Create a professional README content based on the provided Jupyter Notebook image
# Content focuses on Public Information Satisfaction Analysis using K-Means and SHAP

readme_html = """
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<style>
    @page {
        size: A4;
        margin: 20mm;
        background-color: #ffffff;
    }
    body {
        font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
        line-height: 1.6;
        color: #333;
        margin: 0;
        padding: 0;
    }
    h1 {
        color: #2c3e50;
        border-bottom: 2px solid #3498db;
        padding-bottom: 10px;
        font-size: 24pt;
    }
    h2 {
        color: #2980b9;
        margin-top: 25px;
        border-left: 5px solid #3498db;
        padding-left: 10px;
        font-size: 18pt;
    }
    h3 {
        color: #16a085;
        margin-top: 20px;
        font-size: 14pt;
    }
    code {
        background-color: #f4f4f4;
        padding: 2px 5px;
        border-radius: 3px;
        font-family: 'Courier New', Courier, monospace;
    }
    pre {
        background-color: #f8f9fa;
        border: 1px solid #e1e4e8;
        padding: 15px;
        border-radius: 5px;
        overflow-x: auto;
    }
    table {
        width: 100%;
        border-collapse: collapse;
        margin: 20px 0;
    }
    th, td {
        border: 1px solid #ddd;
        padding: 12px;
        text-align: left;
    }
    th {
        background-color: #f2f2f2;
        font-weight: bold;
    }
    .badge {
        display: inline-block;
        padding: 5px 10px;
        background-color: #3498db;
        color: white;
        border-radius: 15px;
        font-size: 0.9em;
        margin-right: 5px;
    }
    .section-box {
        background-color: #fdfdfd;
        border: 1px solid #eee;
        padding: 15px;
        margin-bottom: 20px;
    }
</style>
</head>
<body>

    <h1>Public Information Satisfaction Analysis</h1>
    <p><em>Machine Learning approach for evaluating community satisfaction on Public Information Services in West Kalimantan Province.</em></p>

    <div style="margin-bottom: 20px;">
        <span class="badge">Python</span>
        <span class="badge">K-Means Clustering</span>
        <span class="badge">SHAP Explainability</span>
        <span class="badge">Random Forest</span>
    </div>

    <h2>Project Overview</h2>
    <p>
        This project analyzes public satisfaction data regarding information services provided by the Communication and Informatics Office (Diskominfo). 
        By leveraging unsupervised learning (K-Means) for segmentation and supervised learning with explainable AI (SHAP), this model identifies 
        distinct community groups and the key factors driving their satisfaction levels.
    </p>

    <h2>Key Methodology</h2>
    
    <h3>1. Data Preprocessing</h3>
    <ul>
        <li><strong>Standardization:</strong> Feature scaling using <code>StandardScaler</code> to ensure all survey dimensions (Q1-Q15) contribute equally to the clustering.</li>
        <li><strong>Handling Outliers:</strong> Analysis of data distribution and removal of irrelevant non-numerical columns.</li>
    </ul>

    <h3>2. Unsupervised Learning: Community Segmentation</h3>
    <p>The model uses <strong>K-Means Clustering</strong> to group respondents into three distinct segments:</p>
    <ul>
        <li><strong>Cluster 0 (Satisfied):</strong> Highly satisfied respondents (High Index).</li>
        <li><strong>Cluster 1 (Less Satisfied):</strong> Respondents with average or mixed feedback.</li>
        <li><strong>Cluster 2 (Dissatisfied):</strong> Respondents reporting low satisfaction across multiple dimensions.</li>
    </ul>
    <p><em>Optimal clusters were determined using the Elbow Method and Silhouette Score.</em></p>

    <h3>3. Explainable AI (XAI) with SHAP</h3>
    <p>
        A <strong>Random Forest</strong> classifier is trained to predict cluster membership. 
        <strong>SHAP (SHapley Additive exPlanations)</strong> values are then used to interpret the model, revealing:
    </p>
    <ul>
        <li><strong>Global Feature Importance:</strong> Which survey questions most significantly impact overall satisfaction.</li>
        <li><strong>Local Interpretability:</strong> Factors that characterize specific satisfaction segments (e.g., why Cluster 2 is dissatisfied).</li>
    </ul>

    <h2>Major Findings</h2>
    <div class="section-box">
        <h3>Top Factors Influencing Satisfaction (SHAP Importance):</h3>
        <ol>
            <li><strong>Q10:</strong> Ease of access to information systems (e.g., SIKEDIP).</li>
            <li><strong>Q15:</strong> Ethics and responsiveness of the information staff.</li>
            <li><strong>Q5:</strong> Clarity and updated nature of provided data.</li>
        </ol>
    </div>

    <h2>Visualization Highlights</h2>
    <ul>
        <li><strong>Radar Charts:</strong> Profiling satisfaction across 15 dimensions per cluster.</li>
        <li><strong>SHAP Summary Plots:</strong> Visualizing the distribution of feature impacts on the model's output.</li>
        <li><strong>Correlation Heatmap:</strong> Identifying relationships between different service quality indicators.</li>
    </ul>

    <h2>Requirements</h2>
    <pre>
pip install pandas numpy matplotlib seaborn scikit-learn shap
    </pre>

    <h2>Conclusion</h2>
    <p>
        The analysis suggests that the <strong>ease of access to digital platforms</strong> and <strong>staff ethical conduct</strong> are the primary drivers of public satisfaction. 
        Improvements in these specific areas are likely to move respondents from "Less Satisfied" to "Satisfied" clusters.
    </p>

</body>
</html>
"""

HTML(string=readme_html).write_pdf("Public_Information_Analysis_README.pdf")
