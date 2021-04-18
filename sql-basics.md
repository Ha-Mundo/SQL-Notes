# SQL basics

## 1. SQL

- SQL is a language used for interacting with Relational Database Management Systems
  - You can use SQL to get the RDBMS to do things for you.
    - Create, retrieve, update and delete data
    - Create and manage databases
    - Design and create database tables
    - Perform administration tasks(security, user management, import/export ect)
- SQL implementations vary between systems. ( just little tweak?)

  - not all RDBMS follow the SQL standard to a 'T'
  - The concepts are the same but the implementation may vary

- SQL is actually a hybrid language, it's basically 4 types of languages in one :
  - Data Query Language (DQL)
    - User to query the database for information.
    - Get information that is already stored there.
  - Data Definition Language (DDL)
    - Used for defining database schemas.
  - Data Control Language (DCL)
    - Used for controlling access to the data in the database.
    - User and Permissions management
  - Data Manipulation Language(DML)
    - Used for inserting, updating and deleting data from the database.

## 2. Queries

- A query is a set of instructions given to the RDBMS that tell the RDBMS what information you want it to retrieve for you.
  - TONS of data in a DB
  - Often hidden a complex schema
  - Goal is to only get the data you need.

## 3. Table and Keys examples

- primary key - unique attribute
- define table
- surrogate key - not mapping anything in real word data// it is one kind of primary key
- natural key - social security number as primary key of table -- // key has mapping or purpose in real world
- foreign key - attribute that we can store on database table that link us another table
  its gonna be primary key in different table and use another table
  ( we can define relationship with different tables)
- composite key // key need two attribute //only together they can be unique not one each
- composite key// both can be foreign key and both of them make it together unique

## 4. Creating tables

_Schema_
always to create table is staring point
_data type_

- INT : whole number (integer)
- DECIMAL(M, N) : exact value
- VARCHAR(1) :string of text of length1
- BLOB : Binary Large Object, Stores large data
- Date : yyyy-mm-dd
- TIMESTAMP : yyyy-mm-dd hh:mm:ss

_Creating tables_

      CREATE TABLE student (
          student_id INT PRIMARY KEY,
          name VARCHAR(40),
          major VARCHAR(40)

          -- PRIMARY KEY(student_id) <--comment
        );

_General Queries_

    DESCRIBE student;
    DROP TABLE student;
    ALTER TABLE student ADD gpa DECIMAL;
    ALTER TABLE student DROP COLUMN gpa;

## 5. Inserting Data

    INSERT INTO student VALUES(1, 'Jack', 'Biology');
    INSERT INTO student VALUES(2, 'Kate', 'Sociology');
    INSERT INTO student(student_id, name) VALUES(3, 'Claire');
    INSERT INTO student VALUES(4, 'Jack', 'Biology');
    INSERT INTO student VALUES(5, 'Mike', 'Computer Science');

## 6. Constraints

    CREATE TABLE student (
      student_id INT PRIMARY KEY AUTO_INCREMENT,
      name VARCHAR(40) NOT NULL,
      -- name VARCHAR(40) UNIQUE,
      major VARCHAR(40) DEFAULT 'undecided',
    );

## 7. Update & Delete

    DELETE FROM student;

    DELETE FROM student
    WHERE student_id = 4;

    DELETE FROM student
    WHERE major = 'Sociology' AND name = 'Kate';

    UPDATE student
    SET major = 'Undecided';

    UPDATE student
    SET name = 'Johnny'
    WHERE student_id = 4;

    UPDATE student
    SET major = 'Biological Sciences'
    WHERE major = 'Biology';

    UPDATE student
    SET major = 'Biosociology'
    WHERE major = 'Biology' OR major = 'sociology'

    UPDATE student
    SET major = 'Undecided', name = 'Tom'
    WHERE student_id = 4;

## 8. Basic Queries

    SELECT *
    FROM student;

    SELECT student.name, student.major
    FROM student;

    SELECT *
    FROM student
    WHERE name = 'Jack';

    SELECT *
    FROM student
    WHERE student_id > 2;

    SELECT *
    FROM student
    WHERE major = 'Biology' AND student_id > 1;
