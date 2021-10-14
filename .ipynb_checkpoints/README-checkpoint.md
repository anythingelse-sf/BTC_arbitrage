# BTC_Arbitrage

## Approach
1) Collecting the data.
2) Preparing the data.
3) Analyzing the data.
4) Publish an analysis report.

# Collect the Data, Steps:
1) Pull the CSV files into Data Frames
2) Set the index column and and to_datetime

# Prepare the Data, Steps:
1) Scan the data for missing or NaN values
2) Remove the dollar sign from the string
3) Convert any columns to 'float' dtypes

# Begin to analayze the data, Steps:
1) Get the summary statistics using the describe function to begin your search
2) Use iloc or loc to grab the index and which column to analyze
3) Plot the data using a line plot, transposing each exchange on top of each other

# Narrow your analysis to specific dates, Steps:
1) Select a date
2) Generate the summary statistics
3) Create a box plot to compare the data from a high level

# Calculate the arbitrage profits
1) Measure the arbitrage spread between the two exchanges
    a) Subtract the prices of ohigher priced exchange by the lower priced exchange
2) Measure the spread retun
    a) the amount of spread divided by the price on the lower priced exchange
3) Find profitable trades by deleting all instances where the spread return is less than 1%
    b) use a conditional statement to filer spread_returns > 0.01
4) Calculate the potential profit in dollars per trade
    a) multiply the spread returns greater tha 1% by the cost of what was purchased
5) Calculate the potential arbitrage profits you can make on each day
    b) Sum the elements in your profit_per_trade DataFrame
    
# Analysis Report
1) Calculate the arbitrage profits across random days
    a) Are there any patterns or trends in the profits?
