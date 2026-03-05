# Beginner’s Guide to Writing Your First SQL Query

## What is SQL?

SQL, Structured Query Language, is the standard language for accessing and manipulaing databases. It can store, retrieve, update, and manage data in a database using simple commands. 

SQL is often used in contexts where huge amounts of data need to be processed fast, such as e-commerce to manage customer orders, healthcare to maintain patient records, banking to analyse transaction history, and more. 

## Rules for Writing Queries
- End every SQL statement with a semicolon (;) to tell the computer the statement has ended
- Certain words, like SELECT or INSERT, are reserved for commands and should not be used for naming
- To write a comment (text SQL won't try to run), use -- at the start of a single-line comment, or /* comment here **/ for a multi-line comment
- SQL is case-insensitive, but it is best practice to capitalize keywords for readability
- Similarly, SQL does not care about extra spaces, so using new lines for new commands make it more readable

## How to Write your First Query (SELECT)

Your database will be populated with *tables* that contain your data. SELECT is the keyword that you use to look at some or all of that data. The general format of a SELECT statement is

  `SELECT * FROM table_name;`

The * indicates that you want to see the entire table all at once. You can also pick only one column to view:

  `SELECT column_name FROM table_name;`

or a list of columns like this:

  `SELECT col1, col2, col3 FROM table_name;`

This is often better than using * because large tables will make your query run slower. 

## SELECT example

Let's run some SELECT statements on a table of simulated employee data, aptly named employee_data, that could be in your database.

To see the whole table (only if it's small!), you run:

`SELECT * FROM employee_data;`

and the output looks like this:

| ID      | Name      | Department      | Salary      |
| ------------- | ------------- |------------- | ------------- |
| 1 | Jessie | IT | 90000 |
| 2 | James | Finance | 80000 |

Let's say you're doing some analysis on employee salaries. To see just the salaries, you run:

`SELECT salary FROM employee_data;`

and the output you see is this:

| Salary      | 
| ------------- | 
| 90000 | 
| 80000 | 

Let's say you want to compare salaries by department, you can run:

`SELECT department, salary FROM employee_data;`

and the output will look like this:

| Department      | Salary      | 
| ------------- | ------------- | 
| IT | 90000 | 
| Finance | 80000 | 

That's how you use SELECT to view data in a table!

