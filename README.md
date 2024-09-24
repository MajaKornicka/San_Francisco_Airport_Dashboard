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

From year 2005 and 2020 over 7,3 mln tons of cargo has been transported through San Francisco Airport. The average weight of cargo is 216,5 tons.


Over the years there have been 2 peaks where most of the cargo has been transported: in 2006 and 2019. The least amount of cargo has been transported in 2005 and 2020. In general from 2014 to 2019 there is increasing trend, which has been stopped by covid pandemic in 2020.


The majority of cargo is being transported internationally. Nearly 50/50 split between inbound and outbound cargo, approx. 1% more of outbound cargo.


Aircrafts used to transport cargo are combi, freighter and passenger, with the last one being the most popular.
United Airlines transport the majority of cargo, on the second place there is Korean Air Lines and on the third Alaska Airlines - all these airlines transport their cargo mostly in passenger aircrafts.
There are only few airlines using freighter aircrafts, the biggest among them are: Korean Air Lines, Asian Airlines, China Airlines and Eva Airways.
Combi aircrafts (combination of passenger and freighter aircraft) is used only by Eva Airways and Air China.


37% of all cargo is transported to or from Asia, 26% to/from USA and 17% to/from Europe. The least cargo is transported to and from Latin America (3%).







✈️ ✈️ ✈️





