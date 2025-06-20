# <span style="font-family: Arial, sans-serif; color: #2E86C1;">Greenhouse Gas (GHG) Emissions Prediction Project</span>

## <span style="font-family: Arial, sans-serif; color: #2E86C1;">Overview</span>
<p style="font-family: Arial, sans-serif; font-size: 14px;">
This project focuses on analyzing and predicting greenhouse gas (GHG) emissions from various U.S. industries and commodities using supply chain emission data from 2010 to 2016. The goal is to develop a regression model that can predict the <strong>"Supply Chain Emission Factors with Margins"</strong> based on descriptive and quality metrics such as substance type, unit of measurement, and reliability scores.
</p>

---

## <span style="font-family: Arial, sans-serif; color: #2E86C1;">Dataset</span>
<p style="font-family: Arial, sans-serif; font-size: 14px;">
The dataset is sourced from the <a href="https://catalog.data.gov/dataset/supply-chain-greenhouse-gas-emission-factors-for-us-industries-and-commodities" style="color: #3498DB; text-decoration: none;">U.S. Environmental Protection Agency (EPA)</a> and includes the following key columns:
</p>

<ul style="font-family: Arial, sans-serif; font-size: 14px;">
  <li><strong>Code</strong>: Industry or commodity classification code.</li>
  <li><strong>Name</strong>: Name of the industry or commodity.</li>
  <li><strong>Substance</strong>: Type of GHG (e.g., carbon dioxide, methane, nitrous oxide).</li>
  <li><strong>Unit</strong>: Measurement units (e.g., kg/2018 USD, purchaser price).</li>
  <li><strong>Supply Chain Emission Factors with Margins</strong>: The target variable for prediction.</li>
  <li><strong>DQ ReliabilityScore, TemporalCorrelation, GeographicalCorrelation, etc.</strong>: Quality metrics for the emission factors.</li>
</ul>

---

## <span style="font-family: Arial, sans-serif; color: #2E86C1;">Project Structure</span>
<ol style="font-family: Arial, sans-serif; font-size: 14px;">
  <li><strong>Data Loading</strong>: The dataset is loaded from an Excel file, with separate sheets for each year (2010–2016) and categories (Industry and Commodity).</li>
  <li><strong>Data Preprocessing</strong>:
    <ul>
      <li>Handling missing values (e.g., dropping the <code>Unnamed: 7</code> column, which is entirely null).</li>
      <li>Combining data from multiple years and categories into a single DataFrame.</li>
      <li>Encoding categorical features (e.g., <code>Substance</code>, <code>Unit</code>, <code>Source</code>).</li>
    </ul>
  </li>
  <li><strong>Model Building</strong>:
    <ul>
      <li>Regression models such as Linear Regression and Random Forest are trained to predict emission factors.</li>
      <li>Hyperparameter tuning is performed to optimize model performance.</li>
    </ul>
  </li>
  <li><strong>Evaluation</strong>:
    <ul>
      <li>Metrics like RMSE (Root Mean Squared Error), MAE (Mean Absolute Error), and R² Score are used to assess model accuracy.</li>
    </ul>
  </li>
</ol>

---

## <span style="font-family: Arial, sans-serif; color: #2E86C1;">Tools and Libraries</span>
<ul style="font-family: Arial, sans-serif; font-size: 14px;">
  <li><strong>Python</strong>: Primary programming language.</li>
  <li><strong>Pandas</strong>: For data manipulation and analysis.</li>
  <li><strong>Scikit-learn</strong>: For machine learning model implementation and evaluation.</li>
  <li><strong>Matplotlib/Seaborn</strong>: For data visualization.</li>
  <li><strong>Joblib</strong>: For saving and loading trained models.</li>
</ul>

---

## <span style="font-family: Arial, sans-serif; color: #2E86C1;">How to Use</span>
<ol style="font-family: Arial, sans-serif; font-size: 14px;">
  <li><strong>Install Dependencies</strong>: Ensure you have Python installed along with the required libraries (<code>pandas</code>, <code>scikit-learn</code>, <code>matplotlib</code>, <code>seaborn</code>, <code>joblib</code>).</li>
  <li><strong>Run the Notebook</strong>: Execute the Jupyter Notebook <code>GHG_Emissions_Prediction.ipynb</code> to preprocess the data, train the models, and evaluate their performance.</li>
  <li><strong>Customize</strong>: Modify the notebook to experiment with different models, features, or hyperparameters.</li>
</ol>

---

## <span style="font-family: Arial, sans-serif; color: #2E86C1;">Key Features</span>
<ul style="font-family: Arial, sans-serif; font-size: 14px;">
  <li><strong>Comprehensive Data Handling</strong>: Combines data from multiple years and categories into a unified format.</li>
  <li><strong>Quality Metrics Integration</strong>: Uses reliability and correlation scores to enhance prediction accuracy.</li>
  <li><strong>Scalable Modeling</strong>: Supports experimentation with various regression techniques.</li>
</ul>

---

## <span style="font-family: Arial, sans-serif; color: #2E86C1;">Future Work</span>
<ul style="font-family: Arial, sans-serif; font-size: 14px;">
  <li>Expand the dataset to include more recent years.</li>
  <li>Incorporate additional features such as economic indicators or geographic data.</li>
  <li>Explore deep learning models for potentially better performance.</li>
</ul>

---
