### 1. What is a function in SQL Server, and how is it used?
- A function in SQL Server is a programmable routine that accepts parameters, performs a specific task, and returns a value.
- Functions can be used to encapsulate frequently used logic, making code more modular and maintainable.
- They can be used in SQL statements such as SELECT, WHERE, and HAVING clauses.
- Functions help improve code readability and reusability in database operations.

### 2. How many types of functions are there in SQL Server, and what are they?
- Scalar Functions: Return a single value of any SQL data type.
- Inline Table-Valued Functions (TVFs): Return a table based on a single SELECT statement.
- Multi-Statement Table-Valued Functions (TVFs): Return a table and can contain multiple statements to construct the final result.
- System Functions: Built-in functions provided by SQL Server, such as GETDATE() for current date and time.

### 3. What is a stored procedure, and what are its benefits?
- A stored procedure is a precompiled collection of SQL statements stored in the database.
- Benefits include improved performance due to precompilation and efficient execution plans.
- Stored procedures enhance security by restricting direct access to the underlying data.
- They promote code reuse and maintainability by centralizing complex business logic.

### 4. What are the differences between a function and a stored procedure?
- Functions must return a value (scalar or table), whereas stored procedures do not have to return a value.
- Functions can be used in SELECT, WHERE, and HAVING clauses, while stored procedures cannot.
- Stored procedures can perform DML operations (INSERT, UPDATE, DELETE), whereas functions are generally read-only.
- Functions do not support error handling with TRY...CATCH, while stored procedures do.

### 5. What is the COALESCE function in SQL, and how is it used?
- COALESCE is a SQL function that returns the first non-null expression among its arguments.
- It is commonly used to handle null values in SQL queries.
- COALESCE can take multiple arguments and return the first non-null value.
- It simplifies the handling of default values for nullable columns.

### 6. Can you explain the properties of the COALESCE function?
- COALESCE evaluates arguments from left to right and returns the first non-null value.
- It can handle a variable number of arguments, making it flexible for various use cases.
- The return type of COALESCE is determined by the highest precedence data type among the arguments.
- COALESCE is ANSI SQL compliant and widely supported across different database systems.

### 7. How does the COALESCE function handle null values?
- COALESCE returns the first non-null value from its list of arguments.
- If all arguments are null, COALESCE returns null.
- It is an efficient way to provide default values for nullable columns.
- COALESCE can be used to avoid null value propagation in expressions and calculations.

### 8. Can you provide examples of using the COALESCE function in SQL queries?
- Example 1: `SELECT COALESCE(column1, 'Default Value') FROM table;` - returns 'Default Value' if column1 is null.
- Example 2: `SELECT COALESCE(column1, column2, column3) FROM table;` - returns the first non-null value among the three columns.
- Example 3: `SELECT COALESCE(NULL, NULL, 'Fallback Value');` - returns 'Fallback Value' as all previous arguments are null.
- Example 4: `UPDATE table SET column1 = COALESCE(column1, 'Default');` - updates column1 to 'Default' if it is null.

### 9. What are some benefits of using stored procedures in database operations?
- Stored procedures encapsulate complex business logic, making the application code simpler and more maintainable.
- They improve performance through precompilation and optimized execution plans.
- Stored procedures enhance security by restricting direct access to tables and providing controlled access through execution rights.
- They support error handling and transaction management, ensuring data integrity and consistency.

### 10. How does the COALESCE function compare to the CASE expression in SQL?
- COALESCE is simpler and more concise for handling multiple null checks compared to the CASE expression.
- COALESCE evaluates all arguments and returns the first non-null value, whereas CASE can include more complex logic with multiple conditions.
- CASE provides more flexibility for complex conditional logic, while COALESCE is more straightforward for null handling.
- COALESCE can handle a varying number of arguments, while CASE requires explicit conditions for each possible scenario.
### 11. What is SQL, and how is it used?
- SQL (Structured Query Language) is a standardized language used to manage and manipulate relational databases.
- It allows users to perform various operations such as querying data, updating records, and managing database structures.
- SQL consists of several sublanguages, including DDL (Data Definition Language), DML (Data Manipulation Language), and DCL (Data Control Language).
- SQL is used by database administrators, developers, and analysts to interact with databases and extract meaningful information.

### 12. What is SQL Server, and what are its components?
- SQL Server is a relational database management system (RDBMS) developed by Microsoft.
- Key components include the Database Engine, which handles storage, processing, and security; SQL Server Management Studio (SSMS) for database administration; and SQL Server Agent for job scheduling and automation.
- SQL Server supports various services like Integration Services (SSIS) for data integration, Analysis Services (SSAS) for data analysis, and Reporting Services (SSRS) for reporting.
- It provides tools for database development, management, and business intelligence.

### 13. What is a database, and what is its purpose?
- A database is a structured collection of data stored electronically in a computer system.
- It is designed to efficiently store, retrieve, and manage data.
- Databases ensure data consistency, integrity, and security.
- They support various operations like querying, updating, and administration to facilitate data management and analysis.

### 14. What is a table, and how is data organized within it?
- A table is a database object that organizes data into rows and columns.
- Each row represents a unique record, and each column represents a specific attribute of the data.
- Tables have a defined schema that specifies the data types and constraints for each column.
- Tables are used to store structured data and are the fundamental building blocks of a relational database.

### 15. What is a view in SQL, and how does it differ from a table?
- A view is a virtual table that is created by a query joining one or more tables.
- Unlike a table, a view does not store data physically; it provides a dynamic representation of the data.
- Views can simplify complex queries, encapsulate business logic, and present data in a specific format.
- They provide an additional layer of security by restricting access to specific columns and rows.

