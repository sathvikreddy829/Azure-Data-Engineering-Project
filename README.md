# Azure-Data-Engineering-Project

AZURE DATA ENGINEERING CARS PROJECT :

Copy Data 
INCREMENTAL loading using lookup activities and dynamic pipeline using Date column
Lookup activity>>>>>watermark table>>>>>> stored procedure for initial load and incremental load 
	
Databricks:
Databricks >>> secret ID > app registration >>> data lake gen2 (adding role assignment to data lake to read and write data)
create compute service in data bricks
Creating silver and gold schema in data bricks meta store 

Data Transformation using split() function and performing / operation on 2 columns to derive the unit price of the product 
Data writing >>>> silver layer

Creating dimension models 
gold dimension model >>>>> creating SCD type 1 table 
1.create distinct() source columns 
2.create schema for initial and incremental load by using if condition
3.Join both the schema and source columns 
4.filter old values which are not null
5.filter new values which are null
6.Add surrogate key by using flag parameter and monotonically_increasing_id()
7.create final data frame and add old values and new values using union()
8.writedata to the gold layer and create dimension table >>> If table exists merge()/Upsert() i.e. SCD type1

creating fact table 
1.Read relative columns from silver table/one big table
2.create data fames for dimension tables 
3.join silver data frame with dimension tables and select related columns for fact table by using dimension keys 

Create data workflow using notebooks 
 



