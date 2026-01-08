📦 SSIS Package Overview – NHS A&E ETL
Package Name

NHS_AE_Hybrid_ETL.dtsx

Purpose

This SSIS package is responsible for extracting NHS A&E attendance data from an Excel source, cleaning and transforming the data, and loading it into a SQL Server database for analytics and reporting.

Data Flow Description

The SSIS Data Flow performs the following steps:

Excel Source

Reads NHS A&E attendance data from an Excel workbook

Source data contains inconsistent formatting and mixed data types

Derived Column Transformation

Removes leading and trailing spaces using LTRIM and RTRIM

Handles NULL values by replacing them with safe defaults

Removes commas from numeric values

Cleans percentage symbols from percentage fields

Data Conversion Transformation

Converts cleaned string values into appropriate numeric data types

Ensures compatibility with SQL Server schema

OLE DB Destination

Loads transformed data into SQL Server staging tables

Enforces relational schema and data integrity

Execution & Validation

Package execution shows successful data flow completion

Row counts are verified between source and destination

Loaded data is validated using SQL queries in SSMS

Design Considerations

Text cleaning performed before numeric conversion to avoid runtime errors

Separation of cleansing and conversion improves maintainability

Package designed for repeatable execution

Tools Used

SQL Server Integration Services (SSIS)

SQL Server

SQL Server Management Studio (SSMS)
