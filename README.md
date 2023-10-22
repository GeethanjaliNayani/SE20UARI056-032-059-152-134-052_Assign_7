# SE20UARI056_Assign_7
The trainig data consisted of record_ID, week,	store_id,	sku_id,	total_price,	base_price,	is_featured_sku,	is_display_sku,	units_sold attributed. 
Here the target column is units_sold and supposed to forecast the data for upcoming period of time. The data consisted of no null values nor the duplicates. 
COnstructed a correlation matrix which is used to check the dependencies of columns on each other. Ligher colors indicate weak correlation and vibrant colors indicate strong correlation.
Values close to +1 and -1 are considered to have higher correalation. whereas values that are close to 0 have weak correlation and can be dropped.
Have tried using different models like Holt winter, ARIMA models but the results are not as expected hence, I have built the model based on the Exponential smoothing.
## Paramters:
trend='add': This specifies that the trend component should be modeled as additive. An additive trend means that the trend component is linear, and the difference between 
two consecutive points remains roughly constant.
seasonal='mul': This specifies that the seasonality component should be modeled as multiplicative. A multiplicative seasonality means that the seasonal effect is
proportional to the current value of the series.
seasonal_periods=12: This parameter indicates the number of periods in one season. A value of 12 is commonly used for monthly data with yearly seasonality (because 
a year has 12 months). Adjust this value based on the frequency and seasonality of your data.
After forcasting the data, obtianed forecasted values have been appended into the given "submission format.csv" format
