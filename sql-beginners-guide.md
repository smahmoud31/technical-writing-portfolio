# Beginner’s Guide to Writing Your First SQL Query

This guide introduces the basics of SQL queries and shows how to retrieve data from a database using the `SELECT` statement.

## Prerequisites
- A SQL database (MySQL, PostgreSQL, SQLite)
- A SQL client or terminal
- A table to query

## What is SQL?

SQL (Structured Query Language) is the standard language used to access and manipulate data in relational databases. SQL allows you to store, retrieve, update, and manage data in a database using structured commands called queries.

SQL is commonly used in applications that manage large amounts of data, such as e-commerce systems, healthcare records, and financial transaction systems.

## Rules for Writing Queries
- SQL statements end with a semicolon (;) to tell the computer the statement has ended
- Certain words, such as `SELECT` or `INSERT`, are reserved keywords and should not be used for table or column names
- To write a comment (text SQL won't try to run), use -- at the start of a single-line comment, or /* comment here */ for a multi-line comment
- SQL keywords are case-insensitive, but it is best practice to capitalize keywords for readability
- Similarly, SQL does not care about extra spaces, so formatting queries across multiple lines improves readability

## How to Write Your First Query (SELECT)

A database stores data in tables. A table is similar to a spreadsheet:
- Each row represents a record
- Each column represents a type of data

 `SELECT` is the keyword that you use to look at some or all of that data. The general format of a `SELECT` statement is:

  `SELECT * FROM table_name;`

The * retrieves every column from the table. You can also pick only one column to view:

  `SELECT column_name 
  FROM table_name;`

or a list of columns like this:

  `SELECT col1, 
  col2, 
  col3 
  FROM table_name;`

This is often better than using * because retrieving every column from a large table can return more data than necessary and slow down queries. 

## SELECT example

Let's run some `SELECT` statements on a table of simulated employee data, named `employee_data`, that could be in your database.

If the table is small, you can view all rows by running:

`SELECT * FROM employee_data;`

which returns the following output:

| ID      | Name      | Department      | Salary      |
| ------------- | ------------- |------------- | ------------- |
| 1 | Jessie | IT | 90000 |
| 2 | James | Finance | 80000 |

Each row represents an employee. A data analyst might use `employee_data` to perform analysis on employee salaries. To see the salaries only, run:

  `SELECT salary 
  FROM employee_data;`

which returns the following output:

| Salary      | 
| ------------- | 
| 90000 | 
| 80000 | 

Each row is a different employee's salary. To compare salaries by department, run:

  `SELECT 
  department, 
  salary 
  FROM employee_data;`

which returns the following output:

| Department      | Salary      | 
| ------------- | ------------- | 
| IT | 90000 | 
| Finance | 80000 | 

The query returns two columns: department and salary. Each row will have one employee's department and salary. 

## This guide introduced:
- What SQL is
- How to use `SELECT` to retrieve data from a table

## Next Steps:
- Filter results using WHERE
- Sort results using ORDER BY
- Summarize data using GROUP BY
- Combine tables using JOIN

You can learn these queries in this blog post: 
[https://learnsql.com/blog/sql-101/](https://learnsql.com/blog/sql-101/)
which also discusses what a relational database is and why we use it.

### Other Resources

A 2 page cheat-sheet with download links (I reccommend printing this to have next to your computer):
[https://learnsql.com/blog/sql-basics-cheat-sheet/](https://learnsql.com/blog/sql-basics-cheat-sheet/)

A clear and comprehensive guide to most SQL queries you'll need:
[https://www.sqltutorial.org](https://www.sqltutorial.org)

### Questions? 
Contact me: smahmoudprofessional@gmail.com

