# Pewlett-Hackard-Analysis

# Project Overview

-To determine who is retiring for PH 
-To determine how many individuals would be retiring 

# Resources
- CSV Data Source:, departments, dept_emp, dept_manager, employees, salaries and titles
- Software: PostgreSQL and pgAdmin
- Website: QuickDBD.com

# Objectives
- First Design an ERD using the QuickDBD website
- Create an SQL Schema
- Import CSV into Postgre/pgAdmin
- Create Tables and Joins SQL tables

# Challenge Overview
- In this challenge, we will use advanced queries and joins to create a list of candidates for the mentorship program. 
- To complete this task, we wil use our knowledge of aliasing, filtering, and creating new tables.

# Objectives
-Use an ERD to understand relationships between SQL tables
-Create new tables in pgAdmin by using different joins
-Write basic-to intermediate level SQL statements

# Instructions
Create a technical report in markdown format that contains the following:
-Brief project summary
-PNG of your ERD
-Code for the requested queries, with examples of each output

--titles_retiring
SELECT ri.emp_no,
ri.first_name,
ri.last_name,
ti.title,
ti.from_date,
s.salary
INTO titles_retiring
FROM retirement_info as ri
RIGHT JOIN titles AS ti
ON (ri.emp_no = ti.emp_no)
INNER JOIN salaries AS s
ON (ri.emp_no = s.emp_no)

SELECT * FROM titles_retiring;



