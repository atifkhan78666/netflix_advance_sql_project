# Netflix Movies and TV Shows Data Analysis using Advance SQL

![Netflix Logo](https://github.com/atifkhan78666/netflix_advance_sql_project/blob/main/logo.png)


#Project Overview
This project conducts a comprehensive SQL analysis of Netflix's content library to extract actionable business insights from their movies and TV shows catalog. The analysis addresses key questions about content strategy, including distribution patterns, rating classifications, content duration trends, and geographic production insights.
SQL provides an efficient framework for this analysis due to its ability to handle structured data aggregation, complex filtering, and analytical computations directly within the database layer. This approach enables rapid insight generation without the overhead of external processing tools, making it ideal for exploratory analysis of catalog data.
#Dataset Description
The analysis utilizes the Netflix Movies and TV Shows dataset, containing metadata for titles available on the platform. The dataset includes:

Title name and content type classification (Movie/TV Show)
Production details (director, cast, country of origin)
Temporal information (release year, date added to platform)
Content specifications (rating, duration, genre)

The dataset presents real-world data quality characteristics, including missing values, inconsistent formatting, and mixed data types across approximately 8,800 records. These characteristics make it representative of actual business analytics scenarios.
Objectives of Analysis
The project addresses the following analytical objectives:

Analyze content distribution across movies and TV shows to understand catalog composition
Identify the most prevalent content ratings and their distribution patterns
Determine longest-duration content by category for quality benchmarking
Examine temporal trends in content additions and release patterns
Investigate geographic production distribution and country-specific content strategies
Explore genre popularity and categorization patterns
Segment content by strategic business criteria (rating, duration, release timing)

Key SQL Concepts Utilized
This analysis demonstrates proficiency in advanced SQL techniques:

Aggregation Functions: COUNT, MAX, MIN, AVG for statistical summaries
Window Functions: ROW_NUMBER, RANK, DENSE_RANK for ranking and top-N analysis
Complex Filtering: WHERE clauses with multiple conditions, pattern matching using LIKE/ILIKE
Subqueries: Nested queries for comparative analysis and filtering
Grouping and Segmentation: GROUP BY with HAVING clauses for categorical analysis
Data Type Handling: CAST operations and string manipulation functions
Conditional Logic: CASE statements for dynamic categorization
Set Operations: DISTINCT for unique value identification

Analysis Highlights
The SQL analysis produces the following business insights:

Content catalog composition breakdown showing the relative proportion of movies versus TV shows
Distribution analysis of content ratings revealing platform positioning strategy
Identification of longest-duration movies and most extensive TV show series
Year-over-year content addition trends indicating platform growth patterns
Geographic production analysis highlighting key content sourcing markets
Genre distribution patterns informing content strategy and audience targeting
Country-specific content catalogs for regional market analysis
Rating-based segmentation for audience demographic understanding
Recent content additions tracking for freshness monitoring
Director and cast frequency analysis for creator partnership insights

Project Structure
├── dataset/
│   └── netflix_titles.csv
├── sql/
│   └── analysis_queries.sql
├── README.md
dataset/: Contains the Netflix titles CSV file with content metadata
sql/: Includes all analytical SQL queries organized by business question
README.md: Project documentation and analysis summary
Implementation Instructions
Prerequisites:

PostgreSQL 12+ or MySQL 8+ database environment
SQL client (pgAdmin, DBeaver, MySQL Workbench, or command line)

Setup Steps:

Create a new database for the project

sqlCREATE DATABASE netflix_analysis;

Create the table schema

sqlCREATE TABLE netflix_titles (
    show_id VARCHAR(10) PRIMARY KEY,
    type VARCHAR(10),
    title VARCHAR(200),
    director VARCHAR(250),
    cast TEXT,
    country VARCHAR(200),
    date_added VARCHAR(50),
    release_year INT,
    rating VARCHAR(10),
    duration VARCHAR(15),
    listed_in VARCHAR(100),
    description TEXT
);

Import the CSV file using your SQL client's import functionality or COPY command
Execute queries from the analysis_queries.sql file individually or in sequence

Compatibility Note: Queries are written for PostgreSQL but can be adapted for MySQL with minor syntax adjustments (primarily string functions and date handling).
Skills Demonstrated
This project showcases the following analytical and technical competencies:

SQL Analytics: Advanced query construction for business intelligence
Data Exploration: Systematic investigation of dataset characteristics and patterns
Business Insight Generation: Translation of raw data into strategic recommendations
Analytical Problem-Solving: Structured approach to answering business questions
Data Quality Assessment: Recognition and handling of real-world data inconsistencies
Performance Optimization: Efficient query design for large datasets
Documentation: Clear communication of technical analysis for stakeholder audiences

Conclusion
This project demonstrates a practical application of SQL analytics to derive business intelligence from content platform data. The analysis reflects the type of exploratory work performed by data analysts in media and entertainment organizations, where understanding content strategy, audience preferences, and catalog composition directly informs business decisions.
The combination of technical SQL proficiency and business-focused analysis methodology showcases the core skillset required for data analyst roles in content-driven industries.
