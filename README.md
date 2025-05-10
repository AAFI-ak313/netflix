# Netflix SQL Project

## Overview

> *This project focuses on analyzing Netflix's content catalog using SQL. The goal is to explore trends, uncover insights, and build queries that help understand Netflix’s offerings over time.*

## Dataset

> *The dataset used in this project is the Netflix Movies and TV Shows dataset, which includes the following key fields*:

 - show_id: Unique ID for each show

 - type: Movie or TV Show

 - title: Title of the show

 - director: Director of the show

 - cast: Main cast

 - country: Country of production

 - date_added: Date added to Netflix

 - release_year: Release year

 - rating: TV rating

 - duration: Duration in minutes or number of seasons

 - listed_in: Genres

 - description: Short summary


### **Tools Used**

 > SQL (MySQL/PostgreSQL/SQLite depending on your setup)

 > DBMS: Any SQL-supporting environment (e.g., MySQL Workbench, pgAdmin, SQLiteStudio)

 > Notebook or VS Code (optional for visualization and scripting)


### **Key Objectives**

 > Understand the structure of the Netflix catalog.

 > Perform exploratory data analysis using SQL queries.

 > Identify trends such as:

 > Most common genres

 > Top directors

 > Yearly content addition trends

 > Country-wise content distribution

 > TV Shows vs Movies ratio


#### Clean and transform data for better analysis.


##### Example Queries

**Top 10 countries with the most content**:

`SELECT country, COUNT(*) AS total
FROM netflix
GROUP BY country
ORDER BY total DESC
LIMIT 10;`

**Number of titles added per year**:

`SELECT YEAR(date_added) AS year, COUNT(*) AS titles_added
FROM netflix
GROUP BY year
ORDER BY year;`

**Most popular genres:**

`SELECT listed_in, COUNT(*) AS count
FROM netflix
GROUP BY listed_in
ORDER BY count DESC;`


### How to Use

1. Import the dataset into your SQL environment.


2. Run the provided SQL queries or write your own.


3. Analyze the results and generate insights.


4. Optionally, export results to Excel or visualize in tools like Tableau or Power BI.



### Future Enhancements

 - Create a dashboard using Tableau or Power BI.

 - Automate queries using Python.

 - Perform sentiment analysis on descriptions using NLP tools.


### License

 > This project is for educational purposes only.
