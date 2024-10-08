# PostgreSQL-Clauses
This repository contains the important clauses in PostgreSQL as well as in other databases. It is part 1.


### Please, `Create a Table` like below in order to get benefit of this repository.:-
```
CREATE TABLE EMPLOYEES (
    ID SERIAL PRIMARY KEY,
    NAME VARCHAR(100) NOT NULL,
    EMAIL VARCHAR(150) UNIQUE NOT NULL,
    SALARY DECIMAL(10, 2) NOT NULL,
    ADDRESS VARCHAR(255),
    CITY VARCHAR(100),
    CREATED_AT DATE DEFAULT CURRENT_DATE,
    UPDATED_AT DATE DEFAULT CURRENT_DATE
);
```
### `Insert data:-`

```
INSERT INTO EMPLOYEES (NAME, EMAIL, SALARY, ADDRESS, CITY)
VALUES
('Ali Hassan', 'alihassan@example.com', 55000.50, '123 Maple St.', 'Karachi'),
('Sara Malik', 'saramalik@example.com', 72000.00, '456 Oak Ave.', 'Lahore'),
('Usman Javed', 'usmanj@example.com', 67000.75, '789 Pine Dr.', 'Islamabad'),
('Ayesha Khan', 'ayeshak@example.com', 60000.20, '101 Elm Rd.', 'Rawalpindi'),
('Zain Ali', 'zainali@example.com', 48000.00, '202 Cedar Blvd.', 'Faisalabad'),
('Hira Shah', 'hirashah@example.com', 85000.00, '303 Spruce Ln.', 'Multan'),
('Muhammad Farooq', 'mfarooq@example.com', 54000.10, '404 Birch St.', 'Quetta'),
('Fatima Noor', 'fatimanoor@example.com', 62000.30, '505 Willow Rd.', 'Peshawar'),
('Muhammad Asad', 'masad@example.com', 75000.50, '606 Palm St.', 'Hyderabad'),
('Muhammad Faizan', 'mfaizan@example.com', 68000.00, '707 Fir Ave.', 'Sialkot');
```

### `Clauses`

```
A clause in SQL is a built-in function that helps to fetch the required records from a database table. A clause receives a conditional expression, i.e. a column name or some terms involving the columns.
```

### Some important and useful clauses that will surely help you to create your next project.

### 1) `WHERE:-`

#### Where query specify that we want to select a data where a particular condition match. For example:-

#### Some operator are used with where clause to filter more data with precision.

###### Equal to.
```
SELECT * FROM EMPLOYEES
WHERE SALARY = 72000;
```

###### Greater than or equal to.
```
SELECT * FROM EMPLOYEES
WHERE SALARY >= 72000;
```

###### Less than or equal to.
```
SELECT * FROM EMPLOYEES
WHERE SALARY <= 72000;
```

###### Less than.
```
SELECT * FROM EMPLOYEES
WHERE SALARY <= 72000;
```

###### Greater than.
```
SELECT * FROM EMPLOYEES
WHERE SALARY > 72000;
```

###### OR.
```
SELECT * FROM EMPLOYEES
WHERE SALARY = 72000 OR CITY = 'Lahore';
```

###### AND.
```
SELECT * FROM EMPLOYEES
WHERE SALARY = 72000 AND CITY = 'Lahore';
```

###### IN.
```
SELECT * FROM EMPLOYEES
WHERE SALARY IN (68000, 72000 );
```

###### NOT IN.
```
SELECT * FROM EMPLOYEES
WHERE SALARY NOT IN (68000, 72000 );
```

###### BETWEEN.
```
SELECT * FROM EMPLOYEES
WHERE SALARY BETWEEN (68000, 72000 );
```

###### LIKE.
It gives you data from specifies column with similiar input. For example below code is used to extract the data that whoose employees name are start with a, then end with a, and then both at the end and start respectively.

```
SELECT * FROM EMPLOYEES
WHERE NAME LIKE ('%a');
```

```
SELECT * FROM EMPLOYEES
WHERE NAME LIKE ('a%');
```

```
SELECT * FROM EMPLOYEES
WHERE NAME LIKE ('%a%');
```
`
###  2) `ORDER BY`
#### It ensure that specific type of data will order by on the base on condition. For example:-

###### ASC.
```
SELECT * FROM EMPLOYEES
ORDER BY SALARY ASC;
```

###### DESC.
```
SELECT * FROM EMPLOYEES
ORDER BY SALARY DESC;
```

### 3) `DISTINCT:-`
#### It gives you the unique values from column.

```
SELECT DISTINCT CITY FROM EMPLOYEES;
```

### 4) `LIMIT:-`
#### It limits the return data. For example i limit the return data to only 3 rows. 

```
SELECT * FROM EMPLOYEES LIMIT 3;
```