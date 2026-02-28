# Telco Customer Churn Analysis

## 📌 Problem Statement
A telecom company is losing **26.5% of its customers** every month, resulting in **$1.67M in annual revenue loss**. This project analyzes customer data to identify churn drivers, build a predictive model, and provide actionable business recommendations.

---

## 📊 Dataset
- **Source:** [IBM Telco Customer Churn Dataset (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Size:** 7,043 customers, 21 features
- **Target Variable:** Churn (Yes/No)
- **Features:** Customer demographics, services subscribed, account information

---

## 🔍 Key Findings

| Feature | Finding |
|---|---|
| Contract Type | Month-to-month customers churn at 42.7% vs 2.8% for two year contracts |
| Payment Method | Electronic check customers churn at 45.3% vs ~16% for auto-pay |
| Internet Service | Fiber optic customers churn at 41.9% vs 19% for DSL |
| Online Security | Customers without security churn at 41.8% vs 14.6% with it |
| Tenure | Churners have average tenure of 18 months vs 38 for non-churners |

**Highest risk customer profile:** New customer, month-to-month contract, fiber optic internet, electronic check payment, no online security or tech support.

---

## 🤖 Models Built

| Model | Accuracy | ROC-AUC | Recall (Churners) |
|---|---|---|---|
| Logistic Regression | 0.822 | 0.862 | 0.60 |
| Logistic Regression (Balanced) | 0.752 | 0.862 | 0.84 |
| Decision Tree (Overfit) | 0.710 | 0.629 | 0.45 |
| Decision Tree (Balanced) | 0.745 | 0.836 | 0.79 |
| Random Forest | 0.793 | 0.864 | 0.77 |
| XGBoost | 0.755 | 0.863 | 0.84 |

**Winner: Balanced Logistic Regression**
- ROC-AUC: 0.862
- Recall: 0.84 — catches 84% of at-risk customers
- Most interpretable and deployable

---

## 💡 Business Recommendations

1. **Onboarding Program** — Focus retention on customers in first 12 months. Churners have average tenure of only 18 months.

2. **Incentivize Long Term Contracts** — Month-to-month churn is 15x higher than two year contracts. Offer discounts for annual sign-ups.

3. **Auto-Pay Campaign** — Electronic check customers churn 3x more than auto-pay users. Offer $5/month discount for switching.

4. **Fiber Optic Satisfaction** — Fiber optic churn (41.9%) is more than double DSL (19%). Investigate pricing and service quality.

5. **Bundle Security Services** — Customers without Online Security churn at 41.8% vs 14.6% with it. Offer free trials.

---

## 💰 Revenue Impact

| Metric | Value |
|---|---|
| Annual revenue at risk | $1,669,570 |
| Average monthly charge (churned customer) | $74.44 |
| Potential recovery (10% churn reduction) | $166,957 |
| Potential recovery (20% churn reduction) | $333,914 |
| Potential recovery (30% churn reduction) | $500,871 |

---

## 🛠️ Tech Stack
- **Python** — pandas, numpy
- **Visualization** — matplotlib, seaborn
- **Machine Learning** — scikit-learn, xgboost
- **Environment** — Jupyter Notebook, Anaconda

---

## 📁 Project Structure
```
telco-churn-analysis/
│
├── telco_churn_analysis.ipynb    # Main analysis notebook
├── WA_Fn-UseC_-Telco-Customer-Churn.csv  # Dataset
├── churn_distribution.png        # Churn overview chart
├── key_drivers.png               # Key churn drivers
├── numeric_distributions.png     # Tenure and charges analysis
├── correlation_heatmap.png       # Feature correlations
├── model_comparison.png          # Model performance comparison
├── feature_importance.png        # Feature importance comparison
└── README.md
```

---

## 🚀 How to Run

1. Clone the repository:
```bash
git clone https://github.com/ankitsw/telco-churn-analysis.git
```

2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost jupyter
```

3. Launch Jupyter:
```bash
jupyter notebook telco_churn_analysis.ipynb
```

4. Run all cells from top to bottom.

---

## 👤 Author
**Ankit** — Data Scientist  
[GitHub](https://github.com/ankitsw)