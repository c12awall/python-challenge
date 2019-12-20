import pandas as pd 
import numpy as np
from babel.numbers import format_currency

# Path to collect data
budget_data_1_csv = "budget_data_1.csv"
budget_data_2_csv = "budget_data_2.csv"

# Create dataframe
budget_data_1_df = pd.read_csv(budget_data_1_csv, encoding = "ISO-8859-1")
budget_data_2_df = pd.read_csv(budget_data_2_csv, encoding = "ISO-8859-1")

# Merge the two data sources
budget_merge = pd.concat([budget_data_1_df, budget_data_2_df], ignore_index=True)
    
# total # of months in dataset
unique_months = len(budget_merge["Date"].unique())

# total revenue gained
total_revenue = budget_merge['Revenue'].sum()

# average monthly revenue
avg_revenue = total_revenue / unique_months

# greatest increase in revenue (date, amount)
greatest_revenue_increase = budget_merge['Revenue'].max()

# greatest decrease in revenue (date, amount)
greatest_revenue_decrease = budget_merge['Revenue'].min()


# Print Results
print("Financial Analysis")
print("------------------")
print("Total Months: " + str(unique_months))
print("Total Revenue: " + format_currency(total_revenue, 'USD', locale='en_US'))
print("Average Revenue: " + format_currency(avg_revenue,'USD', locale='en_US'))
print("Greatest Increase in Revenue: " + format_currency(greatest_revenue_increase,'USD', locale='en_US'))
print("Greatest Decrease in Revenue: " + format_currency(greatest_revenue_decrease,'USD', locale='en_US'))

