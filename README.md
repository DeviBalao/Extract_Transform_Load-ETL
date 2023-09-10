# Extract Transform Load - ETL

Building an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions (Regex) to extract and transform the data. 

### Extract:

Data is extracted from two Excel files (crowdfunding.xlsx and contacts.xlsx) using Pandas functions. 
### Transform:

Data Transformations are done using Pandas and Python functions for the data from crowdfunding.xlsx. Two different options are used for transforming the data from contacts.xlsx.

#### ETL_Mini_Project:
In this jupyter notebook file, all data transformations like spliting a column into multiple columns, changing the datatype of the columns, extracting specific data from string values, etc are handled using Pandas and Python functions.

#### ETL_Mini_Project_Regex:
In this jupyter notebook file, data transformations like spliting a column into multiple columns, changing the datatype of the columns, etc are handled using Pandas and Python functions. Transformations like extracting specific data (first name, last name, etc) from contact details are handled using regular expressions (Regex).

Either of these two files can be used to handle the data transformations. The transformed data is exported to four CSV files (category.csv, subcategory.csv, campaign.csv and contacts.csv). 

### Load:

The transformed data is loaded to a Postgres database. Based on the transformed data in the CSV files, Entity Relation Diagram (ERD) is designed using QuickDBD [https://www.quickdatabasediagrams.com/] and the corresponding Database schema is generated. 

        Entity Relation Diagram:



The generated Database schema can be exported to a file (which has queries to create the tables according to the ERD) and used to create the required tables in a Postgres database. After creating the tables, the transformed data from the CSV files are imported into the corresponding tables. While importing data, care should be taken to import data in proper order so that the keyconstraints are satisfied.

    Sample of data in the tables:



Note: The Database_ERD and Database_schema files are available along with code files. All the Excel and CSV files are available in the Resources folder.


