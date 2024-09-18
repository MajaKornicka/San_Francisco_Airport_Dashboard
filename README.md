# ✈️ San Francisco Airport Dashboard

### Project Overview
This data projects aims to provide insights into the San Francisco Airport, specifically Cargo.


### Data Source

Data for this analysis has been taken from Kaggle 

https://www.kaggle.com/datasets/rajsengo/sfo-air-traffic-passenger-and-cargo-statistics?select=Air_Traffic_Passenger_Statistics.csv


### Tools

- SQL Server - Data Cleaning and Analysis
- PowerBI - Data Analysis, Creating Dashboard


### Data Cleaning/Preparation

The dataset was quite clean, so I checked for missing values and adjusted date to the correct format.

```sql

SELECT *, LEFT(activity_period, 4)  AS activity_year, 
         RIGHT(activity_period, 2) AS activity_month,
         CONCAT( '01.', RIGHT(activity_period, 2), '.', LEFT(activity_period, 4)) AS activity_date
FROM Air_Traffic_Cargo_Statistics

```

### Data Analysis

The data has been analyzed based on following questions:

1. What is cargo distribution over the years?
2. Which airlines transport the most of cargo and in which aircrafts?
3. What is the region distribution?
4. What types of cargo prevail for specific years?


### Results
