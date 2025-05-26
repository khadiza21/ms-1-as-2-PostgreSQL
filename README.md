# PostgreSQL 

## 1. How can you calculate aggregate functions like COUNT(), SUM(), and AVG() in PostgreSQL?

### Answer: 
- In PostgreSQL can find the summary of data by using aggregate functions. Here describes: 

#### COUNT () - By this function can count the row's number. It's count the records of a definite column. 
1. Example: SELECT COUNT(*) FROM students;
- Here It will show the total record of student table. 
2. Example: For definite column: SELECT COUNT(email) FROM students;
- It will count the which record are not null in email col. 

#### SUM() : It calculate the sum of a definite column 
1. Example: SELECT SUM(salary) FROM employees;
- Here It calculate the sum of all employees of employees table. 

#### AVG() : It help find the average value. Find a average value of a definte column.
1. Example: SELECT AVG(salary) FROM employees;
- It will show the average salary of salary col. 

2. BY avg() also can find average value with group using GROUP BY key word. 
- Example: SELECT department, AVG(salary)
FROM employees
GROUP BY department;
- It will show the average salary of each department.




## 2. What is the difference between the VARCHAR and CHAR data types?
###  Answer: 


##  3. What are the LIMIT and OFFSET clauses used for?
###  Answer: 


## 4. Explain the purpose of the WHERE clause in a SELECT statement.
###  Answer: 


## 5. What is the significance of the JOIN operation, and how does it work in PostgreSQL?
###  Answer: 