# LITA_CUSTOMERDATA_PROJECT


[Project Overview for Customer Subscription Data](#project-overview-for-customer-subscription-data)

[Data Sources](#data-sources)

[Key Features for Customer Subscription Data](#key-features-for-customer-subscription-data)

[Technologies Used](#technologies-used)

[Data Cleaning and Preparations](#data-cleaning-and-preparations)

[Exploratory Data Analysis (EDA) for Customer Subscription Data](#exploratory-data-analysis-(eda)-for-sales-data-and-customer-subscription-data)

[Data Analysis](#data-analysis)

[Data Visualization for Customer Subscription Data](#data-visualization-for-customer-subscription-data)


[Results and Insights for Customer Subscription Data](#results-and-insights-for-customer-subscription-data)

[Recommendations for  Customer Subscription Data](#recommendations-for-customer-subscription-data)

---

### Project Overview for Customer Subscription Data

This project analyses customer data for an apparel and accessories brand to gain insights into customer behaviour, subscription trends, and revenue generation. This analysis will help inform marketing strategies, improve customer retention, and enhance product offerings.

---

### Data Sources
The primary source of data used here is Data Sale.CSV. It is open-source data that can be freely downloaded from an open source online such as Kaggle, FRED or any other data repository site. 

---

### Key Features for Customer Subscription Data

I. CustomerID: Unique identifier for each customer.

ii. CustomerName: Name of the customer.

iii. Region: Geographic region where the customer is located.

iv. SubscriptionType: Type of subscription the customer has (e.g., basic, premium).

v. SubscriptionStart: Date when the customer's subscription began.

vi. SubscriptionEnd: Date when the customer's subscription ended.

vii. Cancelled: Indicates whether the subscription has been cancelled (Yes/No).

viii. Revenue: Total revenue generated from the customer.

ix. Duration: Duration of the subscription in months.

x. Key Areas of Analysis.

---

### Technologies Used
- Microsoft Excel [Download here](https://www.microsoft.com)
  1. For Data Cleaning
  2. For Analysis
  3. For Data  Visualization
- SQL-  Structured Query Language
  1. For querying of data.
  2. For storing data.
  3. For managing data and,
  4. For manipulating data.
- POWER BI
  1.  For beautiful and interactive data visualizations.
  2.  For insightful data reports.
  3.  For retrieving data from different sources.
- Github
  1. For Portfolio Building.
  2. For collaboration and teamwork

  Therefore, this project aims to equip stakeholders of the brand with actionable insights to enhance sales strategies, boost customer retention, and streamline inventory management.
  
---

### Data Cleaning and Preparations

In the initial phase of the data cleaning and preparations, the following actions were performed on the different technologies used;

#### Excel
  1. Data loading and inspection
  2. Handling missing and null variables using ISBLANK function in Excel
  3. Eliminating duplicates.
  4. Data cleaning and formatting.

#### SQL
  1. The already cleaned data from Excel was converted to a CSV file format, which enabled the data to be imported into SQL quickly and efficiently as opposed to directly importing an Excel file format.
  2. Creation of a database.

      ```SQL
          CREATE DATABASE LITA_PROJECT
      ```

     The above code creates a database that houses all tables ready for querying.
     
  4. Import the SalesData and CustomerData data into the already created database.
  5. Writing amazing codes to show the different trends and patterns in the dataset for making sound decisions (screenshot of the codes).

#### POWER BI
  1. launched the power bi environment.
  2. Importation of both datasets using the TEXT/CSV file extension.
  3. Explored and cleaned the dataset.
  4. Confirmed the integrity of the datasets by using column quality, column distribution, and column profile options under the view tab.

---

### Exploratory Data Analysis (EDA) Customer Subscription Data 
EDA involves exploring the data to answer some questions about the data such as;
- What is the overall sales trend
- Which products are top sellers
- What are the products on peak sales?


  ![Alt text for image](https://github.com/Light63/LITA_CUSTOMERDATA_PROJECT/blob/main/EXCEL%20CUSTOMER%20DATA.JPG?raw=true)
  

  Figure 1: Shows the overall trend sales  for the customer subscription data using pivot tables and charts




  ![Alt text for image](https://github.com/Light63/DATA_ANALYSIS_JOURNEY-_WITH_LITA/blob/main/BI%201.JPG?raw=true)







  Figure 2: Shows the already prepared dataset ready for visualizations. This is particularly important as it enables effective analysis of the data to make valid and informed 
  decisions that will in turn, identify patterns, and sales trends, as well as boost productivity. Hence, increasing revenue and customer satisfaction.


---

  ### Data Analysis
  The images  and codes below show how data analysis was performed on the datasets using the above-mentioned tools.

  ```SQL
  SELECT * FROM TABLE 1
  WHERE CONDITION = TRUE
  ```

1. RETRIEVE THE TOTAL NUMBER OF CUSTOMERS FROM EACH REGION
```
SELECT region, COUNT (CustomerName) as Number_of_Customers
FROM [dbo].[CustomerData_Project]
group by Region
Order by Region
```

2. FIND THE MOST POPULAR SUBSCRIPTION TYPE BY THE NUMBER oF CUSTOMERS

```
select top 1(SubscriptionType),
COUNT (CustomerID) as TOTAL_CUSTOMERS
from [dbo].[CustomerData_Project]
group by SubscriptionType
order by TOTAL_CUSTOMERS desc
```

3. FIND CUSTOMERS WHO CANCELLED THEIR SUBSCRIPTION WITHIN 6 MONTHS

```
SELECT CustomerID, CustomerName, SubscriptionStart, SubscriptionEnd,canceled
from [dbo].[CustomerData_Project]
where canceled = 1
and datediff(month, subscriptionEnd, SubscriptionStart) <= 6
```

4. CALCULATE THE AVERAGE SUBSCRIPTION DURATION FOR ALL CUSTOMERS


```
select  AVG(DATEDIFF(day, SubscriptionStart, SubscriptionEnd)) 
as avg_subscription_duration
from [dbo].[CustomerData_Project]
```

5. FIND CUSTOMERS WITH SUBCRIPTIONS LONGER THAN 12 MONTHS

```
SELECT CustomerID, CustomerName, SubscriptionStart, SubscriptionEnd
from [dbo].[CustomerData_Project]
where datediff(month, subscriptionEnd, SubscriptionStart) > 12
```

6. CALCULATE TOTAL REVENUE BY SUBSCRIPTION TYPE

```
select SubscriptionType,  sum (revenue) as Total_Revenue
from [dbo].[CustomerData_Project]
group by Subscriptiontype
```

7. FIND THE TOP THREE REGIONS BY SUBSCRIPTION CANCELLATIONS

```
SELECT REGION, COUNT(CustomerID) As total_cancellations
from [dbo].[CustomerData_Project]
where canceled = 1
group by region
order by total_cancellations DESC
```

8. FIND THE TOTAL NUMBER OF ACTIVE AND CANCELLED SUBSCRIPTIONS

```
select sum (case when Canceled = 0 then 1 else 0 end) as activeSubsriptions,
sum(case when Canceled = 1 then 1 else 0 end) as CanceledSubscriptions
from [dbo].[CustomerData_Project]
```

---

###  Data Visualization for Customer Subscription Data


![ALT text for image](https://github.com/Light63/LITA_CUSTOMERDATA_PROJECT/blob/main/BI%20CUSTOMER%20VISUALS1.JPG?raw=true)


Figure 3: Shows the brand's customers' subscription trends. This gives insights into the most popular subscription type loved by the brand's customers and the number of active and cancelled  subscriptions. 

---

### Results and Insights for Customer Subscription Data

The total number of Subscriptions reflects 33,787, indicating a robust customer base engaging with the brand’s offerings. The total number of active and cancelled Subscriptions was 18,612 and 15,175, respectively. Therefore, the current active subscriptions represent a significant portion of the customer base, while cancelled subscriptions highlight a substantial churn rate that warrants further investigation.
Also, the basic subscription type emerges as the most popular among customers, suggesting that it meets the needs of a significant segment of the customer base.

---

### Recommendations  for Customer Subscription Data

Enhance the Basic Subscription Offering: Since the basic subscription is the most popular, it is important to consider enhancing its features or benefits to increase customer satisfaction and retention. This could include exclusive discounts, early access to new collections, or personalized recommendations.

Targeted Retention Strategies: It's crucial to analyze the reasons behind cancellations, with nearly half of the subscriptions being cancelled.  Proactive customer feedback mechanisms should be Implemented to identify pain points and address them promptly. Also, targeted re-engagement campaigns for those who have cancelled should be considered.

Segmented Marketing Efforts: Customer segmentation based on region and subscription type to tailor marketing messages should be utilized. Personalized campaigns can increase engagement and conversion rates, especially for those in the Basic subscription tier.

Data-Driven Decision Making: Customer data should be continuously analyzed to track trends over time. Regular monitoring of subscription metrics will enable the brand to make informed decisions about inventory, product offerings, and promotional strategies.

Loyalty Programs: Loyalty programs that reward long-term subscribers should be introduced, encouraging them to stay with the brand and reducing churn rates.

In summary, focusing on these strategies for the brand can enhance customer loyalty, improve subscription retention, and ultimately drive revenue growth.

