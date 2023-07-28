# Crowdfunding_ETL
Project 2

This mini project involved several tasks to create a crowdfunding database. Firstly, in the "[ETL_Mini_Project_JPealy_AHlavac.ipynb](https://github.com/aliciahlavac/Crowdfunding_ETL/blob/main/ETL_Mini_Project_JPealy_AHlavac.ipynb)" file, we created two DataFrames: "category" and "subcategory." These DataFrames were extracted from the Excel data named "[crowdfunding.xlsx](https://github.com/aliciahlavac/Crowdfunding_ETL/blob/main/Resources/crowdfunding.xlsx)" and contained information about unique categories and subcategories, respectively. 

![category](https://github.com/aliciahlavac/Crowdfunding_ETL/assets/127240852/4719da6f-556e-4a41-be47-82fdb526c203)![subcategory](https://github.com/aliciahlavac/Crowdfunding_ETL/assets/127240852/597268d5-da83-4f57-ac95-588cc40fb388)

We exported these DataFrames as "[category.csv](https://github.com/aliciahlavac/Crowdfunding_ETL/blob/main/Resources/category.csv)" and "[subcategory.csv](https://github.com/aliciahlavac/Crowdfunding_ETL/blob/main/Resources/subcategory.csv)".

Next, we created the "campaign" DataFrame from the same "[crowdfunding.xlsx](https://github.com/aliciahlavac/Crowdfunding_ETL/blob/main/Resources/crowdfunding.xlsx)" data. The "campaign" DataFrame included various columns such as "cf_id," "contact_id," "company_name," "description," "goal," "pledged," "outcome," "backers_count," "country," "currency," "launch_date," "end_date," "category_id," and "subcategory_id." We converted the "goal" and "pledged" columns to the float data type and the "launch_date" and "end_date" columns to the date format. The "campaign" DataFrame was exported as "[campaign.csv](https://github.com/aliciahlavac/Crowdfunding_ETL/blob/main/Resources/campaign.csv)".

![campaign_df](https://github.com/aliciahlavac/Crowdfunding_ETL/assets/127240852/511f96a9-3e65-4cbb-a4a9-3671ffb756d7)

Additionally, we created the "contacts" DataFrame, based on the "[contacts.xlsx](https://github.com/aliciahlavac/Crowdfunding_ETL/blob/main/Resources/campaign.csv)" Excel data. The "contacts" DataFrame contained columns for "contact_id," "first_name," "last_name," and "email."We iterated through the DataFrame and converted each row to a dictionary, then split the "name" column into "first_name" and "last_name." The cleaned "contacts" DataFrame was exported as "[contacts.csv](https://github.com/aliciahlavac/Crowdfunding_ETL/blob/main/Resources/contacts.csv)" and saved to the GitHub repository.

In the next phase, we designed the database schema using an ERD, which included tables for "category," "subcategory," "campaign," and "contacts." The schema defined data types, primary keys, foreign keys, and other constraints. We saved this schema as "[crowdfunding_db_schema.sql](https://github.com/aliciahlavac/Crowdfunding_ETL/blob/main/Crowdfunding_DB_Schema.sql)" in the GitHub repository.

![ERD](https://github.com/aliciahlavac/Crowdfunding_ETL/assets/127240852/248ea845-c224-4b69-a9e2-75c080d51fe7)

Next, we created a new Postgres database named "crowdfunding_db." Following the schema, we created the required tables in the correct order to handle foreign keys. Finally, we imported the data from the CSV files into the corresponding SQL tables. After import, we verified that each table contained the correct data by running SELECT statements for each table.

In conclusion, the mini project covered data extraction and transformation from Excel files, creating DataFrames, exporting them as CSV, designing a database schema based on an ERD, creating a Postgres database, creating and verifying tables, and importing data into the tables to build the crowdfunding database.

Links used for reference when writing code:

https://stackoverflow.com/questions/44327999/how-to-merge-multiple-dataframes

https://stackoverflow.com/questions/17134716/convert-dataframe-column-type-from-string-to-datetime


