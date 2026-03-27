# 🛒 JV Market — A/B Test Analysis
An end-to-end data analysis project focused on hypothesis prioritization and A/B test evaluation for an e-commerce store, using ICE/RICE scoring frameworks and statistical testing.

## 📌 Overview
JV Market ran an A/B test to measure the impact of adding a subscription form to all main pages — the top-ranked hypothesis under the RICE framework. This project covers the full analysis pipeline: from data cleaning and exploratory analysis to statistical conclusions and business recommendations.
Test setup:

Group A (Control): Standard main pages without subscription form
Group B (Treatment): Main pages with subscription form added

## 🔍 What's Inside the Notebook
**1. Hypothesis Prioritization**
Nine business hypotheses were scored using two frameworks:

ICE — Impact, Confidence, Effort
RICE — Reach, Impact, Confidence, Effort

Both methods ranked "Add a subscription form to all the main pages" as the #1 priority, making it the natural candidate for the A/B test.

**2. A/B Test Analysis**
The notebook analyzes the test across several key metrics:

📈 Cumulative revenue per group over time
🛍️ Cumulative average order size per group
🔄 Daily and cumulative conversion rates
📊 Relative differences between groups for all metrics

**3. Statistical Testing**

Z-test (proportions) — to evaluate conversion rate differences
Mann-Whitney U test — to evaluate order size differences
Both tests were run with and without outliers for robustness

**4. Outlier Handling**
Cleaned using the 99th percentile as reference:

Removed users with more than 4 purchases
Removed transactions above $900 USD


## 📊 Key Results
MetricResultConversion rate (Z-test p-value)0.0116 — statistically significant ✅Order size (Mann-Whitney p-value)0.691 — no significant difference ❌Conversion rate after removing outliers0.0117 — result holds ✅Order size after removing outliers0.933 — confirms no difference ❌
Group B shows a significantly higher conversion rate than Group A, and this result is consistent before and after removing outliers.

## 🏁 Conclusions & Recommendations

The A/B test was successful: Group B's conversion rate is statistically higher.
Revenue increase in Group B was driven by atypical purchases (Aug 19), not a structural trend.
Most customers purchased only once — loyalty programs are needed.
Recommendation: Adopt Group B's strategy as the new standard and develop incentives to increase purchase frequency.


## 🛠️ Tech Stack
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=matplotlib&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-444876?style=for-the-badge&logo=seaborn&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![Statsmodels](https://img.shields.io/badge/Statsmodels-3B4D98?style=for-the-badge&logo=statsmodels&logoColor=white)


## ⚙️ Setup
bash# Clone the repo
git clone https://github.com/franciscojvazquezp/JV-Market.git
cd JV-Market

# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook "JV Market.ipynb"

👤 Author
franciscojvazquezp
