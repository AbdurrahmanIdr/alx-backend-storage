# 0x00. MySQL Advanced

## Description

This project focuses on advanced MySQL concepts including creating tables with constraints, optimizing queries using indexes, implementing stored procedures, functions, views, and triggers. These skills are essential for efficient database management and ensuring data integrity.

## Learning Objectives

By the end of this project, you should be able to:

- Create tables with constraints.
- Optimize queries by adding indexes.
- Implement stored procedures and functions in MySQL.
- Implement views in MySQL.
- Implement triggers in MySQL.

## Requirements

- All files will be executed on Ubuntu 18.04 LTS using MySQL 5.7 (version 5.7.30).
- All files should end with a new line.
- All SQL queries should have a comment just before.
- All files should start with a comment describing the task.
- All SQL keywords should be in uppercase.
- A `README.md` file at the root of the folder of the project is mandatory.
- The length of your files will be tested using `wc`.

## Resources

- [MySQL cheatsheet](https://devhints.io/mysql)
- [MySQL Performance: How To Leverage MySQL Database Indexing](https://www.eversql.com/mysql-index-guide/)
- [Stored Procedure](https://dev.mysql.com/doc/refman/5.7/en/stored-programs-defining.html)
- [Triggers](https://dev.mysql.com/doc/refman/5.7/en/triggers.html)
- [Views](https://dev.mysql.com/doc/refman/5.7/en/views.html)
- [Functions and Operators](https://dev.mysql.com/doc/refman/5.7/en/functions.html)
- [Trigger Syntax and Examples](https://dev.mysql.com/doc/refman/5.7/en/trigger-syntax.html)
- [CREATE TABLE Statement](https://dev.mysql.com/doc/refman/5.7/en/create-table.html)
- [CREATE PROCEDURE and CREATE FUNCTION Statements](https://dev.mysql.com/doc/refman/5.7/en/create-procedure.html)
- [CREATE INDEX Statement](https://dev.mysql.com/doc/refman/5.7/en/create-index.html)
- [CREATE VIEW Statement](https://dev.mysql.com/doc/refman/5.7/en/create-view.html)

## Project Structure

```.
0x00-MySQL_Advanced/
├── 0-uniq_users.sql
├── 1-country_users.sql
├── 2-fans.sql
├── 3-glam_rock.sql
├── 4-store.sql
├── 5-valid_email.sql
├── 6-bonus.sql
├── 7-average_score.sql
├── 8-index_my_names.sql
├── README.md
```

## How to Use

1. Start MySQL service: `service mysql start`
2. Execute scripts: `cat script_name.sql | mysql -uroot -p database_name`

## Author

- [Abdurrahman Idirs](abdurrahmaneedrees@gmail.com)
