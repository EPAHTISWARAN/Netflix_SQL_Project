Netflix SQL Data Analysis Project

📌 Detailed Project Overview

This project is an end-to-end SQL-based data analysis case study built on a Netflix content dataset, designed to demonstrate advanced DBMS and SQL concepts used in real-world data analytics scenarios. The project focuses on transforming raw, semi-structured data into meaningful business insights using PostgreSQL.

The analysis answers practical questions such as content distribution, rating trends, country-wise production, genre popularity, director and actor analysis, temporal trends, and keyword-based content categorization. Emphasis is placed not just on query results, but on how efficiently and correctly the data is modeled, processed, and analyzed within a relational database system.

This project reflects strong fundamentals in Database Management Systems (DBMS) along with hands-on expertise in advanced SQL querying techniques, making it suitable for Data Analyst, SQL Developer, and Business Intelligence roles.




🧠 DBMS Concepts Applied




1️⃣ Relational Data Modeling

Designed a structured relational table (netflix) with appropriate data types.

Converted raw CSV-style data into a normalized relational format suitable for analysis.

Managed schema-level operations such as table creation and deletion using:

DROP TABLE IF EXISTS netflix;
CREATE TABLE netflix (...);

2️⃣ Schema Management & Data Definition Language (DDL)

Used DDL commands to define and reset database objects safely.

Ensured idempotent execution using IF EXISTS, preventing schema conflicts.

3️⃣ Handling Semi-Structured Data in RDBMS

Managed multi-valued attributes such as country, listed_in, and casts stored as comma-separated strings.

Converted them into relational rows using:

STRING_TO_ARRAY()

UNNEST()





🚀 Advanced SQL Techniques Used





1️⃣ Common Table Expressions (CTEs)

Used CTEs to break complex queries into logical, readable steps.

Use Case: Finding the most common rating for Movies and TV Shows.

First CTE calculates rating frequencies

Second CTE ranks them using window functions

This improves:

Query readability

Maintainability

Debugging efficiency

2️⃣ Window Functions

Applied window functions such as:

RANK() OVER (PARTITION BY ... ORDER BY ...)

Use Case:

Identifying top ratings per content type

Ranking analytical results without collapsing rows

This demonstrates understanding of analytical processing beyond basic GROUP BY.

3️⃣ Advanced Aggregations & Grouping

Used COUNT() with GROUP BY for trend and distribution analysis

Performed nested aggregations to calculate percentage contribution of yearly content releases

Example:

COUNT(show_id)::numeric / total_count * 100

4️⃣ String Manipulation & Text Processing

Extensive use of string functions to clean and analyze textual data:

SPLIT_PART() – extracting numeric values from duration strings

STRING_TO_ARRAY() – converting comma-separated values

UNNEST() – normalizing multi-value fields

ILIKE – case-insensitive keyword matching

Use Cases:

Longest movie identification

Genre-wise content analysis

Actor & director analysis

Keyword-based content classification

5️⃣ Date & Time Handling

Handled unstructured date values stored as strings:

Converted text dates using TO_DATE()

Filtered recent data using date arithmetic and INTERVAL

Use Case:

Identifying content added in the last 5 years

6️⃣ Conditional Logic (CASE Statements)

Implemented business logic using CASE WHEN expressions.

Use Case:

Categorizing content as Good or Bad based on keywords like kill and violence

This showcases the ability to implement rule-based classification directly within SQL.

7️⃣ Subqueries & Derived Tables

Used subqueries to calculate totals and averages

Employed derived tables for cleaner filtering and analysis

8️⃣ Data Quality & Null Handling

Identified missing or incomplete data using IS NULL

Ensured robust filtering where data inconsistencies exist





📈 Analytical Thinking Demonstrated





Business-driven query design

Trend analysis over time

Country-wise and genre-wise insights

Actor and director popularity analysis

Content classification using textual patterns




🎯 Why This Project Stands Out





Uses real-world, messy data instead of idealized datasets

Demonstrates both DBMS theory and practical SQL implementation

Shows ability to handle complex analytical queries

Written with clean, readable, and modular SQL




🧩 Ideal For




Data Analyst portfolios

SQL / DBMS academic projects

Interview-ready SQL case studies

GitHub showcase projects



🛠️ Tech Stack



Database: PostgreSQL

Language: SQL

Tools: pgAdmin / psql (or any PostgreSQL-compatible client)
