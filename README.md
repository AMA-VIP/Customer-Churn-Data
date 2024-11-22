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
- **Region by Retained Customer**: Visualization was done to know the region that churned the most.
- **Customer Status by Credit Card Ownership**: Visuals was done to know if having a credit card had anything to do with customer churning or not.

  


## 🔍KEY INSIGHT
- Count of Customer Status by Credit Card Ownership shows that high proportion of credit card owner are retained customera, which indicate that owning a credit card might contribute 
  positively to customer retention
- Out of the different age groups, customers of age 35-44 has the highest churned rate which is over 34.51%, which also as a slim difference between the next churned age group, age 45-54 
  (34.46%)
- **Geography** plays significant role. From three(3) different regions(Germany, France and Spain), Germany was seen to have the higest churned customer rate.
   **N/B**: Churned Customer from the age range of 35-54 terminated subscription frm Germany.
- From the visuals customer tend to leave within the 1st and the 9th month of subscription.
- filtering via credit card score also unfolded the following: Out of 2037 churned customer this was their credit score status
  
  "Excellent ➡️ 128 customers churned"
  "Good ➡️ 452 customer churned"
  "V.good ➡️ 252 customers chuened"
  "Fair ➡️ 685 customers churned"
  "Poor ➡️ 520 customers churned"
**N/B**: Since majority of the customers fall into the **Fair credit Score range** next to the **Poor credit score range** it could mean:

1. Higer Churn Risk:
   Customers with fair and poor credit scores might be less reliable, which could increase their likelihood of churning (leaving the 
   company)
2. Retention Challenges:
   Retaining customers with poor credit scores might require more effort because they could be less profitable
3. Low risk product or services specially designed for customers with poor credit score should be offered to avoide more retained 
   customwer from churning since we have ahve more number of active retained customers falling under this category 
  
## ✔️ Conclusion
This project provided insights into customer churn patterns, helping businesses understand which segments are more likely to leave and how they can improve retention strategies.

## 🪜 Future Improvement
I will be looking forward to incorporationg data:
- Additional customer data to improve accuracy
- Add more interactive PowerBI dashboards to highlight key insights 

## 🛑 Limitation: 
Limited to basic customer behaviour patterns 

## 🧰 Tools Used
- Excel: Data cleaning
- Power BI: Data visualization and analysis

## ⏫ References
- Data Source: [kaggle](https://www.kaggle.com/)


