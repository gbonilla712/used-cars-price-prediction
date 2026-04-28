# 🚗 Used Cars Price Prediction

This capstone project was completed as part of the **MIT Applied AI & Data Science Program**. 

---

## 📋 Project Overview

The Indian used-car market surpasses the new-car market in volume, with approximately 4 million second-hand cars traded annually compared to 3.6 million new units. Despite this scale, pricing remains inconsistent, opaque, and driven by information asymmetry between buyers and sellers.
This capstone project develops a **machine-learning pricing engine** for **Cars4U**, a used-car startup entering the Indian market. The model predicts fair market values for used cars based on vehicle attributes such as brand, power, age, mileage, and condition — enabling data-driven pricing, reducing negotiation disputes, and building buyer-seller trust.
A dataset of **7,253 used cars** with **14 features** was analyzed through comprehensive exploratory data analysis, feature engineering, and preprocessing. Six regression models were trained and evaluated, with **Random Forest Regression** selected as the final production model, achieving an **R² of 0.90** on unseen test data.

---

## 🎯 Key Objectives

- Develop a reliable, data-driven pricing model that accurately estimates the market value of any used car in Cars4U's inventory
- Identify the most influential features driving used-car prices in the Indian market
- Evaluate and compare multiple regression techniques to determine the optimal modeling approach
- Deliver actionable business recommendations for pricing strategy, inventory optimization, and fraud detection
- Enable price standardization across Indian cities to reduce regional pricing disparities

---

## 🔍 Highlights & Findings

**Data & Feature Engineering**
- Analyzed **7,253 used cars** across **11 Indian cities** with **6 categorical** and **8 numerical** variables
- Engineered high-impact features: **Car_Age**, **Depreciation_Amount**, and **Brand** extraction from vehicle names
- Applied log transformations to Price and Kilometers_Driven to stabilize right-skewed distributions
- Implemented hierarchical imputation strategies for missing values (6,247 missing in New_Price alone)
- Retained all outliers as meaningful luxury-segment market signals rather than removing them

**Modeling & Performance**
- Trained and evaluated **6 regression models**: Multiple Linear Regression, Ridge, Lasso, Decision Tree, Random Forest, and KNN
- **Random Forest Regression** achieved the strongest performance across all metrics:

| Metric | Train | Test |
|--------|-------|------|
| R² | 0.97 | 0.90 |
| RMSE | 2.07 | 3.59 |
| MAE | 0.79 | 0.88 |
| MAPE | 0.09 | 0.09 |

- Identical MAPE (0.09) on train and test sets demonstrates exceptional generalization stability
- Tree-based models significantly outperformed linear models due to their ability to capture nonlinear relationships

**Top Predictors (by Feature Importance)**
1. Power (BHP)
2. Depreciation Amount
3. New Price
4. Year
5. Car Age
6. Kilometers Driven (log)

---

## 💡 Recommendations

- **Improve Data Quality** — Standardize data-collection procedures, mandate required fields, validate entries at ingestion, and implement automated irregularity detection
- **Operational Integration** — Integrate model-predicted prices into seller listings, buyer-facing displays, and procurement decisions to enable real-time, data-driven pricing
- **Periodic Model Retraining** — Adopt a scheduled retraining pipeline with continuous data enrichment, model drift monitoring, and performance tracking through a feedback loop
- **Strategic Applications** — Leverage depreciation patterns and brand-specific value retention for inventory mix optimization, regional marketing, and anomalous pricing detection for fraud prevention
- **Transparent Communication** — Provide buyers and sellers with clear explanations of key pricing factors, visual breakdowns, and confidence ranges to build platform trust

---

## 📁 Project Structure

```
used-cars-price-prediction/
│
├── README.md
│
├── GBonilla_Used_Cars_Price_Prediction_Capstone_EDA_Low_Code.ipynb
├── GBonilla_Used_Cars_Price_Prediction_Capstone_Preprocessing_Modeling_Low_Code.ipynb
│
├── GBonilla_Used_Cars_Price_Prediction_Capstone_Low_Code_Final_Presentation.pdf
├── GBonilla_Used_Cars_Price_Prediction_Capstone_Low_Code_Final_Submission_Report.pdf
├── GBonilla_Used_Cars_Price_Prediction_Capstone_Low_Code_Methodology_and_Workflow.pdf
└── GBonilla_Used_Cars_Price Prediction_Capstone_Low_Code_Milestone_Report.pdf
```

| File | Description |
|------|-------------|
| `...Capstone_EDA_Low_Code.ipynb` | Exploratory data analysis notebook covering data exploration, univariate/bivariate analysis, and correlation analysis |
| `...Capstone_Preprocessing_Modeling_Low_Code.ipynb` | Feature engineering, data preprocessing, model building, evaluation, and final model selection |
| `...Final_Presentation.pdf` | Capstone project presentation slides |
| `...Final_Submission_Report.pdf` | Final submission report with executive summary, recommendations, and appendix |
| `...Methodology_and_Workflow.pdf` | Comprehensive methodology document detailing the end-to-end project workflow |
| `...Milestone_Report.pdf` | Full milestone report covering all phases from problem definition through conclusions |

---

## 🛠️ Tools & Technologies

- **Language:** Python
- **Environment:** Google Colab Notebook
- **Libraries:** pandas, NumPy, Matplotlib, Seaborn, scikit-learn, statsmodels, SciPy
- **Techniques:** Multiple Linear Regression, Ridge Regression, Lasso Regression, Decision Tree Regression, Random Forest Regression, KNN Regression
- **Methods:** Feature Engineering, Log Transformation, Hierarchical Imputation, One-Hot Encoding, VIF Analysis, Hyperparameter Tuning (RandomizedSearchCV), Train-Test Split (70/30)

---

## 📄 Project Report

## Milestone Report 

The milestone report (`GBonilla Used Cars Price Prediction Capstone Low Code Milestone Report.pdf`) provides the full analytical narrative across all project phases:
- Executive Summary
- Business Problem Overview and Solution Approach
- Problem Definition
- Data Exploration
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Data Preprocessing
- Building Models
- Models/Techniques Comparison
- Final Solution Design
- Conclusions and Recommendations

### Final Submission Report

The final submission report (`GBonilla Used Cars Price Prediction Capstone Low Code Final Submission Report.pdf`) delivers a consolidated, decision-ready summary:
- Executive Summary
- Problem and Solution Summary
- Recommendations for Implementation
- Appendix