### 16. Can you explain the concept of virtual tables in SQL views?
- Views act as virtual tables that represent the result of a SQL query.
- They allow users to interact with data as if it were a table, without duplicating the actual data.
- Changes in the underlying tables are reflected in the view, ensuring up-to-date information.
- Views can be used to abstract complex joins and calculations, making queries simpler and more readable.

### 17. How can views be used to control access to sensitive data?
- Views can restrict access to specific columns and rows, providing a customized view of the data.
- By granting access to a view instead of the underlying table, sensitive information can be hidden from unauthorized users.
- Views can implement row-level security by filtering data based on user roles or permissions.
- They provide an additional layer of abstraction and control over data access policies.

### 18. What are some benefits of using views in a database?
- Views simplify complex queries by encapsulating them into a single virtual table.
- They enhance security by restricting access to specific data elements.
- Views provide a consistent interface to data, even if the underlying schema changes.
- They can improve performance by predefining complex joins and calculations, reducing the need for repetitive query processing.

### 19. How are views created in SQL?
- Views are created using the CREATE VIEW statement followed by the view name and the defining query.
- Example: `CREATE VIEW view_name AS SELECT column1, column2 FROM table WHERE condition;`
- Views can be updated using the CREATE OR REPLACE VIEW statement.
- They can be dropped with the DROP VIEW statement when no longer needed.

### 20. Can you provide an example of when to use a view in a database design?
- A view can be used to present a summarized version of sales data, joining multiple tables such as orders, customers, and products.
- Example: `CREATE VIEW sales_summary AS SELECT customer_name, product_name, SUM(sales_amount) FROM orders JOIN customers ON orders.customer_id = customers.id JOIN products ON orders.product_id = products.id GROUP BY customer_name, product_name;`
- This view simplifies reporting by providing a consolidated view of sales data without exposing the details of the underlying tables.
- Views are also useful for creating read-only representations of data for reporting purposes, ensuring that users cannot modify the source data.

### 21. What is normalization, and what is its purpose in database design?
- Normalization is the process of organizing data in a database to reduce redundancy and improve data integrity.
- It involves dividing large tables into smaller, related tables and defining relationships between them.
- The purpose of normalization is to eliminate duplicate data, ensure data dependencies make sense, and facilitate data consistency.
- Normalized databases are easier to maintain and less prone to anomalies during data operations.

### 22. Can you explain the different normal forms in database normalization?
- **First Normal Form (1NF)**: Ensures that each column contains atomic (indivisible) values and each record is unique.
- **Second Normal Form (2NF)**: Builds on 1NF by ensuring that all non-key columns are fully dependent on the primary key.
- **Third Normal Form (3NF)**: Extends 2NF by ensuring that all non-key columns are not only fully dependent on the primary key but also independent of each other (no transitive dependency).
- **Boyce-Codd Normal Form (BCNF)**: A stricter version of 3NF where every determinant is a candidate key.
- **Fourth Normal Form (4NF)**: Ensures no multi-valued dependencies other than a candidate key.
- **Fifth Normal Form (5NF)**: Decomposes tables to avoid any join dependencies.

### 23. What is denormalization, and when is it used in database design?
- Denormalization is the process of combining normalized tables to improve read performance at the cost of write performance and data redundancy.
- It is used when querying complex relationships in a normalized database becomes too slow and cumbersome.
- Denormalization can reduce the number of joins required to retrieve data, thereby improving query performance.
- It is often employed in read-heavy applications, data warehouses, and OLAP systems where performance is a critical factor.

### 24. What are the differences between DDL and DML commands in SQL?
- **DDL (Data Definition Language)**: Used to define and modify database structures such as tables, indexes, and views. Examples include CREATE, ALTER, and DROP.
- **DML (Data Manipulation Language)**: Used to manipulate data within existing structures. Examples include SELECT, INSERT, UPDATE, and DELETE.
- DDL commands affect the schema and structure of the database, while DML commands affect the data within the schema.
- DDL changes are usually auto-committed, meaning they are permanently saved in the database, while DML changes can be rolled back if they are within a transaction.

### 25. What is a default constraint in SQL Server, and how is it used in table creation?
- A default constraint in SQL Server specifies a default value for a column when no value is provided during an insert operation.
- It ensures that columns have a predefined value, improving data consistency and integrity.
- Default constraints are defined using the DEFAULT keyword in the CREATE TABLE or ALTER TABLE statements.
- Example: `CREATE TABLE Employees (ID INT, Name NVARCHAR(100), HireDate DATE DEFAULT GETDATE());` - This sets the HireDate to the current date if no value is provided.

### 26. How does denormalization affect query performance in a database?
- Denormalization can improve read performance by reducing the number of joins required to retrieve related data.
- It can lead to faster query execution times and improved performance for read-heavy operations.
- However, denormalization can negatively impact write performance due to increased data redundancy and the need to update multiple copies of the same data.
- Maintaining data integrity becomes more challenging, as changes need to be propagated across denormalized tables.

### 27. Can you provide examples of DDL and DML commands in SQL?
- **DDL Examples**:
  - `CREATE TABLE Customers (ID INT, Name NVARCHAR(100));` - Creates a new table.
  - `ALTER TABLE Customers ADD Email NVARCHAR(100);` - Adds a new column to an existing table.
  - `DROP TABLE Customers;` - Deletes an existing table.
- **DML Examples**:
  - `INSERT INTO Customers (ID, Name) VALUES (1, 'John Doe');` - Inserts a new record.
  - `UPDATE Customers SET Name = 'Jane Doe' WHERE ID = 1;` - Updates an existing record.
  - `DELETE FROM Customers WHERE ID = 1;` - Deletes an existing record.

