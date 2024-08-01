# Introduction to Databases

- **Relational Databases**: Efficient for storing and accessing massive amounts of data.
- **Spreadsheet Tools**: Excel and Google Sheets use a table format with rows and columns.
    - **Example**: Each row represents a patient, and each column contains data elements (e.g., name, date of birth).
- **Limitations of Spreadsheets**:
    - Works well when each column has a single entry per patient.
    - Problem arises with multiple events (e.g., multiple clinic visits).
        - **Issue**: How to represent multiple visits in one column.
        - **Solution 1**: Add more columns (e.g., visit one, visit two).
        - **Solution 2**: Duplicate rows with the same patient information.
- **Relational Databases**:
    - Use multiple related tables.
    - **Example**:
        - **Patient Table**: Contains patient name, date of birth, and a unique patient ID. Each patient has one row.
        - **Encounters Table**: Records each clinic visit. Multiple rows for a patient with multiple encounters. Contains patient ID, encounter date, and details, along with a unique encounter ID.
- **Relational Aspect**:
    - Common columns (e.g., Patient_ID) in both tables allow combining data.
    - **Example**: Answering "Who was seen in the clinic yesterday?" by matching visit records with patient names.
- **Data Integrity**:
    - **Spreadsheets**: Any data type can be entered into any field.
    - **Databases**: Each column has a specific data type (e.g., number, character, timestamp). Data must match the column format.

This structured format and integrity make relational databases a robust solution for managing complex and large-scale data sets.

# Querying Tables with SQL

- **SQL (Structured Query Language)**:
    - Used to access and manage data in databases.
    - Also known as "sequel."
- **Querying a Database**:
    - Accessing data for viewing or analysis.
- **Single Table Querying**:
    - General format: Select data from a table.
    - **Example**:
        - Query to see the entire table: `SELECT * FROM patient;`
        - Shows all columns and rows in the table.
- **Selecting Particular Variables**:
    - Variables are stored in columns.
    - **Example**:
        - Query to select specific columns: `SELECT first_name, last_name FROM patient;`
        - Returns all rows but only the specified columns (first_name and last_name).
- **Selecting Particular Records**:
    - Records are stored in rows.
    - Use a WHERE statement to filter rows.
    - **Example**:
        - Query to select rows based on a condition: `SELECT * FROM patient WHERE birth_year > 1980;`
        - Shows all columns but only rows where birth year is greater than 1980.
- **Combining Queries**:
    - Select specific columns and filter rows.
    - **Example**:
        - Query to select specific columns and filter rows: `SELECT first_name, last_name FROM patient WHERE birth_year > 1980;`
        - Returns first and last names of patients born after 1980.

This approach allows efficient access to specific data subsets within a database, facilitating targeted analysis and data management.

# Joining Tables with SQL

- **Combining Tables in SQL**:
    - Process known as joining tables.
    - Requires at least one common variable across tables.
- **Example**:
    - Two tables, X and Y, each with an identifier column and data.
    - Join on the common identifier column.
- **Types of Joins**:
    - **Inner Join**:
        - Takes rows common to both tables.
        - Syntax: `SELECT * FROM x INNER JOIN y ON x.ID = y.ID`
        - Example: Shows all columns from both tables for matching rows.
    - **Left Join**:
        - Takes all rows from the left table and matches data from the right table.
        - If no match, columns from the right table are left blank.
        - Syntax: `SELECT * FROM x LEFT JOIN y ON x.ID = y.ID`
        - Example: If a row in X has no match in Y, columns from Y are blank.
    - **Right Join**:
        - Takes all rows from the right table and matches data from the left table.
        - If no match, columns from the left table are left blank.
        - Syntax: `SELECT * FROM x RIGHT JOIN y ON x.ID = y.ID`
        - Example: If a row in Y has no match in X, columns from X are blank.
- **Complex Left Join Example**:
    - Second table has two matches to a single row in the first table.
    - Left join replicates the row data from the first table to match both rows of the second table.
