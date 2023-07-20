# **sql-challenge**

## Prompt:
 *It’s been two weeks since you were hired as a new data engineer at Pewlett Hackard (a fictional company). Your first major task is to do a research project about people whom the company employed during the 1980s and 1990s. All that remains of the employee database from that period are six CSV files.*

## Data Engineering

Before jumping into PostgreSQL, I created the Entity Relationship Diagram starting with the tables based on the CSV files provided. I started with the tables that contained primary keys first then added the tables that would contain these primary keys as foreign keys.

![image](https://github.com/kadyepley/sql-challenge/blob/main/erd_sql_challenge_map.jpg)

The ERD was then exported for PostgreSQL and copied into SQL for accuracy. All data provided was imported prioritizing the tables with primary keys first before importing tables with foreign keys. After a few tries, finally everything was imported and all tables were displayed correctly. 

## Data Analysis

1. **List the employee number, last name, first name, sex, and salary of each employee.**
This pulled the data that I wanted about each employee by column from both the employees and the salaries tables while joining the data at the employee number.  
![image](https://github.com/kadyepley/sql-challenge/blob/main/images/data_analysis_1.jpg)

1. **List the first name, last name, and hire date for the employees who were hired in 1986.**
I did not have to include the table name before the name of each column this time because I would not be joining tables. I used the **WHERE** function to ensure that the hire dates would only include those in the year 1986. This operator is inclusive so I set the endpoints to January 1, 1986 and December 31, 1986.
![image](https://github.com/kadyepley/sql-challenge/blob/main/images/data_analysis_2.jpg)

1. **List the manager of each department along with their department number, department name, employee number, last name, and first name.**
Similarly to the first objective, this would pull the columns we needed across three tables. This would start with the departments table, joining with the dept_manager table at the department number. Then, the employees table was joined at the employee number for each manager.
![image](https://github.com/kadyepley/sql-challenge/blob/main/images/data_analysis_3.jpg)

1. **List the department number for each employee along with that employee’s employee number, last name, first name, and department name.**
This objective will need 3 tables to pull all the columns needed. This is similar to the previous objective.
![image](https://github.com/kadyepley/sql-challenge/blob/main/images/data_analysis_4.jpg)

1. **List first name, last name, and sex of each employee whose first name is Hercules and whose last name begins with the letter B.**
First, select the columns we want displayed. I am only pulling data from the employees table so the column names alone are sufficient. I only want the data where the first name is an exact match to "Hercules". The last name can be any name as long as it begins with a B, so I use **LIKE** instead of the "=" again. 
![image](https://github.com/kadyepley/sql-challenge/blob/main/images/data_analysis_5.jpg)

1. **List each employee in the Sales department, including their employee number, last name, and first name.**
This is a compounded version of the previous objectives where I joined three tables to get all my data displaying together with a constraint at the end. This is like with the first name of Hercules, where I set a constraint that the only employees shown are the ones with their department is equal to "Sales" after all the data is joined together. 
![image](https://github.com/kadyepley/sql-challenge/blob/main/images/data_analysis_6.jpg)

1. **List each employee in the Sales and Development departments, including their employee number, last name, first name, and department name.**
The same code is used as before. However, the **OR** operator is used to add the employees in the Development department as well. 
![image](https://github.com/kadyepley/sql-challenge/blob/main/images/data_analysis_7.jpg)

1. **List the frequency counts, in descending order, of all the employee last names (that is, how many employees share each last name).**
I select the last names column from my employees table to analyze. I use the **COUNT** operator based on the frequency of each last name in the employees table. I then group the output by the last name in decending order based on the count of each last name. 
![image](https://github.com/kadyepley/sql-challenge/blob/main/images/data_analysis_8.jpg)