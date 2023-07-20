# **sql-challenge**

## Prompt:
### *It’s been two weeks since you were hired as a new data engineer at Pewlett Hackard (a fictional company). Your first major task is to do a research project about people whom the company employed during the 1980s and 1990s. All that remains of the employee database from that period are six CSV files.*

## Data Engineering

### Before jumping into PostgreSQL, I created the Entity Relationship Diagram starting with the tables based on the CSV files provided. I started with the tables that contained primary keys first then added the tables that would contain these primary keys as foreign keys.

![image](https://github.com/kadyepley/sql-challenge/blob/main/erd_sql_challenge_map.jpg)

### The ERD was then exported for PostgreSQL and copied into SQL for accuracy. All data provided was imported prioritizing the tables with primary keys first before importing tables with foreign keys. After a few tries, finally everything was imported and all tables were displayed correctly. 

## Data Analysis

1. List the employee number, last name, first name, sex, and salary of each employee.
![image]()
1. List the first name, last name, and hire date for the employees who were hired in 1986.

1. List the manager of each department along with their department number, department name, employee number, last name, and first name.

1. List the department number for each employee along with that employee’s employee number, last name, first name, and department name.

1. List first name, last name, and sex of each employee whose first name is Hercules and whose last name begins with the letter B.

1. List each employee in the Sales department, including their employee number, last name, and first name.

1. List each employee in the Sales and Development departments, including their employee number, last name, first name, and department name.

1. List the frequency counts, in descending order, of all the employee last names (that is, how many employees share each last name).