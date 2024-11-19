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
I used PowerBI to do futher analyse, created more measures and also created an interactive visualization to analyse the data. More measures and calculated column that was crated include:
- AgeGroup (calculated column)
  ```PowerBI
  AgeGroup = SWITCH(TRUE()
  'CUSTOMER CHURN DATA' [Age]<=24, "18-24",
  'CUSTOMER CHURN DATA' [Age]<=34, "25-34",
  'CUSTOMER CHURN DATA' [Age]<=44, "35-44",
  'CUSTOMER CHURN DATA' [Age]<=54, "45-54",
  'CUSTOMER CHURN DATA' [Age]<=64, "55-64",
  "65+")
  ```
- Churned Customer was counted using the new measure
  ```PowerBI
  ChurnedCustomer = Calculate(COUNT (CUSTOMER CHURN DATA '[CustomerID]),
  'CUSTOMER CHURN DATA '[EXITED] = "Yes")
  ``` 
- Retained Customer was also counted using the new measure
  ```PowerBI
   RetainedCustomer = Calculate(COUNT (CUSTOMER CHURN DATA '[CustomerID]),
  'CUSTOMER CHURN DATA '[EXITED] = "No")
  ```
Interactive visualization was also done carried out using PowerBI, key charts include. 
- **Count of CustomerID**: To identify how many customer bought from the brand organization.
- **Number of Churned Customer**: To identify how many customer opted out of the company
- **Number off Retained Customer**: A visualization was also done to know the actual number of retaied customers
- **Retained Active/Inactive Customer**: from the data there was a column for active customer. So, it means most retained customer are not active. Visuals was carried out to know the 
  number of retained customers that are active and not active.
- **Count of Churned by Retained Customer**: This visual was needed to know the propotion of retained and churned customer.
- **Churned Customer by Tenure**: THis was use to understand the trend pattern of customer status. To understand what point they usually get churned.
- **Count of Churned by Age Group**: To know the age group that ismost likedly to get churned.
