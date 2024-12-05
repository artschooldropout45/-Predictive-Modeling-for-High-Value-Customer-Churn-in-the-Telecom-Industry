# Predictive Modeling for High-Value Customer Churn in the Telecom Industry

## Problem Statement

In the highly competitive telecom industry, customer churn rates average between 15-25% annually. Retaining customers is significantly more cost-effective than acquiring new ones, making churn reduction a top priority for telecom firms. This project focuses on predicting churn among high-value customers using customer-level data from a leading telecom firm.

---

## Business Objective

The primary goal is to reduce churn by identifying high-risk customers and understanding the key indicators of churn. The insights will help companies take proactive measures, such as providing personalized offers or improving service quality.

---

## Understanding Churn

### Payment Models
- **Postpaid**: Customers pay after using services (e.g., monthly bills). Churn is clear when services are terminated.
- **Prepaid**: Customers pay upfront. Churn is harder to identify since customers may stop usage without notice.

### Definition of Churn
For this project, churn is defined using a **usage-based definition**, where a customer is considered churned if they:
- Have not made any outgoing or incoming calls.
- Have not used mobile internet services over a given period.

---

## High-Value Customers
In the Indian and Southeast Asian markets, the top 20% of customers contribute 80% of revenue. The project focuses on high-value customers defined as those whose recharge amounts are in the 70th percentile or higher during the "good" phase.

---

## Project Scope

### Data Description
The dataset contains customer information for four months:
1. **June** and **July** (Good Phase)
2. **August** (Action Phase)
3. **September** (Churn Phase)

### Business Objective
Predict churn in the fourth month (Churn Phase) using data from the first three months.

### Customer Lifecycle Phases
1. **Good Phase**: Normal behavior.
2. **Action Phase**: Behavioral changes due to dissatisfaction or competitor offers.
3. **Churn Phase**: Customers stop using services.

---

## Data Preparation Steps

1. **Derive New Features**:
   - Create meaningful indicators of churn based on customer behavior.

2. **Filter High-Value Customers**:
   - Define high-value customers as those with recharge amounts ≥ 70th percentile.

3. **Tag Churners**:
   - Define churn using metrics like:
     - `total_ic_mou_9` (Incoming calls)
     - `total_og_mou_9` (Outgoing calls)
     - `vol_2g_mb_9` (2G data usage)
     - `vol_3g_mb_9` (3G data usage)
   - Remove data from the Churn Phase after tagging.

---

## Modeling

1. **Predictive Model Goals**:
   - Identify customers likely to churn.
   - Determine key indicators of churn.

2. **Modeling Process**:
   - Preprocess data (handle missing values, convert formats).
   - Perform exploratory analysis to extract insights.
   - Use PCA for dimensionality reduction.
   - Train and evaluate classification models (e.g., Logistic Regression, Decision Trees).

3. **Handle Class Imbalance**:
   - Employ techniques like oversampling or cost-sensitive modeling to address low churn rates (5-10%).

4. **Evaluation Metrics**:
   - Focus on identifying churners accurately.

---

## Key Deliverables

1. **Churn Prediction Model**:
   - Predict high-value customer churn using features from the first three months.

2. **Key Predictors**:
   - Identify variables strongly correlated with churn (e.g., usage metrics).

3. **Visualizations**:
   - Present key insights through plots, summary tables, etc.

4. **Recommendations**:
   - Develop actionable strategies to reduce churn, such as personalized offers or service improvements.

---

## Tools and Techniques

- **Data Analysis**: Python, Pandas, NumPy, Matplotlib, Seaborn
- **Modeling**: Scikit-learn, Logistic Regression, Decision Trees, PCA
- **Class Imbalance Handling**: SMOTE, cost-sensitive learning

---

## Conclusion
By predicting churn among high-value customers, this project enables telecom companies to retain valuable clients and minimize revenue leakage. The insights derived from this analysis will help businesses implement targeted interventions to reduce churn effectively.

---

