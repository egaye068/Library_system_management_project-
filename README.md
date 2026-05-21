# Library_System_Management_Using_SQL_Project 

## Project Overview 

-**Project Titel**: Library management system     
-**Level**: Beginner 

This project demonstrates the implementation of a Library Management System using SQL. It includes creating and managing tables, performing CRUD operations, and executing advanced SQL queries. The goal is to showcase skills in database design, manipulation, and querying.

<img width="1402" height="1122" alt="Image" src="https://github.com/user-attachments/assets/4a6ad0d4-4650-4fcb-951c-1a92e2bee210" />

## Objective 

1. **Set up the Library Management System Database**: Create and populate the database with tables for branches, employees, members, books, issued status, and return status.  
2. **CRUD Operations**: Perform Create, Read, Update, and Delete operations on the data.  
3. **CTAS (Create Table As Select)**: Utilize CTAS to create new tables based on query results.  

## Project Structure 

1. ### Database Setup**
<img width="882" height="547" alt="Image 2" src="https://github.com/user-attachments/assets/de275a68-7e9d-409c-9787-2cbba9d6b487" />

- **Database Creation**: Create database named Library_system_management_project  
- **Table Creation**: Created tables for branches, employees, members, books, issued status, and return status. Each table includes relevant columns and relationships.

```sql
CREATE DATABASE library_project_2;
```
```sql
DROP TABLE IF EXISTS branch 
CREATE TABLE branch (
	branch_id	VARCHAR (20) PRIMARY KEY, 
	manager_id	VARCHAR (20),
	branch_address	VARCHAR (20),
	contact_no VARCHAR (20)
);
```
```sql
DROP TABLE IF EXISTS employees 
CREATE TABLE employees (
	emp_id	VARCHAR(20) PRIMARY KEY,
	emp_name	VARCHAR(30),
	position	VARCHAR(30),
	salary	INT,
	branch_id VARCHAR (20) 
);
```
```sql
DROP TABLE IF EXISTS members 
CREATE TABLE members (
	member_id	VARCHAR(20) PRIMARY KEY,
    member_name	VARCHAR(20),
    member_address	VARCHAR(20),
    reg_date DATE 
);
```
```sql
DROP TABLE IF EXISTS books 
CREATE TABLE books (
	isbn	VARCHAR(50) PRIMARY KEY ,
    book_title	VARCHAR(100),
    category	 VARCHAR(30),
    rental_price	FLOAT,
    status	VARCHAR (20),
    author VARCHAR (50),
	publisher VARCHAR (70) 
);
```
```sql
DROP TABLE IF EXISTS issued_status 
CREATE TABLE issued_status (
	issued_id	VARCHAR(20) PRIMARY KEY, 
	issued_member_id	VARCHAR(20), 
	issued_book_name VARCHAR(100),
	issued_date	 DATE,
	issued_book_isbn	VARCHAR(30), 
	issued_emp_id VARCHAR(20) 
	);
```
```sql
DROP TABLE IF EXISTS return_status 
CREATE TABLE return_status (
	return_id	VARCHAR(20) PRIMARY KEY,
	issued_id	VARCHAR(20),
	return_book_name	VARCHAR(100),
	return_date	DATE,
	return_book_isbn VARCHAR(20)
);
```

2. ### CRUD Operations

- **Create**: Inserted sample records into the books table.
- **Read**: Retrieved and displayed data from various tables.
- **Update**: Updated records in the employees table.
- **Delete**: Removed records from the members table as needed.
