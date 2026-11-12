# DBMS Notes

## Week 1 to 4
### Why DBMS

1. Data Redundancy & Inconsistency: more than 1 copy of data
2. Difficulty in Accessing Data: for other system
3. Data Isolation: scattered are not good
4. Integrity Problems: in bank data don't go beyond 0
5. Atomicity Issues: like payment nothing or everything
6. Concurrent-Access Anomalies: we can read or update multiple file at the same time
7. Security Flaws: we can give access of particular data to particular persion

<img width="802" height="466" alt="image" src="https://github.com/user-attachments/assets/90bf13a6-9cd3-4931-acb3-23a313108975" />
1. Physical level
2. View level
3. logical level

__Instance__ refers to the collection of information stored in the database at a given point of time. 
basically rows of data

# Database language
1. **Data Definition Language (DDL) :** to create Tables
2. **Data Manipulation Language (DML) :** like select * --> sql
3. **Data Control Language (DCL)**: Used to manage permissions and security (the bouncers)

## Query process
<img width="942" height="568" alt="image" src="https://github.com/user-attachments/assets/b0eace44-9d8e-45c9-b4fe-c12e4f47bd97" />

⋈ - **natural join**
× - **Cartesian Product**
𝜎 - **Select**
𝜋 - **Project**

### Cammends
1. ALTER - to change blueprint of data after creation it
2. DROP - to delete whole table
3. DELETE - to delete particular row of data

### Sql filtering 
1. **FROM**: The engine goes to the tables to gather the raw data.
2.** WHERE**: It filters out the individual rows that don’t meet the criteria.
3. **GROUP BY**: It takes the surviving rows and sorts them into buckets.
4. **HAVING**: It looks at the buckets, calculates the aggregates, and throws away any buckets that fail the test.
5. **SELECT**: It finally decides which columns to show you on the screen.
6.**ORDER BY**: It alphabetizes or sorts the final output for you.
7. **some**: compare to at least one row
8. **all**: compare to all rows
9. **exist**
10. **not exist**
11. **with**
    ```
    with max_budget(value) as
    (select max(budget) from department)
        select department.dept_name
    from department, max_budget
    where department.budget = max_budget.value;
    ```

# joins remain















