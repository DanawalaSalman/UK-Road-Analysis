# UK Road Safety Data Analysis Project

## Project Overview

The UK Road Safety Data Analysis Project for the year 2015 aims to analyze traffic and road-related data to gain insights into accident severity, vehicle types, and other relevant information. The project involves creating database schemas, loading data, calculating median severity for motorcycle accidents, and conducting various data analyses.

## SQL Files

### 01. UK_Road_Safety_Accidents_Schema_Tables_Load_Data.sql
This SQL script is responsible for creating the necessary database schema and tables for the project. The schema named "accidents" is created.
Three tables are created: "accident," "vehicles," and "vehicle_types" to store accident data, vehicle data, and vehicle types, respectively.
Data is loaded into these tables from CSV files: "Accidents_2015.csv," "Vehicles_2015.csv," and "Vehicle_Types.csv."
### 02. UK_Road_Safety_Accidents_Create_severity_median_Table.sql
This SQL script creates a table named "accidents_median" to store the calculated median severity values for different vehicle types.
### 03. motorcycle_accidents_median_severity_calculation.py
This Python script calculates the median severity for motorcycle accidents.
It connects to the MySQL database using the "pymysql" library.
It retrieves a list of motorcycle-related vehicle types from the "vehicle_types" table.
For each motorcycle-related vehicle type, it calculates the median severity of accidents and inserts the result into the "accidents_median" table.
### 04. UK_Road_Safety_Accidents_Data_Analysis.sql
This SQL script contains various data analysis queries.
It creates indexes on the "accident_index" column in the "accident" and "vehicles" tables to improve query performance.
It provides queries to:
Get accident severity and the total number of accidents per vehicle type.
Calculate the average severity by vehicle type.
Calculate the average severity and total accidents specifically for motorcycle-related vehicle types.

## Project Workflow

Start by running the "01. UK_Road_Safety_Accidents_Schema_Tables_Load_Data.sql" script to create the database schema and load the initial data.
Execute the "02. UK_Road_Safety_Accidents_Create_severity_median_Table.sql" script to create the "accidents_median" table.
Run the Python script "03. motorcycle_accidents_median_severity_calculation.py" to calculate and insert median severity values for motorcycle accidents.
Finally, you can analyze the data using the queries provided in "04. UK_Road_Safety_Accidents_Data_Analysis.sql." These queries include information about accident severity, vehicle types, and motorcycle-related data.