### 28. When would you choose to denormalize a database schema?
- Denormalization is chosen when the application requires faster read performance and can tolerate some level of data redundancy.
- It is suitable for read-heavy applications, such as reporting systems, data warehouses, and OLAP systems.
- Denormalization can simplify complex queries and improve query performance in scenarios where frequent joins are required.
- It is often employed in cases where the database design must be optimized for specific use cases that prioritize read operations over write operations.

### 29. How do you ensure data integrity when denormalizing a database?
- Use triggers to automatically update related tables when changes occur, ensuring data consistency.
- Implement constraints, such as foreign keys and unique constraints, to maintain data integrity.
- Regularly validate and reconcile data between denormalized tables to identify and correct inconsistencies.
- Employ application logic to handle updates and maintain synchronization between denormalized tables.

### 30. Can you discuss the trade-offs between normalization and denormalization in database design?
- **Normalization**:
  - **Pros**: Reduces data redundancy, ensures data integrity, and simplifies data maintenance.
  - **Cons**: Can lead to complex queries with multiple joins, potentially impacting read performance.
- **Denormalization**:
  - **Pros**: Improves read performance by reducing the number of joins required, simplifies query logic.
  - **Cons**: Increases data redundancy, complicates data maintenance, and can negatively impact write performance.
- The choice between normalization and denormalization depends on the specific use case, application requirements, and performance considerations.
- A balanced approach may involve selectively denormalizing certain parts of the database while keeping other parts normalized to achieve optimal performance and data integrity.

### 31. What are ACID properties in SQL Server?
- **Atomicity**: Ensures that all operations within a transaction are completed successfully or none are. If any part of the transaction fails, the entire transaction is rolled back.
- **Consistency**: Guarantees that a transaction will bring the database from one valid state to another, maintaining database integrity.
- **Isolation**: Ensures that concurrent transactions do not interfere with each other, providing a consistent view of data to each transaction.
- **Durability**: Ensures that once a transaction has been committed, it will remain so, even in the event of a system failure.

### 32. What is the difference between DELETE and TRUNCATE commands?
- **DELETE**:
  - Removes rows from a table based on a condition.
  - Can be rolled back if used within a transaction.
  - Triggers are fired for each row deleted.
  - Slower compared to TRUNCATE because it logs individual row deletions.
- **TRUNCATE**:
  - Removes all rows from a table, resetting the table to its empty state.
  - Cannot be rolled back as it is a DDL operation.
  - Triggers are not fired because it does not delete rows individually.
  - Faster because it deallocates the data pages used by the table.

### 33. What is the difference between DROP and TRUNCATE queries?
- **DROP**:
  - Completely removes a table or database from the database management system.
  - Irreversible and cannot be rolled back.
  - All associated data, indexes, and constraints are also removed.
- **TRUNCATE**:
  - Removes all rows from a table without removing the table itself.
  - Resets identity columns if they exist.
  - Can be faster than DELETE but does not remove the table schema.

### 34. What is a trigger in SQL Server?
- A trigger is a special type of stored procedure that automatically executes in response to certain events on a table or view.
- Triggers can be used to enforce business rules, data integrity, and audit changes.
- There are three types of triggers: DML triggers (for INSERT, UPDATE, DELETE), DDL triggers (for CREATE, ALTER, DROP), and logon triggers.
- Triggers can be complex and impact performance, so they should be used judiciously.

### 35. How to handle errors in SQL Server?
- Use TRY...CATCH blocks to handle exceptions and errors in T-SQL code.
- In the TRY block, write the code that might throw an error.
- In the CATCH block, write the code to handle the error, such as logging the error and providing a user-friendly message.
- Example:
  ```sql
  BEGIN TRY
      -- Code that might cause an error
  END TRY
  BEGIN CATCH
      -- Error handling code
      SELECT ERROR_MESSAGE() AS ErrorMessage;
  END CATCH;
  ```

### 36. What is the clustered index in SQL Server?
- A clustered index determines the physical order of data in a table.
- There can be only one clustered index per table because the data rows themselves are stored in the order of the clustered index key.
- It improves the performance of data retrieval when accessing rows by the indexed columns.
- Example: `CREATE CLUSTERED INDEX idx_name ON table_name(column_name);`

### 37. What is the non-clustered index in SQL Server?
- A non-clustered index does not alter the physical order of the data in the table.
- It creates a separate structure from the data rows, with pointers to the actual data.
- Multiple non-clustered indexes can exist on a single table.
- Example: `CREATE NONCLUSTERED INDEX idx_name ON table_name(column_name);`

### 38. What is the difference between a clustered index and a non-clustered index in SQL Server?
- **Clustered Index**:
  - Determines the physical order of data in the table.
  - Only one clustered index per table.
  - Faster for retrieving a range of data.
  - Example: Primary key index.
- **Non-Clustered Index**:
  - Does not determine physical order of data.
  - Multiple non-clustered indexes per table.
  - Separate structure from the data rows with pointers to the data.
  - Example: Index on a non-primary key column.

### 39. What is the difference between a table and a view in SQL Server?
- **Table**:
  - Stores data physically in rows and columns.
  - Can have constraints like primary keys, foreign keys, and indexes.
  - Data is stored and can be modified directly.
- **View**:
  - A virtual table created by a query joining one or more tables.
  - Does not store data physically; reflects data from underlying tables.
  - Used for simplifying complex queries, securing data, and presenting data in a specific format.

### 40. What is a self-join in SQL Server?
- A self-join is a join in which a table is joined with itself.
- It is used to compare rows within the same table.
- Useful for hierarchical data or comparing rows within a single table.
- Example:

  SELECT A.employee_id, A.employee_name, B.manager_name
  FROM employees A
  JOIN employees B ON A.manager_id = B.employee_id;

