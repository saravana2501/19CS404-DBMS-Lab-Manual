# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
--![image](https://github.com/user-attachments/assets/216b62aa-47c8-4993-ab7a-089e46295692)


```sql
--
update Products
set reorder_lvl=reorder_lvl*0.7
where cost_price>50 and quantity<100 ;
```

**Output:**

![image](https://github.com/user-attachments/assets/022ddbd5-f6d0-4b68-a15f-12bb5986c1a4)


**Question 2**
---
-- ![image](https://github.com/user-attachments/assets/ea142d15-a90b-4868-92c9-2d9c1f02c695)


```sql
--
update suppliers
set supplier_name = 'A1 Suppliers'
where supplier_id = 8 ;
```

**Output:**

![image](https://github.com/user-attachments/assets/ef7dddf4-6afa-43ef-bc8e-d86b9a22edcf)


**Question 3**
---
--![image](https://github.com/user-attachments/assets/de1400d7-1c39-453a-b935-d2595162b880)


```sql
--
UPDATE products
SET reorder_lvl = CAST(reorder_lvl * 0.70 AS INT)
WHERE LOWER(product_name) LIKE '%cream%'
  AND quantity > reorder_lvl;
```

**Output:**
![image](https://github.com/user-attachments/assets/5c6e2d6d-39fd-4095-9fb0-5eaf20bf3267)

**Question 4**
---
-- ![image](https://github.com/user-attachments/assets/c80f719f-b685-4f68-a876-8be1b87957d5)


```sql
--
UPDATE products
SET sell_price = round(sell_price * 1.10, 2)
WHERE supplier_id = 6;
```

**Output:**
![image](https://github.com/user-attachments/assets/2a8f83f0-de2c-4d3c-96ce-4d48f722b509)


**Question 5**
---
-- ![image](https://github.com/user-attachments/assets/dbf4cd16-277f-4cce-b3a7-08d4658d64de)


```sql
--
delete from customer
where cust_country = 'India' and cust_city <> 'Chennai';
```

**Output:**

![image](https://github.com/user-attachments/assets/d76ae16e-2f15-4fca-8eb6-bc0bdcc81296)


**Question 6**
---
-- 
![image](https://github.com/user-attachments/assets/a4a31e0e-4038-4837-a821-ed572d11e784)



```sql
--
 delete from Customer
where (GRADE = 3 or AGENT_CODE =  'A008') and OUTSTANDING_AMT < 5000;
```

**Output:**

![image](https://github.com/user-attachments/assets/0f6e1a53-0d7f-4f40-98f6-9c1c847a109f)

**Question 7**
---
-- ![image](https://github.com/user-attachments/assets/e67879b8-da36-439b-9025-9cc015e024b7)


```sql
--
delete from  Customer
where (CUST_COUNTRY = 'UK' and WORKING_AREA = 'London') and GRADE < 3 ;
```

**Output:**

![image](https://github.com/user-attachments/assets/37b2dd41-046f-4fc1-8949-43d4c56efb7c)


**Question 8**
---
-- 
![image](https://github.com/user-attachments/assets/8e5cfad4-96b8-486b-8f2d-464801ec2b8b)

```sql
--
delete from  Doctors
where doctor_id = 1;
```

**Output:**

![image](https://github.com/user-attachments/assets/71233458-e0c6-4030-86a8-2a38a13dd30e)


**Question 9**
---
-- ![image](https://github.com/user-attachments/assets/9e5d53a7-22e3-4b1e-932f-411925b6cb0d)


```sql
--
DELETE FROM customer
WHERE LENGTH(CUST_NAME) = 6;
```

**Output:**

![image](https://github.com/user-attachments/assets/ff6bd5a9-7339-424a-96bb-563518d67e0a)


**Question 10**
---
-- ![image](https://github.com/user-attachments/assets/3e57121d-c3c8-4491-957f-95a30422fb9d)


```sql

SELECT DISTINCT EmpID FROM EmployeePosition
WHERE strftime('%Y', DateOfJoining) = '2024'
  AND Salary > 50000;
```

**Output:**

![image](https://github.com/user-attachments/assets/1721885e-85cd-4a81-aedf-557abab3b125)


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
