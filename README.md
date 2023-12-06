This repository contains SQL scripts to create and manage an employee database. The database schema includes tables for departments, titles, employees, department assignments, managers, and salaries.

Table of Contents
Database Schema
SQL Scripts
Queries
Usage
Contributing
License
Database Schema



Query 1: This query retrieves information about employees along with their salaries. It uses the JOIN operation to combine rows from the employees table (aliased as e) with corresponding rows from the salaries table (aliased as s). The condition for joining is that the emp_no in the employees table should match the emp_no in the salaries table.

Query 2: This query selects employees who were hired in the year 1986. The EXTRACT(YEAR FROM hire_date) function is used to extract the year from the hire_date column, and the WHERE clause filters the results to include only those where the extracted year is equal to 1986.

Query 3:This query retrieves information about department managers and their respective departments. It joins the employees table (aliased as e) with the dept_manager table (aliased as d_mgr) based on the emp_no column. Then, it further joins with the departments table (aliased as dep) based on the dept_no column.

Query 4: This query shows a list of employees along with the departments they belong to. It uses JOIN operations to combine information from the employees, dept_emp, and departments tables based on matching emp_no and dept_no columns.

Query 5: This query retrieves employees with the first name 'Hercules' and last names that start with the letter 'B'. The WHERE clause filters the results based on these conditions.

Query 6: This query lists employees who are currently part of the 'Sales' department. It joins the employees, dept_emp, and departments tables to get information about employees and their respective departments, and the WHERE clause filters the results to include only those in the 'Sales' department.

Query 7: This query retrieves employees who are part of either the 'Sales' or 'Development' departments. It uses the WHERE clause with the condition d.dept_name = 'Sales' OR d.dept_name = 'Development' to filter the results accordingly.

Query 8: This query provides the frequency of each unique last name in the employees table. It uses the COUNT(*) function to count the occurrences of each last name, and GROUP BY last_name groups the results by last name. The ORDER BY frequency DESC sorts the results in descending order based on the frequency.