### 41. Can you explain the use of indexes in SQL?
- Indexes improve the speed of data retrieval operations on a database table by providing a quick way to look up rows based on the values in one or more columns.
- There are two main types of indexes: clustered and non-clustered. Clustered indexes determine the physical order of data in a table, while non-clustered indexes maintain a separate structure from the data rows.
- Indexes can be created on one or multiple columns of a table to enhance query performance, especially for large datasets.
- However, indexes can impact the performance of write operations (INSERT, UPDATE, DELETE) since the indexes need to be maintained whenever data is modified.

### 42. How do you manage database transactions and isolation levels in SQL Server?
- Transactions are used to ensure that a sequence of operations is completed successfully as a single unit of work. If any part of the transaction fails, the entire transaction is rolled back.
- SQL Server provides four isolation levels to control the visibility of changes made by other transactions: READ UNCOMMITTED, READ COMMITTED, REPEATABLE READ, and SERIALIZABLE.
- Isolation levels manage concurrency and consistency of data, with higher isolation levels reducing the risk of data anomalies but potentially impacting performance due to increased locking.
- Transactions are managed using the `BEGIN TRANSACTION`, `COMMIT`, and `ROLLBACK` statements.

### 43. What are the differences between clustered and non-clustered indexes?
- **Clustered Index**:
  - Alters the physical order of data in the table.
  - Only one clustered index is allowed per table.
  - Directly impacts the way data is stored and retrieved.
  - Example: Primary key index.
- **Non-Clustered Index**:
  - Does not alter the physical order of data.
  - Multiple non-clustered indexes can exist on a single table.
  - Uses a separate structure to store the index key values and pointers to the actual data rows.
  - Example: Index on a non-primary key column.

### 44. Can you explain the difference between stored procedures and functions?
- **Stored Procedures**:
  - Can perform actions such as modifying data (INSERT, UPDATE, DELETE).
  - Can return zero, one, or multiple result sets.
  - Allow the use of control-of-flow statements like loops and conditional logic.
  - Can have input and output parameters.
- **Functions**:
  - Generally used to compute values and return a single value or table.
  - Cannot perform actions that modify data.
  - Must return a value (scalar functions) or a table (table-valued functions).
  - Can be used in SELECT statements, WHERE clauses, and other SQL expressions.

### 45. What is SQL Injection, and how can it be prevented?
- SQL Injection is a code injection technique where an attacker can execute malicious SQL statements by exploiting vulnerabilities in an application's input handling.
- It can lead to unauthorized access, data manipulation, and data breaches.
- Prevention methods include using parameterized queries, stored procedures, and ORM frameworks that automatically handle SQL injection protection.
- Validating and sanitizing user inputs, applying the principle of least privilege, and using web application firewalls can also help mitigate SQL injection risks.

### 46. What is the difference between INNER JOIN and OUTER JOIN in SQL?
- **INNER JOIN**:
  - Returns only the rows that have matching values in both tables.
  - Excludes rows that do not have matches in the other table.
  - Example: `SELECT * FROM table1 INNER JOIN table2 ON table1.id = table2.id;`
- **OUTER JOIN**:
  - Returns all rows from one table and the matched rows from the other table.
  - Includes rows that do not have matches in the other table (LEFT JOIN, RIGHT JOIN, FULL JOIN).
  - Example: 
    - `LEFT JOIN`: `SELECT * FROM table1 LEFT JOIN table2 ON table1.id = table2.id;`
    - `RIGHT JOIN`: `SELECT * FROM table1 RIGHT JOIN table2 ON table1.id = table2.id;`
    - `FULL JOIN`: `SELECT * FROM table1 FULL JOIN table2 ON table1.id = table2.id;`

### 47. What is a primary key in SQL, and what are its characteristics?
- A primary key is a column or combination of columns that uniquely identifies each row in a table.
- Characteristics of a primary key include:
  - **Uniqueness**: Each value in the primary key column(s) must be unique.
  - **Non-nullability**: Primary key columns cannot contain NULL values.
  - **Single key per table**: Each table can have only one primary key.
  - **Implicit index**: SQL Server automatically creates a clustered index on the primary key column(s), unless specified otherwise.

### 48. What is a foreign key in SQL, and what are its purposes?
- A foreign key is a column or combination of columns that establishes a relationship between two tables by referencing the primary key of another table.
- Purposes of a foreign key include:
  - **Referential integrity**: Ensures that values in the foreign key column correspond to valid values in the referenced primary key column.
  - **Cascading actions**: Can define actions like CASCADE DELETE or CASCADE UPDATE to automatically propagate changes from the parent table to the child table.
  - **Relationships**: Helps enforce logical relationships between tables, supporting relational database design principles.

### 49. What is an index, and how does it improve query performance in SQL Server?
- An index is a database object that improves the speed of data retrieval operations on a table by providing a fast lookup mechanism for rows based on the values in one or more columns.
- Indexes can significantly reduce the amount of data that needs to be scanned during a query, thus improving performance.
- They are particularly useful for large tables where searching for data without an index would be slow and inefficient.
- Indexes can be created on columns used frequently in WHERE clauses, JOIN conditions, and ORDER BY clauses.

### 50. What is a transaction in SQL, and why is it important?
- A transaction is a sequence of one or more SQL operations executed as a single unit of work.
- Transactions are important because they ensure data integrity and consistency, particularly in multi-user environments.
- Key properties of transactions (ACID properties) include Atomicity, Consistency, Isolation, and Durability.
- Transactions allow operations to be committed or rolled back, ensuring that either all changes are applied successfully or none are, thus maintaining database stability and reliability.

### 51. What is a cursor in SQL Server?
- A cursor is a database object used to retrieve, manipulate, and navigate through a result set one row at a time.
- Cursors can be used to perform row-by-row operations in a result set.
- There are different types of cursors, such as static, dynamic, forward-only, and keyset-driven.
- While cursors provide flexibility for row-based operations, they can be slow and resource-intensive, so they should be used judiciously.

