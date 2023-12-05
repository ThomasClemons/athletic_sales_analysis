# athletic_sales_analysis
Assignment for AI/ML Bootcamp Module 5 Challenge

Our assignment was to analyze sales data using Pandas methods to answer a series of questions.

---------------------------------------------------------------------

## Description

This is a class assignment to analyze sales data to gain insights into which cities in the U.S. have sold the most athletic wear over two years. Next, I'll determine which retailers had the greatest total sales for athletic wear, and which retailers sold the most women's athletic footwear. Finally, I'll determine which day and week had the highest sales for women's athletic footwear..

## Getting Started

### Dependencies

- Python 3.10
- Jupyter Notebooks

### Installing

- Clone this repo to your environment

### Executing program

- Open '**athletic_sales_analysis_starter_code.ipynb**' from your cloned repo folder in Jupyter Notebooks
- Step through the completed notebook to see my analysis by clicking the "Run" button.
- The results are displayed after each step.

**Step 1:  Combine and Clean the Data**
- Imported two CSV files, athletic_sales_2020.csv and athletic_sales_2021.csv, and read them into DataFrames.
- Checked that the columns in the two DataFrames have similar names and data types.
- Combined the two DataFrames by the rows using concatenate, and reset the index.

- After combining the DataFrames, I did the following:
    - Checked if there are any null values.
    - Checked each column’s data type.
    - Converted the "invoice_date" column to a datetime data type.
    - Confirmed that the data type has been changed.

**Step 2:  Determine which Region Sold the Most Products**
- Used the groupby and pivot_table functions to create a multi-index DataFrame with the "region", "state", and "city" columns.
- Renamed the aggregated column to "Total_Products_Sold" to reflect the aggregation of the data in the column.
- Sorted the results in descending order to show the top five regions, including the state and city that have the greatest number of products sold. 
- My final table for the top five regions with their states and cities that have the greatest number of products sold:

| | | | **Total_Products_Sold** | 
| --: | --: | --: | --: |
| **region** | **state** | **city** | |
| **Northeast** | **New York** | **New York** | 111954 |
| **South** | **Texas** | **Houston** | 90322 |
| **West** | **California** | **San Francisco** | 85478 |
|  |  | **Los Angeles** | 76384 |
| **Southeast** | **Florida** | **Miami** | 73135 |


**Step 3:  Determine which Region had the Most Sales**
- Used the groupby and pivot_table functions to create a multi-index DataFrame with the "region", "state", and "city" columns.
- Renamed the aggregated column to "Total_Sales" to reflect the aggregation of the data in the column.
- Sorted the results in descending order to show the top five regions, including the state and city that generated the most sales.
- My final table for the top five regions with their states and cities that generated the most sales:

| | | | **Total_Sales** | 
| --: | --: | --: | --: |
| **region** | **state** | **city** | |
| **Northeast** | **New York** | **New York** | 39801235 |
| **West** | **California** | **San Francisco** | 33973228 |
| **Southeast** | **Florida** | **Miami** | 31600863 |
| | **South Carolina** | **Charleston** | 29285637 |
| | **Florida** | **Orlando** | 27682851 |


**Step 4:  Determine which Retailer had the Most Sales**
- Used the groupby and pivot_table functions to create a multi-index DataFrame with the "retailer", "region", "state", and "city" columns.
- Renamed the aggregated column to "Total_Sales" to reflect the aggregation of the data in the column.
- Sorted the results in descending order to show the top five retailers along with their region, state, and city that generated the most sales.
- My final table for the top five retailers along with their region, state, and city that have the greatest average price for the products ordered:

| | | | | **Total_Sales** | 
| --: | --: | --: | --: | --: |
| **retailer** |**region** | **state** | **city** | |
| **West Gear** | **West** | **California** | **San Francisco** | 32794405 |
| **Kohl's** | **West** | **California** | **Los Angeles** | 25127160 |
| **Foot Locker** | **Northeast** | **New York** | **New York** | 825008568 |
| **West Gear** | **West** | **Washington** | **Seattle** | 24862675 |
| **Foot Locker** | **Southeast** | **South Carolina** | **Charleston** | 24822280 |


**Step 5:  Determine which Retailer Sold the Most Women's Athletic Footwear**
- Filtered the combined DataFrame to create a DataFrame with only women's athletic footwear sales data.
- Used the groupby and pivot_table functions to create a multi-index DataFrame with the "retailer", "region", "state", and "city" columns.
- Renamed the aggregated column to "Womens_Footwear_Units_Sold" to reflect the aggregation of the data in the column.
- Sorted the results in descending order to show the top five retailers along with their region, state, and city that sold the most women's athletic footwear.
- My final table for the top five retailers along with their region, state, and city that sold the most women's athletic footwear:

| | | | | **Womens_Footwear_Units_Sold** | 
| --: | --: | --: | --: | --: |
| **retailer** |**region** | **state** | **city** | |
| **West Gear** | **West** | **California** | **San Francisco** | 12107 |
| **Foot Locker** | **Northeast** | **New York** | **New York** | 10996 |
| **Kohl's** | **West** | **California** | **Los Angeles** | 10826 |
| **Foot Locker** | **Southeast** | **South Carolina** | **Charleston** | 8814 |
| **Sports Direct** | **South** | **Texas** | **Dallas** | 8790 |


**Step 5:  Determine the Day with the Most Women's Athletic Footwear Sales**
- Created a pivot table with the "invoice_date" column as the index and the "total_sales" column as the values parameter.
- Renamed the aggregated column to "Total Sales" to reflect the aggregation of the data in the column.
- Applied the resample function to the pivot table, place the data into daily bins, and get the total sales for each day.
- Sorted the resampled DataFrame in descending order to show the top 10 days that generated the most women's athletic footwear sales.
- My final table for the top 10 days that generated the most women's athletic footwear sales:

| | **Total Sales** | 
| --: | --: |
| **invoice_date** | |
| **2021-07-16** | 1521825 |
| **2021-12-16** | 1473497 |
| **2021-06-17** | 1376988 |
| **2021-08-17** | 1086294 |
| **2021-07-23** | 1021806 |
| **2021-11-17** | 1021145 |
| **2021-12-09** | 915011 |
| **2021-06-24** | 884238 |
| **2021-07-09** | 869054 |
| **2021-08-10** | 839120 |


**Step 6:  Determine the Week with the Most Women's Athletic Footwear Sales**
- Applied resample to the pivot table above, placed the data into weekly bins, and got the total sales for each week.
- Sorted the resampled DataFrame in descending order to show the top 10 weeks that generated the most women's athletic footwear sales.
- My final table for the top 10 weeks that generated the most women's athletic footwear sales:

| | **Total Sales** | 
| --: | --: |
| **invoice_date** | |
| **2021-12-19** | 3098970 |
| **2021-12-12** | 2922161 |
| **2021-07-11** | 2835078 |
| **2021-07-18** | 2801449 |
| **2021-11-14** | 2531721 |
| **2021-08-22** | 2491259 |
| **2021-08-15** | 2463941 |
| **2021-11-21** | 2449537 |
| **2021-05-16** | 2422132 |
| **2021-06-13** | 2358602 |


## Help

- Please execute all steps in the notebook.  The results of above steps are used in subsequent steps. 


## Authors

- Author:  Tom Clemons

## Version History

- 0.1
    - Initial Release

## Acknowledgments

- None