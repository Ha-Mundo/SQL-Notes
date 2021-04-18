 <old note>

# SQL

to talk with data base

relational / non relational

- SQL-relational = -mysql, postgresql, sqlite

- nonSQL = mongoDB, firebase, DynamoDB, couchDB

industry standard

# understanding

looks like excel
ex select email from students
ex select email from students where age>21
ex select email from students where email like "%naver.com"

# ORM

python ->(orm)->SQL

node.js->(orm)->SQL

problem happen when orm not working!

# What is Database(DB)?

### 1.

- Any collection of related information

  - Phone Book
  - Shopping list
  - Todo list
  - Your 5 best friends
  - Facebook's User Base

- Databases can be stored in different ways

  - On paper
  - In your mind
  - On a computer
  - This powerpoint
  - Comments section

### 2.

- Computers + Database = <3

  - Amazon.com

    - Keeps track of Products, Reviews, Purchase Orders, Credit Cards, Users, Media etc
    - Trillions of pieces of information need to be stored and readily available
    - Information is extremely valuable and critical to Amazon's functioning.
    - Security is peoples personal information(Credit cards, SSN, Address, Phone)
    - Information is stored on a computer

  - vs Shopping List
    - Keeps track of consumer products that need to be purchased
    - 10-20 pieces of information need to be stored and readily available
    - information is for convenience sake only and not necessary for shopping
    - Security is not important
    - information is stored on a piece of paper or even just in someones memory

### 3.

- Database Management Systems (DBMS)
  - A special software program that helps users create and maintain a database.
    - Makes it easy to manage large amounts of information
    - Handles Security
    - Backups
    - Importing/ exporting data
    - Concurrency
    - Interacts with software applications

### 4.

Amazon Database Diagram

- Amazon will interact with the DBMS in order to create, read, update and delete info

### 5. CRUD

- DBMS is able to do CRUD

### 6. Two types of Databases

- Relational Databases(SQL) sequel
  - Organize data into one or more tables
    - Each table had columns and rows
    - A unique key identifies each row
- Non-Relational (noSQL / not just SQL) (very general)
  - Organize data is anything but a traditional table
    - Key-value stores
    - Documents(JSON, XML, etc)
    - Graphs
    - Flexible Tables

### 7. SQL

- actual table

- Relational Database Management Systems(RDBMS)

  - Help users create and maintain a relational database
    - mySQL, Oracle, postgresSQL, mariaDB etc

- Structured Query Language(SQL)
  - Standardized language for interacting with RDBMS.
  - Used to perform C.R.U.D operations, as well as other administrative tasks (user management, security, backup etc)
  - Used to define tables and structures
  - SQL code used on one RDBMS is not always portable to another without modification

### 8. noSQL

- Non-Relational Database Management Systems(NRDBMS)
  - Help users create and maintain a non-relational database
    - mongoDB, dynamoDB, apache cassandra, firebase etc
- Implementation specific
  - Any non relational database falls under this category, so there is no set language standard
  - Most NRDBMS will implement their own language for performing C.R.U.D and administrative operations on the database

### 9. Database Queries

- Queries are requests made to the database management system for specific information
- As the database's structure become more and more complex, it becomes more difficult to get the specific pieces of information we want.
- A google search is a query.

### 10. Wrap up

- Database is any collection of related information.
- Computer are great for storing databases
- Database Management Systems (DBMS) make it easy to create, maintain and secure a database.
- DBMS allow you to perform the C.R.U.D operations and other tasks
- Two type of Databases
- Relational databases use SQL and store data in tables with rows and columns
- Non Relational data store data using other data structures