### 52. What is a temporary table in SQL Server, and how is it used?
- A temporary table is a table that is created and used temporarily within a session or batch.
- Temporary tables are stored in the tempdb database and are automatically dropped when the session ends or the batch completes.
- There are two types of temporary tables: local temporary tables (prefixed with `#`) and global temporary tables (prefixed with `##`).
- Temporary tables are useful for storing intermediate results, complex queries, and session-specific data manipulation.

### 53. What is a common table expression (CTE) in SQL Server?
- A CTE is a temporary result set that can be referenced within a SELECT, INSERT, UPDATE, or DELETE statement.
- CTEs are defined using the `WITH` clause and can improve readability and maintainability of complex queries.
- CTEs can be recursive, allowing for operations such as hierarchical data retrieval.
- Example:
  ```sql
  WITH CTE AS (
      SELECT column1, column2
      FROM table_name
  )
  SELECT * FROM CTE;
  ```

### 54. What is a UNION in SQL, and how is it used?
- The UNION operator is used to combine the result sets of two or more SELECT statements.
- Each SELECT statement within the UNION must have the same number of columns in the same order, and the columns must have compatible data types.
- UNION removes duplicate rows by default. To include duplicate rows, use UNION ALL.
- Example:
  ```sql
  SELECT column1, column2 FROM table1
  UNION
  SELECT column1, column2 FROM table2;
  ```

### 55. What is a JOIN in SQL, and what types of JOINs are there?
- A JOIN is a SQL operation used to combine rows from two or more tables based on a related column.
- Types of JOINs include:
  - **INNER JOIN**: Returns only matching rows from both tables.
  - **LEFT JOIN (LEFT OUTER JOIN)**: Returns all rows from the left table and matching rows from the right table, with NULLs for non-matching rows.
  - **RIGHT JOIN (RIGHT OUTER JOIN)**: Returns all rows from the right table and matching rows from the left table, with NULLs for non-matching rows.
  - **FULL JOIN (FULL OUTER JOIN)**: Returns all rows when there is a match in either left or right table, with NULLs for non-matching rows.
  - **CROSS JOIN**: Returns the Cartesian product of both tables, combining all rows from the left table with all rows from the right table.

### 56. What is a subquery in SQL, and how is it used?
- A subquery is a query nested within another SQL query.
- Subqueries can be used in SELECT, INSERT, UPDATE, and DELETE statements.
- They can return a single value, a row, or a table.
- Subqueries are used to perform operations that require the results of another query, such as filtering, calculating, or validating data.

### 57. What is the difference between HAVING and WHERE clauses in SQL?
- **WHERE**: Filters rows before any groupings are made. It is used to specify conditions on individual rows.
- **HAVING**: Filters groups after the `GROUP BY` clause has been applied. It is used to specify conditions on groups.
- Example:
  ```sql
  SELECT department, COUNT(*)
  FROM employees
  WHERE salary > 50000
  GROUP BY department
  HAVING COUNT(*) > 10;
  ```

### 58. What is an index scan, and how does it differ from an index seek?
- **Index Scan**:
  - Reads all rows in the index to find the ones that satisfy the query condition.
  - Generally slower than an index seek, especially for large tables.
  - Used when the query retrieves a large portion of the table or when no suitable index exists.
- **Index Seek**:
  - Efficiently retrieves rows from the index based on the indexed column.
  - Generally faster because it directly locates the rows that satisfy the query condition.
  - Used when the query retrieves a small subset of rows based on the index key.

### 59. What is a covering index in SQL Server?
- A covering index is a non-clustered index that includes all the columns referenced in a query, either in the index key or as included columns.
- It can significantly improve query performance by allowing the database engine to retrieve all necessary data from the index without accessing the base table.
- Covering indexes reduce I/O operations and improve query efficiency.
- Example:
  ```sql
  CREATE INDEX idx_covering ON table_name (column1) INCLUDE (column2, column3);
  ```

### 60. What is database normalization, and why is it important?
- Database normalization is the process of organizing data to reduce redundancy and improve data integrity.
- It involves dividing tables into smaller, related tables and defining relationships between them.
- Normalization ensures data consistency, minimizes duplication, and simplifies data maintenance.
- Normalized databases are easier to query, update, and maintain, reducing the risk of data anomalies and improving overall database performance.

### 61. What is denormalization, and why would you use it?
- Denormalization is the process of combining normalized tables to improve read performance and simplify queries.
- It involves adding redundant data to reduce the number of joins required to retrieve related data.
- Denormalization is used when read performance is a higher priority than data redundancy, such as in reporting systems and data warehouses.
- While denormalization can improve query performance, it can also complicate data maintenance and increase the risk of data anomalies.

### 62. What is a schema in SQL Server?
- A schema is a logical container for database objects such as tables, views, stored procedures, and functions.
- It helps organize and manage database objects, providing a way to group related objects together.
- Schemas improve security by allowing you to define permissions at the schema level, controlling access to the contained objects.
- Example: Creating a schema and a table within it:
  ```sql
  CREATE SCHEMA sales;
  CREATE TABLE sales.customers (ID INT, Name NVARCHAR(100));
  ```

### 63. What is the difference between UNION and UNION ALL in SQL?
- **UNION**:
  - Combines the result sets of two or more SELECT statements.
  - Removes duplicate rows from the combined result set.
  - Performs an implicit DISTINCT operation.
- **UNION ALL**:
  - Combines the result sets of two or more SELECT statements.
  - Includes all rows from the combined result set, including duplicates.
  - Does not perform a DISTINCT operation, making it faster than UNION.

### 64. What is the difference between a primary key and a unique key in SQL Server?
- **Primary Key**:
  - Uniquely identifies each row in a table.
  - Cannot contain NULL values.
  - Each table can have only one primary key.
  - Implicitly creates a clustered index unless specified otherwise.
