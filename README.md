# PyBer_Analysis

## Project Overview
The CEO of a fictonal ride sharing company named PyBer asked for help to analyze their companies rider and driver data by city type. They hope to use the analysis and summary when making executive level decisions at the company. The three main tasks of the project were:

1. Create a ride-sharing summary DataFrame by city type with driver, rider, and fare metrics
2. Create a multiple line chart of total fare for each city type
3. Write a report for the analysis with recommendations on how to address any disparities among city types

## Resources
- Data Source: city_data.csv, ride_data.csv
- Software: Jupyter Notebooks 6.4.8
- Language: Python 3.7.13
- Packages: Pandas, Matplotlib.pyplot
- Output File: PyBer_fare_summary.png

##Analysis
### Import Data to Single DataFrame
The CEO provided complete rider and driver PyBer company data in two CSV files. My approach was to use Jupyter Notebooks to write Python script that read the ride and driver data into seperate Pandas dataframes. I then combined the two dataframes into a single set using Pandas .merge() function to make my analysis cleaner.
### Create a Summary DataFrame
Once I had my data in a single dataframe, I used the Pandas groupby() function with the count() and sum() methods to get the total number of rides, driver, and fares for each city type. I then referenced these values to calculate the average fare per ride and fare per driver by city type. These summary metrics were saved and formatted in a new clean dataframe to share with the CEO.
###Create a Multiple Line Plot
I created another new dataframe using the groupy() function and sum() method to return the total fare amount for each date in the dataset, then the pivot() function to set the index as the date. The final line plot should display the data by weeks, so I used the loc method to filter for the specified date range, then the resample() function to sum the fares by weeks instead of days. Using Matplotlib, I graphed the three city type's fares by week on the same chart using the object oriented method. Finally, I saved a PNG image of the multiple line chart to easily share my results.

## Results
Recc

1. 
2. 

##Summary
I believe the following recommendations address disparities among the city types: 
1. one
2. two
3. three
