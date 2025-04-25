# Finals Lab Task 1 - Events Management Database (Naythan_DB)

## Overview

This project involves creating a database for managing events, attendees, and sponsors, following the requirements of the task. The database **Naythan_DB** contains multiple tables and relationships, aimed at tracking event details, attendee participation, and event sponsorship.

## Project Components

### Step 1: Database Structure

The database consists of the following tables:

1. **events_tbl**: Holds events with an `event_id` as the primary key and `event_name`.
2. **attendees_tbl**: Contains attendees with an `attendee_id` as the primary key and `attendee_name`.
3. **events_attendees_tbl**: Links events and attendees in a many-to-many relationship, using `event_id` and `attendee_id` as foreign keys.
4. **event_sponsors_tbl**: Connects sponsors to events, using `event_id` and `sponsor_name`.

### Step 2: Table Design and Output

Here is the output of the tables in the **Naythan_DB** database:

![Tables Output](Images/TABLES.jpg)

### Step 3: Entity Relationship Diagram (ERD)

Below is the ERD showing the relationships between the tables:

![ERD](Images/ERD.jpg)

## Raw Files

The following raw files are available for download:

1. [SQL Script](https://github.com/NaythanIsME/EDM-Portfolio/blob/main/Finals%20Task%201/Files/naytheen.sql) - The SQL script to create the database and tables.
2. [ERD File](https://github.com/NaythanIsME/EDM-Portfolio/blob/main/Finals%20Task%201/Files/naythan.mwb) - The raw ERD file for visual representation of the database.

## Database Creation SQL Script

```sql
CREATE DATABASE IF NOT EXISTS Naythan_DB;
USE Naythan_DB;

CREATE TABLE IF NOT EXISTS events_tbl (
  event_id INT AUTO_INCREMENT PRIMARY KEY,
  event_name VARCHAR(255) NOT NULL
);

CREATE TABLE IF NOT EXISTS attendees_tbl (
  attendee_id INT AUTO_INCREMENT PRIMARY KEY,
  attendee_name VARCHAR(255) NOT NULL
);

CREATE TABLE IF NOT EXISTS events_attendees_tbl (
  event_id INT,
  attendee_id INT,
  PRIMARY KEY (event_id, attendee_id),
  FOREIGN KEY (event_id) REFERENCES events_tbl(event_id),
  FOREIGN KEY (attendee_id) REFERENCES attendees_tbl(attendee_id)
);

CREATE TABLE IF NOT EXISTS event_sponsors_tbl (
  event_id INT,
  sponsor_name VARCHAR(255) NOT NULL,
  PRIMARY KEY (event_id, sponsor_name),
  FOREIGN KEY (event_id) REFERENCES events_tbl(event_id)
);
