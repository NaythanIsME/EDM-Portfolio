## Midterm Lab Task 2 – Data Cleaning and Transformation Using Power Query Editor
For this task, we are provided with an Uncleaned_DS_jobs.csv dataset (from Kaggle) and tasked with performing data cleaning and transformation using Power Query Editor in Excel to generate meaningful insights.
## STEP 1 – Data Cleaning Process
- Load the raw file
- Fit Column and row width and height
- TRIM extra spaces
- Remove NULL values
- Remove Duplicates
## STEP 2 – Data Transformation
1. Salary Estimate Column:

 - In Power Query, select the Salary Estimate column.
 - Use Transform > Extract > Text Before Delimiter to remove any characters after the open parenthesis.

2. Create Min and Max Salary Columns:

 - Use Add Column > Column from Examples to generate the Min Sal and Max Sal columns from the Salary Estimate column.
   
3. Add Role Type Column.

 - Go to Add Column > Custom Column and use the formula to categorize job titles into roles like Data Scientist, Data Analyst, Data Engineer, etc.
   
4. Split Location Column:
 - Select the Location column and use Transform > Split Column by Delimiter (Comma) to split location into separate columns.
   
5. Location Correction:
 - Create a custom column to correct location values, replacing certain locations (e.g., "New Jersey" to ", NJ", "California" to ", CA").
   
6. Handle Negative Values:

 - Filter out negative values in Competitors and Industry columns.
   
7. Clean Company Name:
 - Remove any unwanted text from the Company Name column using Transform > Replace Values or Remove Text.
## STEP 3 – Screenshots

Before Data Cleaning:
(See screenshot of raw data before any transformations were made.)

<img src="Images/Uncleaned_data.jpg" alt="Alt Text" width="400" height="300"> 

[*Here's the raw file*](Certificate/Partner-_CLA_-_Programming_Essentials_in_C_certificate_nlimiac24-0228-cca-edu-ph_937351ad-c137-4407-9169-5046bf2376d6.pdf)


After Data Cleaning:
(See screenshot of cleaned data post-transformation.)
<img src="Images/Uncleaned_data.jpg" alt="Alt Text" width="400" height="300"> 

## STEP 4 – Final Output Queries
Here are the final queries after performing all necessary data transformations:

Sal By Role Type dup: A query with job titles categorized by role type.

Sal By Size ref: A query focusing on salary data by company size or another metric.

Sal By State ref: A query analyzing salary data by state/location.

Uncleaned DS Jobs: The original dataset before any transformations.

## Physical Data Model
(Insert physical data model screenshot here)