- **Unique Key**:
  - Ensures that all values in the column(s) are unique.
  - Can contain one NULL value (for a single-column unique key).
  - A table can have multiple unique keys.
  - Typically creates a non-clustered index.

### 65. What is referential integrity in SQL Server?
- Referential integrity ensures that relationships between tables remain consistent.
- It is enforced using foreign keys, which link columns in one table to the primary key or unique key columns in another table.
- Referential integrity prevents orphaned records and maintains data consistency across related tables.
- Cascading actions (CASCADE DELETE and CASCADE UPDATE) can be defined to automatically propagate changes from the parent table to the child table.

### 66. What is a stored procedure in SQL Server, and what are its advantages?
- A stored procedure is a precompiled collection of one or more SQL statements that can be executed as a single unit.
- Advantages of stored procedures include:
  - Improved performance due to precompilation.
  - Reduced network traffic by executing multiple statements in a single call.
  - Enhanced security by encapsulating business logic and controlling access to data.
  - Easier maintenance and reusability of code.

### 67. What is a trigger in SQL Server, and what are its types?
- A trigger is a special type of stored procedure that automatically executes in response to certain events on a table or view.
- Types of triggers include:
  - **DML Triggers**: Execute in response to data manipulation events (INSERT, UPDATE, DELETE).
  - **DDL Triggers**: Execute in response to data definition events (CREATE, ALTER, DROP).
  - **Logon Triggers**: Execute in response to logon events.
- Triggers enforce business rules, maintain data integrity, and automate audit tasks.

### 68. What is the purpose of the COALESCE function in SQL Server?
- The COALESCE function returns the first non-null value from a list of expressions.
- It is used to handle null values and provide default values when data is missing.
- COALESCE simplifies conditional logic in queries by avoiding complex CASE expressions.
- Example:
  ```sql
  SELECT COALESCE(column

1, column2, 'default value') AS result FROM table_name;
  ```

### 69. What are the ACID properties in SQL Server, and why are they important?
- ACID properties ensure reliable processing of database transactions.
  - **Atomicity**: Ensures that a transaction is all-or-nothing; it is fully completed or fully rolled back.
  - **Consistency**: Ensures that a transaction brings the database from one valid state to another, maintaining data integrity.
  - **Isolation**: Ensures that transactions are executed in isolation, preventing concurrent transactions from interfering with each other.
  - **Durability**: Ensures that once a transaction is committed, its changes are permanently saved, even in the event of a system failure.
- ACID properties are crucial for maintaining data reliability, consistency, and integrity in multi-user environments.

### 70. What is a view in SQL Server, and how does it differ from a table?
- A view is a virtual table that provides a specific representation of data from one or more tables.
- Views do not store data themselves but retrieve data dynamically when queried.
- Views can simplify complex queries, provide a level of abstraction, and enhance security by restricting access to specific data.
- Unlike tables, views cannot have indexes, constraints, or triggers directly defined on them.

### 71. What is a common table expression (CTE) in SQL, and how is it used?
- A CTE is a temporary result set defined within a SELECT, INSERT, UPDATE, or DELETE statement.
- CTEs improve the readability and maintainability of complex queries by breaking them into simpler parts.
- CTEs can be recursive, allowing for operations like hierarchical data retrieval.
- Example:
  ```sql
  WITH CTE AS (
      SELECT column1, column2
      FROM table_name
  )
  SELECT * FROM CTE;
  ```

### 72. What is a cross join in SQL, and how does it work?
- A cross join returns the Cartesian product of two tables, combining all rows from the first table with all rows from the second table.
- Cross joins do not require a join condition and can result in large result sets.
- Example:
  ```sql
  SELECT *
  FROM table1
  CROSS JOIN table2;
  ```

### 73. What is a composite key in SQL Server?
- A composite key is a primary key or unique key that consists of two or more columns.
- Composite keys ensure the uniqueness of rows based on the combination of values in multiple columns.
- They are used when a single column is insufficient to uniquely identify rows.
- Example:
  ```sql
  CREATE TABLE table_name (
      column1 INT,
      column2 INT,
      PRIMARY KEY (column1, column2)
  );
  ```

### 74. What is a clustered index in SQL Server?
- A clustered index determines the physical order of data in a table.
- Each table can have only one clustered index, typically on the primary key.
- The data rows are stored in the order of the clustered index key values.
- Clustered indexes improve query performance for range queries and sorting operations.

### 75. What is a non-clustered index in SQL Server?
- A non-clustered index is a separate structure from the data rows that stores the index key values and pointers to the actual data.
- A table can have multiple non-clustered indexes.
- Non-clustered indexes improve query performance for specific columns frequently used in search conditions.
- Example:
  ```sql
  CREATE INDEX idx_name ON table_name (column_name);
  ```

### 76. What is the difference between DELETE and TRUNCATE commands in SQL Server?
- **DELETE**:
  - Removes rows from a table based on a condition.
  - Can be rolled back if used within a transaction.
  - Triggers and constraints are enforced.
  - Example: `DELETE FROM table_name WHERE condition;`
- **TRUNCATE**:
  - Removes all rows from a table without logging individual row deletions.
  - Cannot be rolled back if not used within a transaction.
  - Triggers are not fired.
  - Resets identity columns.
  - Example: `TRUNCATE TABLE table_name;`

### 77. What is the difference between DROP and TRUNCATE commands in SQL Server?
- **DROP**:
  - Removes an entire database object (e.g., table, view, index) from the database.
  - Cannot be rolled back once executed.
  - Example: `DROP TABLE table_name;`
