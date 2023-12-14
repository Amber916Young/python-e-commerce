If your original data is in columns B, F, and J (with 'REF' in column B, 'COLOR_CN' in column F, and 'inv' in column J), and you want to filter rows where the sum of 'inv' is greater than 200 for each unique combination of 'REF' and 'COLOR_CN', you can follow these steps:

1. **Create a Helper Column for Summing 'inv':**
   - In cell K2, enter the formula to sum 'inv' for each 'REF' and 'COLOR_CN' combination:
     ```excel
     =SUMIFS(J:J, B:B, B2, F:F, F2)
     ```
     Drag this formula down for all rows.

2. **Filter Rows with 'inv' > 200:**
   - In cell L2, enter the formula to check if the sum of 'inv' is greater than 200:
     ```excel
     =IF(K2 > 200, 1, 0)
     ```
     Drag this formula down for all rows.

3. **Filter and Copy Data:**
   - Filter the data based on the 'inv' column (column L) to show only rows where 'inv' is greater than 200.
   - Copy the visible rows (filtered data).
   - Paste the copied data to another sheet or location.

Now, you have the filtered data where the sum of 'inv' is greater than 200 for each unique combination of 'REF' and 'COLOR_CN'. Adjust the column references based on your actual data structure.
