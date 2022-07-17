# PyBer_Analysis

## Project Overview
The CEO of a fictional ride sharing company named PyBer asked for help to analyze their companies rider and driver data by city type. They hope to use the analysis and summary when making executive level decisions at the company. The three main tasks of the project were:

1. Create a ride-sharing summary DataFrame by city type with driver, rider, and fare metrics
2. Create a multiple line chart of total fare for each city type
3. Write a report for the analysis with recommendations on how to address any disparities among city types

## Resources
- Data Source: city_data.csv, ride_data.csv
- Software: Jupyter Notebooks 6.4.8
- Language: Python 3.7.13
- Packages: Pandas, Matplotlib.pyplot
- Output File: PyBer_fare_summary.png

## Analysis
### Import Data to Single DataFrame
The CEO provided complete rider and driver PyBer company data in two CSV files. My approach was to use Jupyter Notebooks to write Python script that read the ride and driver data into separate Pandas dataframes. I then combined the two dataframes into a single set using Pandas .merge() function to make my analysis cleaner.
### Create a Summary DataFrame
Once I had my data in a single dataframe, I used the Pandas groupby() function with the count() and sum() methods to get the total number of rides, driver, and fares for each city type. I then referenced these values to calculate the average fare per ride and fare per driver by city type. These summary metrics were saved and formatted in a new clean dataframe to share with the CEO.
### Create a Multiple Line Plot
I created another new dataframe using the groupy() function and sum() method to return the total fare amount for each date in the dataset, then the pivot() function to set the index as the date. The final line plot should display the data by weeks, so I used the loc method to filter for the specified date range, then the resample() function to sum the fares by weeks instead of days. Using Matplotlib, I graphed the three city type's fares by week on the same chart using the object oriented method. Finally, I saved a PNG image of the multiple line chart to easily share my results.

## Results
### Summary Table:
![Summary Table](../main/analysis/PyBer_Summary_Df.png)
### Multiple Line Chart:
![Summary Graph](../main/analysis/PyBer_fare_summary.png)
### Conclusions:
1. Urban city types had the most rides when compared to rural and suburban types. This is likely due to the higher population of people without cars in cities, higher number of activities, and population density.
2. Rural city types had a significantly lower number of drivers than suburban or urban types. Since there were less rides taken in rural areas, there may not be a high enough demand to hire additional drivers in rural areas. 
3. The total fares for each city type fell in line with the same order ranking that the number of total rides and drivers did; from the least fares to the most fares was rural, suburban, and urban city types. 
4. The average fare per ride was calculated by dividing the total fares by total rides. The highest fare per ride was the rural city type. Taking a ride in a rural city type was over $10 more expensive on average than in a city. We did not analyze data on the ride distance, but rural rides may be longer, which could explain why they are more expensive on average. 
5. The average fare per driver was calculated by dividing the total fares by total drivers. This metric had an extremely significant difference between city types. Drivers in urban areas had an average fare of $16.57, while drivers in rural areas had an average fare of $55.49. Urban city types are the only type with more total drivers than total rides, so the average fare per driver is less than the average fare per ride. 
6. The multiple line graph plots the Total Fare by City Type by week from March to May. All city types saw Total Fares peak near the end of February, which could be due to higher priced rides or a higher quantity of rides taken. Suburban and Urban city types both fluctuated more in Total Fares during the period than Rural city types (~$450 difference between high and low).

## Summary
The following business recommendations address PyBer disparities among the city types: 
1. Urban city types have more total drivers than total rides, which means these areas are over-employed given the demand. You should stop hiring drivers in urban cities to ensure the employees are each given enough rides to make money.
2. Rural city types have the lowest proportion of drivers to total rides and have the highest average fare per driver. You could incentivize urban drivers to make trips in rural areas by advertising data on how much more money they could make by working in the rural areas or by offering incentives if they take a few rural trips each week. This would also address the over-saturation of drivers in urban areas. 
3. This report did not analyze the trip lengths. I would suggest using trip fare and trip length data to calculate the average cost per mile in each city type to determine if you could raise prices to be more profitable per trip in urban areas or if you could lower the cost per mile in rural cities to attract more customers. 
