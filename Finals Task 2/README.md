# Finals Lab Task 1 - Events Management DB

## Task 2 - Table Structure 
CREATE DATABASE student_assignment_db;
USE student_assignment_db;

CREATE TABLE student_tb (
username VARCHAR(50) PRIMARY KEY
);

CREATE TABLE assignment_tb (
shortname VARCHAR(50) PRIMARY KEY,
due_date DATE NOT NULL,
url VARCHAR(255) DEFAULT NULL
);

CREATE TABLE submission_tb (
username VARCHAR(50),
shortname VARCHAR(50),
version INT,
submit_date DATE NOT NULL,
data TEXT,

    PRIMARY KEY (username, shortname, version),
    
    FOREIGN KEY (username) REFERENCES student_tb(username)
        ON DELETE CASCADE ON UPDATE CASCADE,

    FOREIGN KEY (shortname) REFERENCES assignment_tb(shortname)
        ON DELETE CASCADE ON UPDATE CASCADE
);

## Task 3 -  ER Diagram or Relational schema from phpMyAdmin or Workbench

<img src="Images/FT2%20ERD.jpg" alt="Alt Text" width="1000" height="300"> 
