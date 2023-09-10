# Extract Transform Load - ETL

Building an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions (Regex) to extract and transform the data. 

### Extract:

Data is extracted from two Excel files (crowdfunding.xlsx and contacts.xlsx) using Pandas functions. 
### Transform:

Data Transformations are done using Pandas and Python functions for the data from crowdfunding.xlsx. Two different options are used for transforming the data from contacts.xlsx.

ETL_Mini_Project:
In this jupyter notebook file, all data transformations like spliting a column into multiple columns, changing the datatype of the columns, extracting specific data from string values, etc are handled using Pandas and Python functions.

ETL_Mini_Project_Regex:
In this jupyter notebook file, data transformations like spliting a column into multiple columns, changing the datatype of the columns, etc are handled using Pandas and Python functions. Transformations like extracting specific data (first name, last name, etc) from contact details are handled using regular expressions (Regex).

Either of these two files can be used to handle the data transformations. The transformed data is exported to four CSV files (category.csv, subcategory.csv, campaign.csv and contacts.csv). 

### Load:

The transformed data is loaded to a Postgres database. Based on the transformed data in the CSV files, Entity Relation Diagram (ERD) is designed using QuickDBD [https://www.quickdatabasediagrams.com/] and the corresponding Database schema is generated. 

Entity Relation Diagram:

<img width="602" alt="ERD" src="https://github.com/TestUser-2022/Extract_Transform_Load-ETL/assets/98562722/b49fce05-2663-46d9-96b7-2772cf8473cc">


The generated Database schema can be exported to a file (which has queries to create the tables according to the ERD) and used to create the required tables in a Postgres database. After creating the tables, the transformed data from the CSV files are imported into the corresponding tables. While importing data, care should be taken to import data in proper order so that the keyconstraints are satisfied.

Sample of data in the tables:

<img width="300" alt="category table sample data" src="https://github.com/TestUser-2022/Extract_Transform_Load-ETL/assets/98562722/5d14f5c0-ea69-443a-8a42-d6cf50af6b0d">

<img width="291" alt="subcategory table sample data" src="https://github.com/TestUser-2022/Extract_Transform_Load-ETL/assets/98562722/95c2a21e-fbaa-4824-8088-3289b128376a">

<br> <p>
<img width="768" alt="campaign table sample data" src="https://github.com/TestUser-2022/Extract_Transform_Load-ETL/assets/98562722/e94bf61d-6c9f-40a6-b799-b17270c1f3fa">
</p>



Note: The Database_ERD and Database_schema files are available along with code files. All the Excel and CSV files are available in the Resources folder.


