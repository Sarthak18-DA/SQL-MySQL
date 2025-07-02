# SQL-MySQL
Learning MySQL by practicing key SQL concepts and queries. Documenting what I’ve learned so far and tracking my current progress through hands-on examples and exercises.


## Section 1 : Getting Started
# What is Databases
A database is an organized collection of data that is stored and accessed electronically.

# What is Database Management Systems (DBMS)
A Database Management System (DBMS) is software that helps you create, manage, and interact with databases.

# SQL VS MySQL

* **SQL** is a language we used to talked with **Database** called as **Structured Query Language**
* **MySQL** is a **database management system** which we used to store **data/databases**

# Some Database Management systems
* MySQL
* PostgreSQL
* SQLite
* Oracle
* Many More

- There are slight differences in syntax of databases


## Section 2: Creating Databses & Tables

# Creating Databases
Firstly we need to check in command prompt to check if the MySQL latest version is perfectly installed or not.

### ✅ Steps to Start MySQL on Windows

```
1. Check if MySQL is installed  
   mysql --version

2. Login to MySQL as root user  
   mysql -u root -p

3. Enter your MySQL root password  
   (It won’t be visible as you type)

4. If the prompt shows `mysql>`, you are ready to run SQL commands!
```

## CODE: Showing Databases
To list available databases:

show databases;

Now coming to our motive of creating databases
- **Note** - This databases will be empty; We are not adding any data in it for now
Our First Database

1. CREATE DATABASE pet_shop;
2.  create database SlimeStore; --- you can type in uppercase and lowercase as well

Till now we have created databases in command prompt/ Terminal

### MySQL Workbench
Now we are going to create databases in our workbench

# CREATE DATABASE 
CODE: Creating Databases
The general command for creating a database:

CREATE DATABASE <database_name>;

A specific example:

CREATE DATABASE soap_store;

-----------------------------------------------------------------------------------------

## Drop Databases

DROP DATABASE SlimeStore;

> ⚠️ **Note:**  
> It's not a common practice to drop databases casually, as they may contain important data.  
> Always back up your database before running destructive commands like `DROP DATABASE`.

## How to use database or select it as a default schema

USE chicken_coop --- The query to use a database


* How to know on which database we are working on 

SELECT DATABASE();  --- It will show you the default database you are using


## CODE: Dropping and Using Databases
To drop a database:

DROP DATABASE <database-name>;

To use a database:

USE <database-name>;

---

# Introducing Tables

Databases consist of bunch of tables
A collection of related data held in structured format within a database

## Tables - Data Types: The Basics

1. Numeric Types
2. String Types
3. DateTime Types

    See More... https://dev.mysql.com/doc/refman/8.4/en/data-types.html

## Creating Tables

CODE: Creating Tables
Creating Tables:

CREATE TABLE cats (
    name VARCHAR(50),
    age INT
);
 
CREATE TABLE dogs (
    name VARCHAR(50),
    breed VARCHAR(50),
    age INT
);

---

## How do we know it worked

SHOW tables;
SHOW COLUMNS FROM cats;
DESC cats;

---

# Deleting Tables
## CODE: Dropping Tables
To drop a table:

DROP TABLE <table-name>;

To specifically drop the cats table:

DROP TABLE cats;

---

# Tables Basics Activity
Create the table:

CREATE TABLE pastries
  (
    name VARCHAR(50),
    quantity INT
  );
View tables:

SHOW TABLES;

View details of pastries table:

DESC pastries;

Delete the whole pastries table:

DROP TABLE pastries;

---

## Section 3
# MySQL Comments

-- Sql comments with (--)

---

# Insert - The Basics

CODE: INSERT: The Basics
-- Re-create the cats table (I dropped it in a previous section)



CREATE TABLE cats (
    name VARCHAR(50),
    age INT
);


Insert a cat:

INSERT INTO cats (name, age) 
VALUES ('Samson', 4);
And another:

INSERT INTO cats (name, age) 
VALUES ('cariona', 2);

## How do we know that it worked

CODE: A Quick Preview of SELECT
To view all rows in our table:

SELECT * FROM cats;

---

## Multi_Inserts

CODE: Multi-inserts

-- Multiple Insert:

INSERT INTO cats (name, age) 
VALUES 
  ('kamla', 5), 
  ('dolly', 1), 
  ('Sively', 15);

