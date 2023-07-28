# Crowdfunding_ETL
Project 2

This mini project involved several tasks to create a crowdfunding database. Firstly, we created two DataFrames: "category" and "subcategory." These DataFrames were extracted from the "crowdfunding.xlsx" Excel data and contained information about unique categories and subcategories, respectively. We exported these DataFrames as "category.csv" and "subcategory.csv" and saved them to the GitHub repository.

Next, we created the "campaign" DataFrame from the same "crowdfunding.xlsx" data. The "campaign" DataFrame included various columns such as "cf_id," "contact_id," "company_name," "description," "goal," "pledged," "outcome," "backers_count," "country," "currency," "launch_date," "end_date," "category_id," and "subcategory_id." We converted the "goal" and "pledged" columns to the float data type and the "launch_date" and "end_date" columns to the datetime format. The "campaign" DataFrame was exported as "campaign.csv" and saved to the GitHub repository.

Additionally, we created the "contacts" DataFrame, either using Option 1 with Python dictionary methods or Option 2 with regular expressions, based on the "contacts.xlsx" Excel data. The "contacts" DataFrame contained columns for "contact_id," "first_name," "last_name," and "email." For Option 1, we iterated through the DataFrame and converted each row to a dictionary, then split the "name" column into "first_name" and "last_name." For Option 2, we used regular expressions to extract the required columns and split the "name" column. The cleaned "contacts" DataFrame was exported as "contacts.csv" and saved to the GitHub repository.

In the next phase, we designed the database schema using an ERD, which included tables for "category," "subcategory," "campaign," and "contacts." The schema defined data types, primary keys, foreign keys, and other constraints. We saved this schema as "crowdfunding_db_schema.sql" in the GitHub repository.

With the database schema in hand, we created a new Postgres database named "crowdfunding_db." Following the schema, we created the required tables in the correct order to handle foreign keys. We verified table creation by running SELECT statements for each table.

Finally, we imported the data from the CSV files into the corresponding SQL tables. After import, we verified that each table contained the correct data by running SELECT statements for each table.

In conclusion, the mini project covered data extraction and transformation from Excel files, creating DataFrames, exporting them as CSV, designing a database schema based on an ERD, creating a Postgres database, creating and verifying tables, and importing data into the tables to build the crowdfunding database.

links used:
https://stackoverflow.com/questions/44327999/how-to-merge-multiple-dataframes

https://stackoverflow.com/questions/17134716/convert-dataframe-column-type-from-string-to-datetime


