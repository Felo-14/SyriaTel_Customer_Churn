# SyriaTel Customer Churn

## Overview
Customer churn is a critical issue for SyriaTel, directly affecting profitability and long-term business sustainability. This project aims to develop a machine learning-based churn prediction model to identify customers who are likely to leave. Therefore, through the analysis of historical customer data and predictive analysis, retention strategies can be applied to encourage customers to stay, thereby reducing churn rates and improving customer loyalty.

## Business Understanding
SyriaTel aims to improve customer retention by proactively identifying customers likely to churn. Churn (whether a customer will leave the service) is a significant problem that has an immediate impact on profitability and sustainability. Retaining existing customers is more cost-effective than acquiring new ones, making churn prediction an essential business goal.

### Metrics of Success
The projects' success can be measured by:

1. Model Performance.
Conducting and analyzing accuracy, precision, recall, F1-score, or ROC-AUC for churn prediction.

2. Business Impact.
Reducing churn rate over a defined period.

3. Actionable Insights.
Identifying factors that influence churn, leading to targeted business interventions.

  
## Data Understanding
The data used for analysis is from:
    
**SyriaTel Customer Churn**: SyriaTel is a telecommunication company based in Syria, whose dataset contains 20 features and 3,333 rows.

## Tech Stack
- Python
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Scikit-Learn

## EDA

![Distribution of Customer Churn](/images/Customer%20Churn%20Distribution.png)

The chart shows a significantly larger number of customers classified as `non-churners` (false), compared to `churners` (true).

![Churn Distribution by International Plan](/images/Churn%20Distribution%20by%20International%20Plan.png)

Majority of customers do not have an international plan and within that group, the churn rate is significantly lower compared to the group with an international plan, which exhibits a higher proportion of churned customers relative to non-churned customers.


## Feature Engineering
Features used are shown below:

- Total_Minutes
- Total_Calls
- Total_Charges
- Charges_Per_Minute
- Calls_Per_Minute

## Modeling - Random Forest

The Random Forest algorithm performed best with an accuracy of ~96%

![Confusion Matrix - Random Forest](/images/Confusion%20Matrix%20-%20Random%20Forest.png)
![Final Classification Report](/images/Classification%20Report.png)

![ROC Curve](/images/ROC%20Curve.png)

An AUC of 0.90 suggests strong predictive power

## Feature Selection

The most important features were Total_Charges and Customer_Service_Calls.

![Top 10 Most Important Features For Churn Prediction](/images/Top%2010%20Most%20Important%20Features%20for%20Churn%20Prediction.png).


## Conclusions

- SyriaTel should implement the optimized Random Forest model with threshold adjustment, as it balances recall and precision effectively.

- The company should target high-risk customers (e.g., those with high charges and frequent customer service interactions) with personalized offers and better customer support.

- SyriaTel should improve customer service quality to reduce dissatisfaction and churn risk.

- The company should offer incentives to customers on the International Plan to increase retention.

- Further improvements can be made by exploring alternative models such as XGBoost.