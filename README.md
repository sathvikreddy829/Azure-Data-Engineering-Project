# Azure-Data-Engineering-Project

Azure Data Engineering Cars project

Utilizing lookup operations and a dynamic pipeline with a date column, copy data incrementally and then
Using Databricks To read and write data from Data Lake Gen2, create a silver and gold schema in the Data Bricks Meta Store
After the data has been transformed using notebooks in data bricks, it is put in the silver layer schema

Utilizing if/else conditions, create schema for initial and incremental load by reading different relative source columns to use in the dimension table.
After identifying the source and schema columns as dataframes, join them both, filter out old, non-null values, and then filter out new, null values.
Use the flag parameter and the monotonically_increasing_id() function to add a surrogate key for the dimension table 
Use union() to generate the final data frame and add the old and new values.
establish a dimension table, write data to the gold layer, and  The merge()/Upsert() function (i.e. SCD type1) is used if a table exists already 

Utilized dimension keys to align each dimension table with the fact table to craete star schema 
