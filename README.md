# Customer-Churn-Data

## 📊 Project Overview
This project focuses on aalysing customer churn data using a sample dataset of 10,000 customers. the analysis was conducted using PowerBI to gain insights into customer behaviour, retention rate and churn patterns. 

## 📑Table of content 
- Prpject Overview
- Data Description
- Data Cleaning & Preparation
- Data Analysis and Visualization
- Key Insights
- Future Work
- Conclusion
- How to Use

## 🪕Data Description 
The dataset contains information on customer demographies, account information, and whether the customer churned or not. Here's a brief description of the columns:
- CustomerID: Unique identifier for each customer
- Age: Age of the customer
- Tenure: Number of years the customer has been with the company
- CreditScore: CreditScore of the customer
- Geography: country of the customer
- HasCrCard: whether the customer has a credit card (Yes/No)
- EstimatedSalary: Customer annual salary 
- ChurnedCustomer: whether the customer churned (Yes/No)

## ⚒️ Data Cleaning & Preparation
Before conducting the analysis, the following steps where done on excel 
1. Removed duplicate and handled missing value
2. Each cell was formatted to its appropriate category
3. A new column was created to replace the "Exited" column with the detail (Yes/No) instead of 1 & 0
4. Row number column was removed because it was a duplicate of the row number found on excel spreadsheet
5. Active members was also changed to Yes/No instead of 1 and 0

## 📈 Data Analysis and Visualization
I use PowerBI to do futher analyse, created more measures and also created an interactive visualization to analyse the data. More measures and calculated column that was crated include:
- AgeGroup (calculated column)
  ```PowerBI
  AgeGroup = SWITCH(TRUE,()
  'CUSTOMER CHURN DATA' [Age]<=24, "18-24"
  
