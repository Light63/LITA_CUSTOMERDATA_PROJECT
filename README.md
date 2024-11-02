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

Dataset Description:
The dataset includes the following columns:


Expected Outcomes:

Comprehensive insights into customer demographics and behaviours.
Data-driven recommendations for marketing strategies and customer engagement.
Identification of trends that can inform product development and inventory management.
This analysis will empower the brand to enhance its customer experience and optimize its offerings to meet customer needs effectively.

---

### Data Sources
The primary source of data used here is Data Sale.CSV. It is open-source data that can be freely downloaded from an open source online such as Kaggle or FRED or any other data repository site. 

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

ix. DURATION: Duration of the subscription in months.

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
  4. Confirmed the integrity of the datasets by using column quality, column distribution, and column profile options under the view tab(screenshot of this).

---

### Exploratory Data Analysis (EDA) Customer Subscription Data 
EDA involves exploring the data to answer some questions about the data such as;
- What is the overall sales trend
- Which products are top sellers
- What are the products on peak sales? (pivot tables and charts for both datasets here)


  ![Alt text for image](https://github.com/Light63/DATA_ANALYSIS_JOURNEY-_WITH_LITA/blob/main/EXCEL%20CUSTOMER%20DATA.JPG?raw=true)


  Figure 1: Shows the overall trend sales  for the customer subscription data using pivot tables and charts




  ![Alt text for image](https://github.com/Light63/DATA_ANALYSIS_JOURNEY-_WITH_LITA/blob/main/BI%201.JPG?raw=true)







  Figure 2: Shows the already prepared dataset ready for visualizations. this is particularly important as it enables effective analysis of the data to make valid and informed 
  decisions that will in turn, identify patterns, and sales trends, as well as boost productivity. Hence, increasing revenue and customer satisfaction.


---

  ### Data Analysis
  the images  and codes below show how data analysis was performed on the datasets using the above-mentioned tools.

  ```SQL
  SELECT * FROM TABLE 1
  WHERE CONDITION = TRUE
  ```

---

###  Data Visualization for Customer Subscription Data


![ALT text for image](https://github.com/Light63/DATA_ANALYSIS_JOURNEY-_WITH_LITA/blob/main/BI%20CUSTOMER%20VISUALS1.JPG?raw=true)



Figure 3: Shows the subscription trends of the customers in the brand. This gives insights on the most popular subscription type loved by the brand's customers, and the number of active and cancelled  subscriptions. 

---

### Results and Insights for Customer Subscription Data

The total count of Subscriptions reflects a total of 33,787 subscriptions, indicating a robust customer base engaging with the brand’s offerings. The total Active and cancelled Subscriptions are 18,612 and 15,175 respectively. therefore,  the current active subscriptions represent a significant portion of the customer base while cancelled subscriptions highlight a substantial churn rate that warrants further investigation.
Also, the Basic subscription type emerges as the most popular among customers, suggesting that it meets the needs of a significant segment of the customer base.

---

### Recommendations  for Customer Subscription Data

Enhance the Basic Subscription Offering: Since the Basic subscription is the most popular, consider enhancing its features or benefits to increase customer satisfaction and retention. This could include exclusive discounts, early access to new collections, or personalized recommendations.

Targeted Retention Strategies: It's crucial to analyze the reasons behind cancellations, with nearly half of the subscriptions being cancelled.  Proactive customer feedback mechanisms should be Implemented to identify pain points and address them promptly. Also, targeted re-engagement campaigns for those who have cancelled should be Considered.

Segmented Marketing Efforts: Utilize customer segmentation based on region and subscription type to tailor marketing messages. Personalized campaigns can increase engagement and conversion rates, especially for those in the Basic subscription tier.

Data-Driven Decision Making: Continuously analyze customer data to track trends over time. Regular monitoring of subscription metrics will enable the brand to make informed decisions about inventory, product offerings, and promotional strategies.

Loyalty Programs: Introduce loyalty programs that reward long-term subscribers, encouraging them to stay with the brand and reducing churn rates.

By focusing on these strategies, the brand can enhance customer loyalty, improve subscription retention, and ultimately drive revenue growth.

