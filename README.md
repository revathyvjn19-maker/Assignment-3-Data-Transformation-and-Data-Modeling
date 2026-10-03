# Assignment-3-Data-Transformation-and-Data-Modeling
Power BI Assignment 1 – Data Transformation and Data Modeling 
Power BI Assignment 1 – Data Transformation & Data Modeling

# Import Data:
●	Import “List of Orders.csv” into Power BI.

**Power BI -Home – Get Data – Text/CSV- Select data (“List of Orders.csv”)- Load**

●	Open “List of Orders” in Power Query Editor by clicking on ‘Transform’.

**Select data (List of orders) in Power BI – Transform data**

●	Import “Order Details.csv” and “Sales target.csv” into Power Query Editor.

**Home – New Source – Text/ CSV- Select data (“Order Details.csv”) – Ok**

**Home – New Source – Text/ CSV- Select data (“Sales target.csv”) – Ok**


# Data Transformation:
●	Restrict the "List of Orders" table to only the first 500 rows.

**Home – Keep Rows – Keep Top Rows – 500 – Ok**

●	Ensure the “Order Date” column in the “List of Orders” table is set to data type 'Date'.

**Set Order date column data type to ‘Date’**

●	Change the data type of “Amount” and “Target” columns to ‘Fixed Decimal Number’.

**Set Amount and Target Column data type to ‘Fixed Decimal Number’**

●	Format	the	"Customer Name"	column	into	proper	case,	ensuring consistent capitalization for each word.

**Select column “customer name”- Transform – Format – Capitalize each word**

●	Merge the "State" and "City" columns to create a new column named "Location" in the format ‘City, State’.

**Reordered Columns "State" and "City"  to “City and State” and created new column named Location**

**Selected “City and State” column – Transform – Merge Columns**

●	Create a new custom column named "Profit Margin" as the percentage of "Profit" divided by "Amount".

**Add column – Custom Column – Changed Column name to “Profit Margin”**
**Formula - Profit Margin = Profit ÷ Amount**

 
●	Add a new conditional column named "Profit Status" based on the values in the "Profit" column. The conditions are as follows: if the profit is less than 0, the label should be "Loss"; if the profit equals 0, the label should be "Break-Even"; and if the profit is greater than 0, the label should be "Profit".

**Add column – Conditional Column – Changed Column name to “Profit Status”**

Syntax
**IF (profit) < 0 then loss ,else if (profit) < = 0 Break-even, else 0**


# Merging Data (Joins):
●	Merge the "List of Orders" and "Order Details" tables into a new single table named "Orders Data" based on the "Order ID" relationship.

**Merged the "List of Orders" and "Order Details" tables into a new single table named "Orders Data" based on the "Order ID" relationship
Home – Merge Queries – Merge Queries as New**

# Handling Missing Data & Duplicate Data:
●	Identify missing values in the data and determine a strategy to address them.
**There is no missing values in the data set**

●	Check for duplicate rows and define a strategy to handle duplicates.

**Select column - Home – Remove Rows- Remove  Duplicates**


# Sorting and Filtering Data:

●	In the ‘Orders Data’ table, utilize sorting and filtering techniques on columns like Order Date, State or Category to analyze data based on specific criteria:
◆	Sort the orders by Order Date in descending order to analyze recent trends.

**Select Order date column – Sort  Descending**

◆	Filter the orders to focus only on a specific state (e.g., Tamil Nadu) for regional analysis.

**Select Location Column – Select the “ Tamil Nadu” state from the drop down**

Grouping and Aggregating Data:
●	Duplicate the “Order Details” table and calculate the count of each Order ID, average profit by Category or total amount by Sub-Category.
Duplicate “ Order details” table – Group by Order ID – Operation given as count rows – Ok
**Duplicate “Order details” table - Group by Sub category – Operation given as Sum  and Column given as amount – ok**

●	Duplicate the “Sales Target” table and aggregate the total target amount by Month of Order Date.

**Duplicate “Sale target” table – Group by – Month of order date – operation given as sum  - and column given as “Target”**

Data Modeling:
●	Establish a relationship between the “List of Orders” and “Order Details” tables using the ‘Order ID’ column.

**Modeling – Manage Relationship – New relationship – give from table as Order details  and To table as List of Order– Set cardinality as Many to one  and set cross filter direction – Save**

●	Build a relationship between the “Order Details” and “Sales Target” tables based on the ‘Category’ column. Click "Manage relationships" and ensure this relationship is active.

**Modeling – Manage Relationship – New relationship – give from table as Order details and To table as Sales target-  Set cardinality as Many to Many and set cross filter direction – Save**
