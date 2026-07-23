# ✈️ Airport Data Analysis using MySQL

## 📌 Project Overview

This project demonstrates a complete end-to-end **Airport Data Analysis** solution using **MySQL**. The project focuses on transforming raw aviation data into a well-structured relational database, followed by performing SQL-based exploratory data analysis to uncover meaningful business insights.

The workflow begins by importing raw flight data into a staging table (`Meta_Data`). The dataset is then normalized into multiple relational tables following good database design principles. Finally, various SQL queries are executed to analyze passenger traffic, flight routes, airport performance, and the relationship between city population and air traffic.

This project showcases practical SQL skills including:

- Database Design
- Data Modeling
- Data Normalization
- Data Cleaning
- SQL Joins
- Aggregate Functions
- GROUP BY Analysis
- Data Transformation
- Business Intelligence Queries

The project is suitable for Data Analyst and SQL portfolio demonstrations because it mimics a real-world ETL (Extract, Transform, Load) workflow before performing analytical reporting.

---

# 🛠️ Technologies Used

- MySQL 8.0
- MySQL Workbench
- SQL
- Relational Database Concepts

---

# 📂 Database Architecture

The raw airport dataset is first imported into a staging table named:

- **Meta_Data**

The data is then normalized into separate relational tables.

### Tables Created

### 1. Airline
Contains airline-related information.

Columns include:

- Airline ID
- Carrier Code
- Carrier Name
- Carrier Entity

---

### 2. Airport

Stores airport details such as:

- Airport ID
- Airport Code
- Airport Sequence ID
- City
- State
- Market ID
- WAC

This table is created by combining both Origin and Destination airport records while removing duplicates.

---

### 3. Flight

Stores flight-specific information.

Contains:

- Airline
- Origin Airport
- Destination Airport
- Distance
- Distance Group
- Year
- Quarter
- Month
- Flight Class

Each flight receives a unique auto-generated Flight ID.

---

### 4. FlightMetrics

Contains measurable flight statistics including:

- Passenger Count
- Freight
- Mail

This table is linked to the Flight table using the Flight ID.

---

### 5. City

Stores city information including:

- City Name
- State
- Population (after enrichment)

The city table is later enhanced by joining with an external population dataset.

---

# 🔄 ETL Process

The project follows a structured ETL pipeline.

## Step 1

Import raw data into the **Meta_Data** table.

## Step 2

Create normalized relational tables.

## Step 3

Populate dimension tables:

- Airline
- Airport
- City

## Step 4

Populate fact tables:

- Flight
- FlightMetrics

## Step 5

Clean city names using string functions such as:

- `SUBSTRING_INDEX()`

## Step 6

Merge city population data.

## Step 7

Perform business analysis using SQL queries.

---

# 📊 Business Analysis Performed

The project answers several real-world aviation business questions.

## 1. Route-wise Passenger Analysis

Identifies the busiest routes based on passenger traffic.

Metrics:

- Origin Airport
- Destination Airport
- Origin City
- Destination City
- Total Passengers

---

## 2. Monthly Passenger Trend

Calculates the number of passengers transported each month.

Metrics:

- Year
- Month
- Total Passengers

Useful for identifying seasonal travel demand.

---

## 3. Average Passengers per Origin Airport

Calculates:

- Total Flights
- Total Passengers
- Average Passengers per Flight

This helps identify high-performing origin airports.

---

## 4. Average Passengers per Destination Airport

Ranks destination airports based on:

- Passenger Volume
- Flight Count
- Average Passengers

Useful for identifying major travel hubs.

---

## 5. Flight Frequency Analysis

Determines:

- Most frequently traveled routes
- High-traffic flight corridors

Metrics include:

- Flight Count
- Origin City
- Destination City

---

## 6. Airport Performance Comparison

Compares airports based on:

- Total Flights
- Total Passengers

Performed separately for:

- Origin Airports
- Destination Airports

---

## 7. Population vs Air Traffic Analysis

One of the most interesting analyses in the project.

The city table is enriched with population data to study whether larger cities generate more air traffic.

Metrics calculated include:

- Population
- Total Passengers
- Total Flights
- Passenger-to-Population Ratio

This provides insights into airport utilization relative to city size.

---

# 📈 SQL Concepts Demonstrated

This project demonstrates practical usage of:

- DDL Statements
- DML Statements
- INSERT INTO SELECT
- UNION
- INNER JOIN
- LEFT JOIN
- GROUP BY
- ORDER BY
- Aggregate Functions
- COUNT()
- SUM()
- AVG()
- ROUND()
- DISTINCT
- LIMIT
- AUTO_INCREMENT
- Foreign Keys
- Data Cleaning using String Functions
- Data Normalization

---

# 📌 Key Learning Outcomes

Through this project, the following concepts were applied:

- Designing a normalized relational database
- Building relationships using primary and foreign keys
- Loading and transforming raw datasets
- Writing analytical SQL queries
- Performing business intelligence reporting
- Integrating external datasets
- Cleaning inconsistent textual data
- Generating actionable insights from aviation data

---

# 🚀 Future Improvements

Possible enhancements include:

- Building an interactive Power BI dashboard
- Creating Tableau visualizations
- Adding flight delay analysis
- Analyzing airline-wise performance
- Forecasting passenger traffic using Python
- Developing stored procedures and SQL views
- Optimizing queries with indexes

---

# 📚 Conclusion

This project demonstrates a complete SQL-based data analysis workflow, starting from raw data ingestion and database normalization to generating meaningful business insights. By organizing the data into relational tables and applying SQL techniques such as joins, aggregations, and data transformation, the project highlights how structured query language can be used to solve real-world analytical problems.

The analyses provide valuable insights into passenger trends, airport performance, route popularity, and the relationship between city population and air traffic. Overall, this project reflects practical database design skills, ETL processes, and analytical thinking, making it a strong portfolio project for aspiring Data Analysts and SQL developers.