- **Query Nuances with Joins**:
    - Explicitly label which table holds a particular column.
    - Use format: `Table_Name.Column_Name`
    - Table alias can simplify long table names:
        - Example: `SELECT * FROM Patient AS p`
        - Use alias for columns: `p.Last_Name`
- **Column Alias**:
    - Simplify column names in the result.
    - Example: `Patient.Last_Name AS Last_Name`
    - Rename a column: `select Patient.Last_Name as Pt_Last_Name from Patient`
- **Importance of Understanding Joins**:
    - Joins are powerful but complex.
    - Animations available for repeated viewing for better understanding.
- **Acknowledgment**:
    - Thanks to Garrick Aden-Buie for creating and sharing these animations on GitHub as an open educational resource.

# Aggregating Data with SQL

- **Data Aggregation**:
    - Process of combining and summarizing data.
- **Example Scenario**:
    - **Table**: Encounters, lists all patient encounters at a hospital in the last year.
    - Columns: encounter ID (unique), patient ID (identifies patient), date of encounter.
- **Counting Rows**:
    - **Question**: How many encounters happened in the last year?
    - Use the `count` function:
        - Query: `SELECT COUNT(*) FROM encounters;`
        - Returns the number of rows in the table.
- **Counting Unique Patients**:
    - **Question**: How many unique patients were seen?
    - Use the `DISTINCT` command to filter duplicates:
        - Query: `SELECT COUNT(DISTINCT patient_ID) FROM encounters`
        - Returns the number of distinct patients.
- **Counting Visits per Patient**:
    - Use the `GROUP BY` clause to group rows and apply a function to each group:
        - Query: `SELECT patient_ID, COUNT(DISTINCT encounter_ID) FROM encounters GROUP BY patient_ID`
        - Returns a list showing the number of visits per patient.
        - **Rule**: The column being grouped by must be in the `SELECT` statement.
- **Additional Aggregation Functions**:
    - **MIN**: Find the minimum value.
    - **MAX**: Find the maximum value.
    - **AVG**: Find the average value.
    - **Variety of SQL Functions**: Functions may differ slightly across SQL variants (MySQL, Postgres, Google BigQuery).
- **Ordering Data**:
    - **ORDER BY**: Arrange data in a specific order.
        - Example: `ORDER BY patient_ID` (ascending order).
        - Reverse order: `ORDER BY patient_ID DESC` (descending order).
- **Combining `GROUP BY` and `ORDER BY`**:
    - Can use multiple columns in both commands.
    - Columns used must be in the `SELECT` statement.

These commands and functions allow for efficient data analysis and manipulation, enabling detailed insights and organized data presentation.

# Introduction to BigQuery

- **BigQuery Overview**:
    - Tool for storing and accessing data in a specialization.
    - Google Cloud platform's enterprise data warehouse for analytics.
    - Uses standard SQL for data access.
    - Scales linearly to store many petabytes of data.
    - Fully encrypted with easy data access management and control.
    - Pricing based on the amount of data stored and queried.
    - No need to buy or maintain hardware.
- **Accessing BigQuery**:
    - Web interface:
        - View databases and tables.
        - Write and see query results.
        - View query history.
    - Database drivers and libraries for programming languages (Python, R).
- **Reason for Choosing BigQuery**:
    - Effective tool for clinical data science.
    - Healthcare generates massive amounts of data.
    - Clinical data warehouses must store decades of data for millions of patients.
    - Regular databases struggle with querying such large datasets.
    - Advanced systems like BigQuery's Dremel backend are necessary.
- **Advantages of BigQuery**:
    - Massive parallel processing capabilities.
    - Fast query processing times.
    - Example: Complex text searches of billions of patient notes in about 2 minutes.
    - Used by UC Health, Children's Hospital of Colorado, CU Medicine, and the university for storing and querying patient data.
    - Reduced query times by 97% compared to previous on-site technology.
    - Supports storage and analysis of genomic data.
    - Connects data with publicly available datasets (e.g., air quality measurements).
- **Conclusion**:
    - BigQuery is a highly effective tool for managing and analyzing large-scale healthcare data.
    - Excited to use BigQuery throughout the specializatio