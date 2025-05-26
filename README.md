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
###  Answer: In PostgreSQL , the "VARCHAR" and "CHAR" both data type store STRING type data types. But there have some differences. 

#### CHAR(n) is Fixed length character. It contains difinte length string. As like if the length is CHAR(10) then the value will be of 10 character. If the character length less than 10 length then rest will be fill up with spaces.
1. Example: CREATE TABLE users (
  code CHAR(5)
);


#### VARCHAR (n) (Variable-length character): It support changeable length character. If the length is VARCHAR(10) then it can contain highest 10 character. Here don't fill extra space by space character.


#### Main differences are:
- CHAR length is fixed but VARCAHR length is Changeable.
- CHAR, Rest place fill up by space but VARCHAR rest place not used. 
- It's useful for Code, id and VARCHAR is usefull for name, address. 


##  3. What are the LIMIT and OFFSET clauses used for?
###  Answer: 


## 4. Explain the purpose of the WHERE clause in a SELECT statement.
###  Answer: WHERE clause is used for data filter with condition. It's used for filtering a definte data from all data. 
1. Example: SELECT * FROM students
WHERE grade = 'A';
- Here, in grade column only show which result grade is 'A'.
2. SELECT * FROM employees
WHERE salary > 50000;
- Only showing the data thoose employees salary is more than 50,000;


## 5. What is the significance of the JOIN operation, and how does it work in PostgreSQL?
###  Answer: The JOIN operation is used to combine two or more tables together, where there is a relationship between the tables. 
#### The importance of JOIN:
- Data from different tables can be brought together and analyzed.
- After normalizing the database, it is possible to extract related data from fragmented tables.
- It's essential for creating reports.
#### How works the JOIN: 
- The JOIN operation usually joins tables by matching columns (such as primary key and foreign key).

1. Example: Inner JOIN: 
SELECT students.name, classes.class_name
FROM students
JOIN classes ON students.class_id = classes.id;

#### Types of JOINS: 
- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- FULL JOIN