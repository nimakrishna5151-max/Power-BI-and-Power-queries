**Data Transformation**

Using Get data function in power bi  uploaded 3 data set one by one 
1.Row Restriction: Restricted the "List of Orders" table to the first 500 rows for streamlined processing.  
Data Type Optimization: Converted "Order Date" to Date data type, and set "Amount" and "Target" columns to Fixed Decimal Number.  
Text Formatting: Standardized the "CustomerName" column into proper case ("Capitalize Each Word") for clean visual presentation.  
Column Merging: Combined the "State" and "City" columns into a new custom column named "Location" formatted as City, State.  
Custom Calculations:
Created a custom column named "Profit Margin" calculated as [Profit] / [Amount] and formatted it as a percentage.  
Added a conditional column named "Profit Status": labeled as "Loss" if profit < 0, "Break-Even" if = 0, and "Profit" if > 0.  
2. Merging & Data Cleaning
Table Merging (Joins): Merged "List of Orders" and "Order Details" into a unified single table named "Orders Data" using the relational "Order ID".  
Missing & Duplicate Values: Evaluated datasets to handle null identifiers and managed duplicate line items strategically to preserve unique transaction lines.  
3. Sorting & Filtering
Sorting: Organized the "Orders Data" table by sorting "Order Date" in descending order to surface recent trends.  
Regional Filtering: Applied regional filters on the location data to isolate specific states for targeted regional analysis , i filtered based on the state called banglore.  
4. Grouping & Aggregating Data
Order Details Aggregation: Duplicated the "Order Details" table and grouped data to compute the count of each Order ID, average profit by Category, and total amount by Sub-Category.  
Sales Target Aggregation: Duplicated the "Sales Target" table and aggregated the total target amount by the month of Order Date.  
5. Data Modeling & Relationships
Model Configuration: Established a primary One-to-Many (1:*) relationship between "List of Orders" and "Order Details" using the "Order ID" column.  
 Linked the "Order Details" and "Sales Target" tables based on the matching Category column.
