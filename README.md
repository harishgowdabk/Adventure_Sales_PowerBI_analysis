# Adventure_Sales_PowerBI_analysis

# 💡 Project Overview

AdventureWorks Database is a Microsoft product sample for an online transaction processing (OLTP) database. The AdventureWorks Database supports a fictitious, multinational manufacturing company called Adventure Works Cycles. Analyzed data of this fictitious company by connecting and shaping data in Power Query, built a relational model and added calculate fields with DAX measures. Finally, created an interactive Dashboard for data visualization of the performance of the company.

# Contents

Connect and transform the raw data

Creating table relationships and data models

Create new calculated columns and DAX measures

Design an interactive report to analyze and visualize the data

# Connect and transform the raw data
Access data from database tables, flat files, folders and created fully automated data shaping and loading (ETL) procedures

The Query Editor
The Power Query Editor consist various Query Editing tools like table transformations, calculated columns, etc it also consist of Formula Bar to write 'M' code and applied steps pane to see the
steps applied

The main tabs of Power Query Editor are 'Transform' and 'Add column'

The TRANSFORM tab includes tools to modify existing columns
(splitting/grouping, transposing, extracting text, etc)

The ADD COLUMN tools create new columns (based on conditional rules, text operations, calculations, dates, etc

# Conditional Columns
Conditional Columns allow you to define new fields based on logical rules and conditions (IF/THEN statements)

For example: In this case we’re creating a new conditional column called “QuantityType”, which depends on the values in the “OrderQuantity” column, as follows:

If OrderQuantity =1, QuantityType = “Single Item”

If OrderQuantity >1, QuantityType = “Multiple Items”

Otherwise QuantityType = “Other”

# Hierarchies
Hierarchies are groups of nested columns that reflect multiple
levels of granularity

For example, a “Geography” hierarchy might include Country State, and City columns

Each hierarchy can be treated as a single item in tables and reports, allowing users to “drill up” and “drill down” through different levels of the hierarchy in a
meaningful way

# Creating table relationships and data models
Data models
Data Modeling is one of the features used to connect multiple data sources in BI tool using a relationship. A relationship defines how data sources are connected with each other and you can create interesting data visualizations on multiple data sources

# Creating Snowflake schemas
Models with chains of dimension tables are often called “snowflake” schemas (whereas “star” schemas usually have individual lookup tables surrounding a central data table)
By creating relationships from Products to Subcategories (using ProductSubcategoryKey) and Subcategories to Categories (using ProductCategoryKey), we have essentially connected Sales_Data to each lookup table; filter context will now flow all the way down the chain

# Relationship Cardinality
Cardinality refers to the uniqueness of values in a column

For our purposes, all relationships in the data model should follow a “one-to-many” cardinality; one instance of each primary key, but potentially many instances of each foreign key

# calculated columns and DAX measures
DAX
Data Analysis Expressions, commonly known as DAX, is the formula language that drives Power BI
With DAX we can

Add calculated columns and measures to your model, using intuitive syntax

Go beyond the capabilities of traditional “grid-style” formulas, with powerful and flexible functions built specifically to work with relational data models.

# calculated columns
Calculated columns are typically used for filtering data, rather than creating numerical values

Calculated columns generate values for each row, which are visible within tables in the Data view

Calculated columns understand row context; they’re great for defining properties based on information in each row, but generally useless for aggregation (SUM, COUNT, etc)

# Measures
Measures are DAX formulas used to generate new calculated values

Use measures to create numerical, calculated values that can be analyzed in the “values” field of a report visual

Measures are evaluated based on filter context, which means they recalculate when the fields or filters around them change (like when new row or column labels are pulled into a matrix or when new filters are applied to a report

# Related
RELATED() = Returns related values in each row of a table based on relationships with other tables

=RELATED(ColumnName)

# Calculate
CALCULATE() = Evaluates a given expression or formula under a set of defined filters

=CALCULATE(Expression, [Filter1], [Filter2],…)

CALCULATE works just like SUMIF or COUNTIF in Excel, except it can evaluate measures based on ANY sort of calculation (not just a sum, count, etc); it may help to think of it like “CALCULATEIF”

#  Power BI Report View
The Power BI report view consist of various tools and visualization options such as Charts, Slicers, Maps, Matrices, etc Filters Pane such as Visual-Level, Page-Level, and Report-Level Filters

This options will provide to create Interactive visualization
