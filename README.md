# SE20UARI056_Assign_7
In the given database consist of nine columns in which the last column (unit_sold) should be forecasted.After analysing the data we found out that there are no null values and no duplicates hence there is no requirement of cleaning the data.For the bases of understanding the graphs is plotted with 'week' on the X axis and 'units_sold' on Y axis.We have genearated a correlation matrix for understanding of relation between first eight columns and the targeted column(units_sold).We have dropped few columns like record_id,store_id etc because there values are close to zero as compared to +1 or -1 which indicated that they have lower correlation.For forcasting the given database we have initially tried the ARIMA model but it was giving negative values due to which we had to shift to exponential smoothing . In exponential smoothing we have tried the multiplicative model but the values were exponentially increasing which was not a reasonable solution . Later we used the combination of multiplicative and additive exponential smoothing we got reasonable values in decimal form which were then rounded off to closer integers.
## Paramters:
trend='add': This specifies that the trend component should be modeled as additive. An additive trend means that the trend component is linear, and the difference between 
two consecutive points remains roughly constant.
seasonal='mul': This specifies that the seasonality component should be modeled as multiplicative. A multiplicative seasonality means that the seasonal effect is
proportional to the current value of the series.
seasonal_periods=12: This parameter indicates the number of periods in one season. A value of 12 is commonly used for monthly data with yearly seasonality (because 
a year has 12 months). Adjust this value based on the frequency and seasonality of your data.
After forcasting the data, obtianed forecasted values have been appended into the given "submission format.csv" format