- **TRUNCATE**:
  - Removes all rows from a table but retains the table structure for future use.
  - Cannot be rolled back if not used within a transaction.
  - Example: `TRUNCATE TABLE table_name;`

### 78. What is a self-join in SQL Server?
- A self-join is a join of a table with itself.
- It is used to compare rows within the same table or retrieve hierarchical data.
- A self-join requires table aliases to distinguish the different instances of the same table.
- Example:
  ```sql
  SELECT A.column1, B.column2
  FROM table_name A
  JOIN table_name B ON A.id = B.parent_id;
  ```

### 79. What is a subquery in SQL, and how is it used?
- A subquery is a query nested within another SQL query.
- Subqueries can return single values, multiple values, or entire result sets.
- They are used in SELECT, INSERT, UPDATE, and DELETE statements for filtering, calculating, or validating data.
- Example:
  ```sql
  SELECT column1
  FROM table_name
  WHERE column2 = (SELECT MAX(column2) FROM table_name);
  ```

### 80. What is the difference between a local temporary table and a global temporary table in SQL Server?
- **Local Temporary Table**:
  - Prefixed with `#`.
  - Visible only to the session that created it.
  - Automatically dropped when the session ends.
  - Example: `CREATE TABLE #temp_table (column1 INT);`
- **Global Temporary Table**:
  - Prefixed with `##`.
  - Visible to all sessions.
  - Dropped when the last session referencing it ends.
  - Example: `CREATE TABLE ##global_temp_table (column1 INT);`

### 81. What are the differences between DDL and DML commands in SQL?
- **DDL (Data Definition Language)**:
  - Used to define, alter, and manage database objects.
  - Includes commands like CREATE, ALTER, DROP, and TRUNCATE.
  - Example: `CREATE TABLE table_name (column1 INT);`
- **DML (Data Manipulation Language)**:
  - Used to manipulate data within database objects.
  - Includes commands like SELECT, INSERT, UPDATE, and DELETE.
  - Example: `INSERT INTO table_name (column1) VALUES (1);`

### 82. What is a correlated subquery in SQL, and how is it different from a regular subquery?
- A correlated subquery is a subquery that references columns from the outer query.
- It is evaluated once for each row processed by the outer query.
- Correlated subqueries are used for row-by-row comparisons and calculations.
- Example:
  ```sql
  SELECT column1
  FROM table_name A
  WHERE EXISTS (
      SELECT 1
      FROM table_name B
      WHERE B.column2 = A.column2
  );
  ```

### 83. What is a derived table in SQL, and how is it used?
- A derived table is a subquery used in the FROM clause of a SQL query.
- It provides a temporary result set that can be queried further.
- Derived tables simplify complex queries by breaking them into manageable parts.
- Example:
  ```sql
  SELECT *
  FROM (
      SELECT column1, column2
      FROM table_name
  ) AS derived_table;
  ```

### 84. What is a scalar function in SQL Server?
- A scalar function is a user-defined function that returns a single value.
- Scalar functions can accept parameters and perform calculations, transformations, or validations.
- They can be used in SELECT, WHERE, and other SQL clauses.
- Example:
  ```sql
  CREATE FUNCTION udf_add (@a INT, @b INT)
  RETURNS INT
  AS
  BEGIN
      RETURN @a + @b;
  END;
  ```

### 85. What is a table-valued function in SQL Server?
- A table-valued function is a user-defined function that returns a table.
- It can be used as a table in SQL queries, providing a dynamic result set.
- Table-valued functions can accept parameters and perform operations like joins, filtering, and aggregations.
- Example:
  ```sql
  CREATE FUNCTION udf_get_table ()
  RETURNS TABLE
  AS
  RETURN (
      SELECT column1, column2
      FROM table_name
  );
  ```

### 86. What is a window function in SQL, and how is it used?
- A window function performs calculations across a set of table rows related to the current row.
- It provides aggregated values without collapsing rows, allowing for more complex analytics.
- Common window functions include ROW_NUMBER(), RANK(), DENSE_RANK(), and aggregate functions with the OVER() clause.
- Example:
  ```sql
  SELECT column1,
         ROW_NUMBER() OVER (PARTITION BY column2 ORDER BY column3) AS row_num
  FROM table_name;
  ```

### 87. What is a pivot table in SQL, and how is it used?
- A pivot table transforms rows into columns, allowing for cross-tabulation of data.
- It is used to aggregate and summarize data for reporting and analysis.
- SQL Server provides

 the PIVOT operator for creating pivot tables.
- Example:
  ```sql
  SELECT *
  FROM (
      SELECT column1, column2, column3
      FROM table_name
  ) AS source_table
  PIVOT (
      SUM(column3)
      FOR column2 IN ([value1], [value2], [value3])
  ) AS pivot_table;
  ```

### 88. What is an unpivot table in SQL, and how is it used?
- An unpivot table transforms columns into rows, reversing the pivot operation.
- It is used to normalize data by converting wide tables into long tables.
- SQL Server provides the UNPIVOT operator for creating unpivot tables.
- Example:
  ```sql
  SELECT column1, column2, column3
  FROM table_name
  UNPIVOT (
      column3 FOR column2 IN (column2_1, column2_2, column2_3)
  ) AS unpivot_table;
  ```

### 89. What is a recursive CTE in SQL Server, and how is it used?
- A recursive CTE is a common table expression that references itself to perform iterative processing.
- It is used for hierarchical data retrieval, such as organizational charts and tree structures.
- Recursive CTEs consist of an anchor member (base query) and a recursive member (iterative query).
- Example:
  ```sql
  WITH RecursiveCTE AS (
      SELECT column1, column2
      FROM table_name
      WHERE condition
      UNION ALL
      SELECT column1, column2
      FROM table_name
      JOIN RecursiveCTE ON table_name.column1 = RecursiveCTE.column2
  )
  SELECT * FROM RecursiveCTE;
  ```

