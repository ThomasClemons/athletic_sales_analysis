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

**Step 1 in Notebook:**

<pre>import pandas as pd

# Create two dataframes from csv files
athletic_sales_2020_file = 'Resources/athletic_sales_2020.csv'
athletic_sales_2020_df = pd.read_csv(athletic_sales_2020_file)

athletic_sales_2021_file = 'Resources/athletic_sales_2021.csv'
athletic_sales_2021_df = pd.read_csv(athletic_sales_2021_file)

</pre>

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
- Renamed the aggregated column to reflect the aggregation of the data in the column.
- Sorted the results in descending order to show the top five regions, including the state and city that have the greatest number of products sold. 
- My final table for the Regions Sold the Most Products:

## put image here!!


| | | | **Total_Products_Sold** | 
| --: | --: | --: | --: |
| **region** | **state** | **city** | |
| **Northeast** | **New York** | **New York** | 111954 |
| **South** | **Texas** | **Houston** | 90322 |
| **West** | **California** | **San Francisco** | 85478 |
|  |  | **Los Angeles** | 76384 |
| **Southeast** | **Florida** | **Miami** | 73135 |

- The top five regions with their states and cities that have the greatest number of products sold.

**Step 3:  Determine which Region had the Most Sales**
- Used the groupby and pivot_table functions to create a multi-index DataFrame with the "region", "state", and "city" columns.
- Renamed the aggregated column to reflect the aggregation of the data in the column.
- Sorted the results in descending order to show the top five regions, including the state and city that generated the most sales.
- Your final table should look like the following image:

## put image here!!

- The top five regions with their states and cities that generated the most sales.

**Step 4:  Determine which Retailer had the Most Sales**
- Used the groupby and pivot_table functions to create a multi-index DataFrame with the "retailer", "region", "state", and "city" columns.
- Renamed the aggregated column to reflect the aggregation of the data in the column.
- Sorted the results in descending order to show the top five retailers along with their region, state, and city that generated the most sales.
- Your final table should look like the following image:

## put image here!!

- The top five retailers along with their region, state, and city that have the greatest average price for the products ordered.

**Step 5:  Determine which Retailer Sold the Most Women's Athletic Footwear**
- Filter the combined DataFrame to create a DataFrame with only women's athletic footwear sales data.
- Used the groupby and pivot_table functions to create a multi-index DataFrame with the "retailer", "region", "state", and "city" columns.
- Renamed the aggregated column to reflect the aggregation of the data in the column.
- Sorted the results in descending order to show the top five retailers along with their region, state, and city that sold the most women's athletic footwear.
- Your final table should look like the following image:

## put image here!!

- The top five retailers along with their region, state, and city that sold the most women's athletic footwear.

**Step 5:  Determine the Day with the Most Women's Athletic Footwear Sales**
- Created a pivot table with the "invoice_date" column as the index and the "total_sales" column as the values parameter.
- Renamed the aggregated column to reflect the aggregation of the data in the column.
- Applied the resample function to the pivot table, place the data into daily bins, and get the total sales for each day.
- Sorted the resampled DataFrame in descending order to show the top 10 days that generated the most women's athletic footwear sales.
- Your final table should look like the following image:

## put image here!!

- The top 10 days that generated the most women's athletic footwear sales.

**Step 6:  Determine the Week with the Most Women's Athletic Footwear Sales**
- Applied resample to the pivot table above, placeed the data into weekly bins, and got the total sales for each week.
- Sorted the resampled DataFrame in descending order to show the top 10 weeks that generated the most women's athletic footwear sales.
- Your final table should look like the following image:

- The top 10 weeks that generated the most women's athletic footwear sales.

## Help

- Please execute all steps in the notebook.  The results of above steps are used in subsequent steps. 


## Authors

- Author:  Tom Clemons

## Version History

- 0.1
    - Initial Release

## Acknowledgments

- None