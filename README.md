# learn-mariaDB

Learn Database using MariaDB

## Data Schema

### Employees

|   emp_no | birth_date   | first_name   | last_name   | gender   | hire_date   |
|----------|--------------|--------------|-------------|----------|-------------|
|        1 | 1994-11-20   | Guntur       | KH          | M        | 2018-08-07  |
|        2 | 1997-12-20   | Alif         | Raher       | M        | 2018-08-07  |
|        3 | 1998-11-06   | Dwi          | Heryanto    | M        | 2018-08-07  |
|        4 | 1999-11-07   | Andre        | Kurniawan   | M        | 2018-08-07  |

### Titles

|   emp_no | title           | from_date   | to_date    |
|----------|-----------------|-------------|------------|
|        1 | BACK END DEV    | 2018-07-01  | 9999-01-01 |
|        2 | PROJECT MANAGER | 2018-07-01  | 9999-01-01 |
|        3 | BACK END DEV    | 2018-07-01  | 9999-01-01 |
|        4 | FRONT END DEV   | 2018-07-01  | 2018-09-01 |

### Describe Employees table

```sql
DESC employees;
+------------+---------------+--------+-------+-----------+----------------+
| Field      | Type          | Null   | Key   |   Default | Extra          |
|------------+---------------+--------+-------+-----------+----------------|
| emp_no     | int(11)       | NO     | PRI   |    <null> | auto_increment |
| birth_date | date          | NO     |       |    <null> |                |
| first_name | varchar(14)   | NO     |       |    <null> |                |
| last_name  | varchar(16)   | NO     |       |    <null> |                |
| gender     | enum('M','F') | NO     |       |    <null> |                |
| hire_date  | date          | NO     |       |    <null> |                |
+------------+---------------+--------+-------+-----------+----------------+

```

### Describe Titles table

```sql
DESC titles;
+-----------+-------------+--------+-------+------------+----------------+
| Field     | Type        | Null   | Key   | Default    | Extra          |
|-----------+-------------+--------+-------+------------+----------------|
| emp_no    | int(11)     | NO     | PRI   | <null>     | auto_increment |
| title     | varchar(50) | NO     | PRI   | <null>     |                |
| from_date | date        | NO     |       | <null>     |                |
| to_date   | date        | YES    |       | 9999-01-01 |                |
+-----------+-------------+--------+-------+------------+----------------+

```