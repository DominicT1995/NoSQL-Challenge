# NoSQL-Challenge
UTSA Data Analytics Bootcamp NoSQL challenge where UK restaurant ratings data will be updated, aggregated, and analyzed using MongoDB and Python.

------------------------------------------------------------------------------------------------------------------
Resources

Inside the No-SQL-Challenge repository, there is a Resources folder containing the establishments.json file that is used for data extraction for this repository. Using terminal, locate the Resources folder and run:

mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json

This will import the dataset under the database 'uk_food' with a single collection named 'establishments'.

------------------------------------------------------------------------------------------------------------------
UKFoodRatings

The UKFoodRatings folder contains the NoSQL_setup_starter.ipynb and NoSQL_analysis_starter.ipynb files which are used to setup and update the uk_food database and analyze it, respectively.

The NoSQL_setup_starter.ipynb utilizes PyMongo to explore the uk_food database, update the database with a new restaurant, edit the new restaurant document based on existing document info, delete documents pertaining to a specified local authority, and convert string type numbers in the database to integer and decimal types.

The NoSQL_analysis_starter.ipynb file utilizes PyMongo to filter the updated database on queries that will answer the following questions:

1. Which establishments have a hygiene score equal to 20?
2. Which establishments in London have a RatingValue greater than or equal to 4?
3. What are the top 5 establishments with a RatingValue rating value of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
4. How many establishments in each Local Authority area have a hygiene score of 0?

The results are displayed by converting the queries into DataFrames and listing the number of documents produced by the query, or the number of rows present in the resulting DataFrame.