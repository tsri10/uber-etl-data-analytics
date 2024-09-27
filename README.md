## Uber Data Pipeline with Modern Data Engineering Stack

This project demonstrates the creation of an ETL (Extract, Transform, Load) pipeline using an Uber-like dataset. The pipeline is developed using Mage, an open-source modern data pipeline tool, deployed on Google Cloud Compute Engine. The data transformation is performed in Python, and the final data is loaded into Google BigQuery for analytics. A Looker Studio dashboard is created to visualize the insights.

### Project Architecture

This is the architecture overview of the pipeline. It shows how the raw data flows through the ETL pipeline, eventually leading to the dashboarding layer.

Components:

1.	Data Source (Google Cloud Storage): Stores the raw data.
   
2.	Mage VM (Google Compute Engine): Hosts the Mage data pipeline tool where the transformation logic is written and executed.
   
3.	BigQuery: A cloud-based data warehouse used for analytics.
   
4.	Looker Studio: BI tool used for creating dashboards and visualizing data.

### Data Model

We follow the dimensional modeling approach with fact and dimension tables. The fact table contains the trip-related metrics, while dimension tables capture descriptive attributes like date, location, passenger count, etc.

### Project Features

1.	ETL Process:
   
    o	Extract: The data is extracted from Google Cloud Storage (GCS) in CSV format.
  	
    o	Transform: Python is used to transform raw data into a structured format, dividing it into fact and dimension tables. See the transform.py for the transformation logic.
  	
    o	Load: Transformed data is loaded into Google BigQuery for storage and analytics.
  	
2.	Dimensional Modeling:

    o	The data is structured into a star schema with a central fact table and multiple dimension tables (e.g., trip distance, rate code, passenger count, payment type).
  	
3.	Dashboard: The insights from the data are visualized using Looker Studio, including key metrics like total revenue, average fare, trip distance, and more.

### Business Insights

This pipeline allows Uber or any ride-sharing company to gain valuable insights into their operations. Here are some key business insights that can be derived from the data:

1.	Top Pickup Locations: Identifying the most frequent pickup locations can help Uber deploy resources more efficiently, ensuring a higher supply of drivers in high-demand areas.
   
2.	Revenue by Vendor: By tracking which vendor is generating the most revenue, the company can adjust strategies to reward high-performing vendors or provide support where needed.
   
3.	Customer Tipping Behavior: Analyzing the tipping behavior based on payment type (e.g., credit card vs cash) can inform decisions around payment system improvements or marketing incentives for drivers.

4.	Passenger Count Analysis:	Understanding the distribution of passenger counts in vehicles can help Uber optimize vehicle types for different regions or times of day.
   
5.	Trip Duration and Fare Trends: Tracking the average trip fare and distance per trip over time can help Uber understand pricing strategies and customer demand patterns.
    
6.	Impact of Payment Methods: Insight into the distribution of payment methods (cash, card, etc.) can help Uber identify customer preferences and push digital payments more effectively in regions where cash is dominant.

### Key Insights to Explore

Here are a few analysis questions that can be answered using the data:

   •	What are the top 10 most popular pickup locations?
  
   •	Which vendor generated the highest revenue?
  
   •	How does the payment method affect tip amounts?
  
   •	What is the average trip distance by hour of the day?

