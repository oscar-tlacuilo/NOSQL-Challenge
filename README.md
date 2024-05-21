# UK Food Hygiene Ratings Analysis

## Project Overview

This project involves evaluating the food hygiene ratings of various establishments across the United Kingdom using MongoDB and Python. The goal is to help the editors of the food magazine, Eat Safe, Love, to analyze the data and provide insights to their journalists and food critics.

# Part 1: Database and Jupyter Notebook Setup
This section covers the setup process for the database and Jupyter Notebook.

## Data Import
The establishments.json data file is imported into MongoDB using the following command:


### Copy code
mongoimport --db uk_food --collection establishments --drop --file establishments.json --jsonArray


# Part 2: Update the Database
This section covers the updates made to the database.

## Modifications
1. Adding New Restaurant:

The data for the new restaurant, "Penang Flavours," is inserted into the establishments collection.

2. Finding BusinessTypeID:

A query is executed to find the BusinessTypeID for "Restaurant/Cafe/Canteen" and returns only the relevant fields.

3. Updating "Penang Flavours" Document:

The document for "Penang Flavours" is updated with the correct BusinessTypeID.

4. Removing Dover Establishments:

Documents with "Dover Local Authority" are deleted from the collection.

5. Data Type Conversion:

Latitude, longitude, and RatingValue fields are converted to appropriate data types.

# Part 3: Exploratory Analysis
This section focuses on exploratory analysis of the data.

## Analysis Questions
1. Hygiene Score of 20:

- Query to find establishments with a hygiene score of 20.
- Count the number of documents and display the first result.
- Convert results to a Pandas DataFrame.
  
2. Establishments in London with RatingValue >= 4:

- Query to find establishments in London with a RatingValue greater than or equal to 4.
- Count the number of documents and display the first result.
- Convert results to a Pandas DataFrame.

3. Top 5 Establishments with RatingValue of 5:

- Query to find the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score and nearest to "Penang Flavours" restaurant.
- Convert results to a Pandas DataFrame.

4. Local Authorities with Hygiene Score of 0:

- Aggregation pipeline to count establishments in each Local Authority area with a hygiene score of 0.
- Sort results from highest to lowest and display the top ten local authority areas.
- Convert results to a Pandas DataFrame.

