Sales Data Warehouse ETL Pipeline (SSIS & SQL Server)
Overview

This project focuses on designing and implementing a Sales Data Warehouse using SQL Server Integration Services (SSIS). The solution includes building a complete ETL pipeline that extracts data from source systems, applies transformations, and loads it into a structured data warehouse optimized for analytical reporting.

The warehouse is designed using a star schema to support efficient querying and business intelligence operations.

Data Warehouse Design

The data model follows a star schema structure consisting of one fact table surrounded by multiple dimension tables.

Fact Table
Sales Fact Table containing transactional measures related to sales operations.

Dimension Tables
Customer Dimension
Product Dimension
Salesman Dimension
Date Dimension
Time Dimension

Each dimension table is connected to the fact table using surrogate keys to ensure data integrity and performance optimization.

ETL Process (SSIS)

The ETL pipeline is implemented using SQL Server Integration Services and follows a structured flow:

Data is extracted from source files or transactional systems
Data is cleaned and validated by handling missing values, duplicates, and inconsistencies
Data transformations are applied including type conversions and business rule enforcement
Data is first loaded into staging tables
Dimension tables are populated with surrogate key mapping using Lookup transformations
Fact table is loaded after resolving all dimensional relationships

Key Features

Star schema data warehouse design
End-to-end ETL pipeline using SSIS
Surrogate key management for all dimensions
Lookup transformations for dimension mapping
Incremental loading using control tables
Separation of staging and warehouse layers
Support for Date and Time dimensions for detailed analytics

Incremental Load Strategy

Control tables are used to manage incremental loading by tracking the last processed records. This ensures that only new or updated data is processed during each ETL execution, improving performance and reducing redundant processing.

Technologies Used

SQL Server
SQL Server Integration Services (SSIS)
T-SQL
Visual Studio (SQL Server Data Tools)

Project Structure

Source Data
SSIS Packages
SQL Scripts
Staging Database
Data Warehouse Schema
Control Tables

Learning Outcomes

Designing a relational data warehouse using star schema
Building ETL pipelines using SSIS
Implementing surrogate keys and Lookup transformations
Handling incremental data loading using control mechanisms
Structuring data for analytical and reporting purposes

Future Enhancements

Implementation of Slowly Changing Dimensions (SCD Type 2)
Integration with Power BI dashboards for visualization
Automation of ETL execution using SQL Server Agent
Advanced logging and error handling mechanisms
