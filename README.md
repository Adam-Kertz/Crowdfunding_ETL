# Crowdfunding_ETL
### Project Introduction and File Locations
Boot Camp Project Page:<br>
https://courses.bootcampspot.com/courses/3483/assignments/52329?module_item_id=937307<br>
<br>
The purpose of this project is to build an ETL pipeline using Python to extract and transform campaign data. The starting data is contained in two files that were provided by EdX:<br>
<br>
A file containing contacts:<br>
https://github.com/Adam-Kertz/Crowdfunding_ETL/blob/main/Resources/contacts.xlsx<br>
and a file containing additional campaign data:<br>
https://github.com/Adam-Kertz/Crowdfunding_ETL/blob/main/Resources/crowdfunding.xlsx<br>
<br>
The following python file is used to transform the data:<br>
https://github.com/Adam-Kertz/Crowdfunding_ETL/blob/main/ETL_Mini_Project_Starter_Code_TWade_AKertz.ipynb<br>
*comments within the above file provide detailed descriptions of the types of transformations performed<br>
<br>
The above python code produces the following 4 csv files:<br>
<br>
General Crowdfunding Campaign Info:<br>
https://github.com/Adam-Kertz/Crowdfunding_ETL/blob/main/Resources/campaign.csv<br>
A Table of Crowdfunding Catagories:<br>
https://github.com/Adam-Kertz/Crowdfunding_ETL/blob/main/Resources/category.csv<br>
A Table of Crowdfunding Subcategories:<br>
https://github.com/Adam-Kertz/Crowdfunding_ETL/blob/main/Resources/subcategory.csv<br>
Important Contact Information:<br>
https://github.com/Adam-Kertz/Crowdfunding_ETL/blob/main/Resources/contacts.csv<br>
<br>
The database was created using the following schematic design<br>
https://github.com/Adam-Kertz/Crowdfunding_ETL/blob/main/Resources/Database%20Schema/Database%20Schema.jpg<br>
Exporting the above diagram produced the following import code<br>
https://github.com/Adam-Kertz/Crowdfunding_ETL/blob/main/Resources/Database%20Schema/crowdfunding_db_schema.sql<br>
Which can be used with the csv files above to load and create a database
### Steps to Re-produce Results
##### 1) Run the jupyter notebook file
https://github.com/Adam-Kertz/Crowdfunding_ETL/blob/main/ETL_Mini_Project_Starter_Code_TWade_AKertz.ipynb
##### 2) Open pgAdmin and create a database named crowdfunding_db
##### 3) Run the code from the crowdfunding_db_schema.sql file to create the tables
##### 4) Populate each of the tables by importing the corresponding csv file
Make sure to import the campaign.csv file last, as the campaign table has dependencies on other tables.
##### 5) Run the following commands to verify the data has been properly imported into the database
<br>SELECT * FROM "Campaign"<br>
<br>SELECT * FROM "Category"<br>
<br>SELECT * FROM "Contacts"<br>
<br>SELECT * FROM "Subcategory"<br>
Note: The quotes around the table names are necessary because QuickDBD's export tool names the tables that way.
