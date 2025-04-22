# Finals Task 3 - Table Manipulation

## Task 1 - Query Statements

SELECT * FROM products_tbl;

DESCRIBE products_tbl;

## Task 2 - Table Structure

CREATE DATABASE products_db;
USE products_db;

CREATE TABLE products_tbl (
    id INT AUTO_INCREMENT PRIMARY KEY,
    product_name VARCHAR(100) NOT NULL,
    price DECIMAL(10, 2)
);

ALTER TABLE products_tbl
ADD CONSTRAINT chk_price CHECK (price > 0);

INSERT INTO products_tbl (product_name, price)
VALUES
    ('Laptop', 999.99),
    ('Smartphone', 599.99),
    ('Tablet', 299.99),
    ('Keyboard', 19.99),
    ('Mouse', 14.99),
    ('Desk Lamp', 24.99),
    ('Speakers', 9.99);

ALTER TABLE products_tbl
MODIFY COLUMN product_name VARCHAR(120) NOT NULL;

## Task 3 - ER Diagram or Relational Schema from phpMyAdmin or Workbench

<img src="Images/FT2%20ERD.jpg" alt="Alt Text" width="800" height="400"> 

## Task 4 - SQL Copy of the Database and Table Structures

[Raw Copy of MySQL File](https://github.com/NaythanIsME/EDM-Portfolio/blob/main/Finals%20Task%202/Files/Naythan.sql)

CREATE DATABASE products_db;
USE products_db;

CREATE TABLE products_tbl (
    id INT AUTO_INCREMENT PRIMARY KEY,
    product_name VARCHAR(100) NOT NULL,
    price DECIMAL(10, 2)
);

ALTER TABLE products_tbl
ADD CONSTRAINT chk_price CHECK (price > 0);

INSERT INTO products_tbl (product_name, price)
VALUES
    ('Laptop', 999.99),
    ('Smartphone', 599.99),
    ('Tablet', 299.99),
    ('Keyboard', 19.99),
    ('Mouse', 14.99),
    ('Desk Lamp', 24.99),
    ('Speakers', 9.99);

ALTER TABLE products_tbl
MODIFY COLUMN product_name VARCHAR(120) NOT NULL;

SELECT * FROM products_tbl;

DESCRIBE products_tbl;