### 90. What is a materialized view in SQL Server, and how is it different from a regular view?
- A materialized view (indexed view) stores the result set of a query physically, improving read performance.
- Unlike regular views, materialized views are refreshed periodically to reflect changes in the base tables.
- They are used for performance optimization, especially in data warehousing and reporting scenarios.
- Example:
  ```sql
  CREATE VIEW materialized_view_name
  WITH SCHEMABINDING
  AS
  SELECT column1, column2, COUNT_BIG(*)
  FROM table_name
  GROUP BY column1, column2;
  CREATE UNIQUE CLUSTERED INDEX idx_materialized_view
  ON materialized_view_name (column1, column2);
  ```

### 91. What is a table variable in SQL Server, and how is it different from a temporary table?
- A table variable is a variable that stores a result set for the duration of a batch or stored procedure.
- It is declared using the `DECLARE` statement and is stored in memory.
- Table variables are less resource-intensive and have a smaller scope than temporary tables.
- Example:
  ```sql
  DECLARE @table_variable TABLE (column1 INT, column2 NVARCHAR(100));
  ```

### 92. What is a data type in SQL, and why is it important?
- A data type defines the kind of data that can be stored in a column or variable.
- It ensures data integrity by restricting the type and format of data values.
- Common data types include INT, VARCHAR, DATE, and FLOAT.
- Proper data type selection improves database performance and storage efficiency.

### 93. What is a constraint in SQL Server, and what types are there?
- A constraint is a rule enforced on data columns to ensure data integrity and consistency.
- Types of constraints include:
  - **Primary Key**: Uniquely identifies each row in a table.
  - **Foreign Key**: Enforces referential integrity between tables.
  - **Unique**: Ensures all values in a column are unique.
  - **Check**: Ensures that all values in a column satisfy a specific condition.
  - **Default**: Provides a default value for a column if no value is specified.
  - **Not Null**: Ensures that a column cannot contain NULL values.

### 94. What is a default constraint in SQL Server, and how is it used?
- A default constraint provides a default value for a column if no value is specified during an insert operation.
- It ensures that columns have a valid value when no explicit value is provided.
- Default constraints are defined using the `DEFAULT` keyword.
- Example:
  ```sql
  CREATE TABLE table_name (
      column1 INT DEFAULT 0,
      column2 NVARCHAR(100) DEFAULT 'N/A'
  );
  ```

### 95. What is a unique constraint in SQL Server, and how is it used?
- A unique constraint ensures that all values in a column or a combination of columns are unique.
- It prevents duplicate values and enforces data integrity.
- Unique constraints can be defined using the `UNIQUE` keyword.
- Example:
  ```sql
  CREATE TABLE table_name (
      column1 INT,
      column2 NVARCHAR(100),
      UNIQUE (column1, column2)
  );
  ```

### 96. What is the difference between a primary key constraint and a unique constraint in SQL Server?
- **Primary Key Constraint**:
  - Ensures that each row in a table is uniquely identified.
  - Cannot contain NULL values.
  - Each table can have only one primary key.
  - Implicitly creates a clustered index unless specified otherwise.
- **Unique Constraint**:
  - Ensures that all values in the column(s) are unique.
  - Can contain one NULL value (for a single-column unique key).
  - A table can have multiple unique constraints.
  - Typically creates a non-clustered index.

### 97. What is a foreign key constraint in SQL Server?
- A foreign key constraint enforces referential integrity between tables by linking columns in one table to the primary key or unique key columns in another table.
- It ensures that the values in the foreign key column(s) match values in the referenced primary or unique key column(s).
- Foreign key constraints prevent orphaned records and maintain data consistency across related tables.
- Example:
  ```sql
  CREATE TABLE child_table (
      child_id INT,
      parent_id INT,
      FOREIGN KEY (parent_id) REFERENCES parent_table(parent_id)
  );
  ```

### 98. What is the difference between a clustered index and a non-clustered index in SQL Server?
- **Clustered Index**:
  - Determines the physical order of data in a table.
  - Each table can have only one clustered index.
  - Data rows are stored in the order of the clustered index key values.
  - Improves query performance for range queries and sorting operations.
- **Non-Clustered Index**:
  - A separate structure from the data rows that stores the index key values and pointers to the actual data.
  - A table can have multiple non-clustered indexes.
  - Improves query performance for specific columns frequently used in search conditions.

### 99. What is the difference between a view and a materialized view in SQL Server?
- **View**:
  - A virtual table that provides a specific representation of data from one or more tables.
  - Does not store data itself; retrieves data dynamically when queried.
  - Simplifies complex queries, provides abstraction, and enhances security.
- **Materialized View (Indexed View)**:
  - Stores the result set of a query physically, improving read performance.
  - Requires periodic refreshes to reflect changes in the base tables.
  - Used for performance optimization, especially in data warehousing and reporting scenarios.

### 100. What is the difference between a scalar function and a table-valued function in SQL Server?
- **Scalar Function**:
  - Returns a single value.
  - Can accept parameters and perform calculations, transformations, or validations.
  - Can be used in SELECT, WHERE, and other SQL clauses.
  - Example: 
    ```sql
    CREATE FUNCTION udf_add (@a INT, @b INT)
    RETURNS INT
    AS
    BEGIN
        RETURN @a + @b;
    END;
    ```
- **Table-Valued Function**:
  - Returns a table.
  - Can accept parameters and perform operations like joins, filtering, and aggregations.
  - Can be used as a table in SQL queries, providing a dynamic result set.
  - Example:
    ```sql
    CREATE FUNCTION udf_get_table ()
    RETURNS TABLE
    AS
    RETURN (
        SELECT column1, column2
        FROM table_name
    );
    ```
