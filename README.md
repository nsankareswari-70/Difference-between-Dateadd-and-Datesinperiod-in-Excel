#### Difference-between-Dateadd-and-Datesinperiod-in-Excel
###### In DAX, DATEADD shifts a single date by a specified interval (e.g., 7 days prior), returning a single new date, whereas DATESINPERIOD returns a table (or range) of dates within a dynamic or rolling period (e.g., the last 7 days) relative to a starting date. Use DATEADD for point-in-time comparisons, like year-over-year sales, and DATESINPERIOD for rolling metrics, such as a trailing 3-month sales trend.  
#### DATEADD  
###### What it does: Adds or subtracts a specified number of intervals (days, months, years, etc.) to a given date, producing a single new date.     
Use Case: Benchmarking and point-in-time comparisons, such as finding the sales amount for exactly 7 days ago or the same date last year.       
Returns: A single date.     
Example: DATEADD('Date'[Date], -7, DAY) returns the date that is 7 days before the current date.     
#### DATESINPERIOD    
###### Purpose: To generate a table of a dynamic date range, starting from a specified date and continuing for a defined number of intervals.    
Arguments:    
Dates: The date column from your date table.     
Start Date: The date on which to begin the period.     
Number of Intervals: The number of intervals to extend the period.     
Interval: The type of interval (DAY, MONTH, QUARTER, or YEAR).     
Output: Returns a table of dates forming a period.     
Use Case: Excellent for creating dynamic rolling reports, such as "last 12 months of sales" or "last 3 months," where you need a defined period of dates to filter your data.    
