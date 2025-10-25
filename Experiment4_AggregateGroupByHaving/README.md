# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
-- ![Screenshot 2025-04-29 175256](https://github.com/user-attachments/assets/7272ef76-6d77-4604-8108-e97d2bffc783)


```sql
--
SELECT Specialty, Gender, COUNT(*) AS TotalDoctors
FROM Doctors
GROUP BY Specialty, Gender
ORDER BY Specialty, Gender;
```

**Output:**
![Screenshot 2025-04-29 175307](https://github.com/user-attachments/assets/b4e05133-e49e-4af7-987a-d4f09f37bceb)



**Question 2**
---
--![Screenshot 2025-04-29 175314](https://github.com/user-attachments/assets/101e5d00-02c2-4b37-89e7-81cfebe1ddc2)


```sql
--
SELECT 
  StartYear AS ValidityYear,
  COUNT(DISTINCT PatientID) AS TotalPatients
FROM ValidYears
GROUP BY StartYear
ORDER BY StartYear;

```

**Output:**
![Screenshot 2025-04-29 175325](https://github.com/user-attachments/assets/7d0a4514-7d1b-4f35-bb8f-ebf572d31c08)



**Question 3**
---
--![Screenshot 2025-04-29 175352](https://github.com/user-attachments/assets/2c9377e7-55be-4d91-99f2-2d2b90868498)


```sql
--
SELECT DoctorID, COUNT(DoctorID) AS TotalRecords
FROM MedicalRecords
GROUP BY DoctorID;
```

**Output:**

![Screenshot 2025-04-29 175400](https://github.com/user-attachments/assets/b18c53b4-d81a-4f9b-9b9e-673fbb952584)

**Question 4**
---
-- 
![Screenshot 2025-04-29 175416](https://github.com/user-attachments/assets/3ceda034-d41e-4544-b8cd-563fa80ebffc)



```sql
-- SELECT 
  MAX(age) - MIN(age) AS age_difference
FROM 
  employee;
```

**Output:**
![Screenshot 2025-04-29 175423](https://github.com/user-attachments/assets/bb9251a5-96e9-452e-942d-1eb0032d4067)



**Question 5**
---
-- 
![Screenshot 2025-04-29 175436](https://github.com/user-attachments/assets/aa66c6be-94ab-4df9-a7cf-9bd44f68dc17)

```sql
SELECT 
  AVG(income) AS Average_Salary
FROM 
  employee;
--

```

**Output:**

![Screenshot 2025-04-29 175447](https://github.com/user-attachments/assets/a36c847a-c831-4e71-bb2b-cf2f86726824)


**Question 6**
---
--
![Screenshot 2025-04-29 175457](https://github.com/user-attachments/assets/0a74824c-d604-4046-86af-f849e6a2e20f)

```sql
-- 
SELECT 
  COUNT(DISTINCT city) AS unique_cities
FROM 
  customer;
```

**Output:**
![Screenshot 2025-04-29 175503](https://github.com/user-attachments/assets/e5a7c486-3c3e-4f86-b6b4-4eb35a4588a1)


**Question 7**
---
-- ![Screenshot 2025-04-29 175510](https://github.com/user-attachments/assets/d88cbb43-9554-45bc-9aa7-c2450de6348c)


```sql
--
SELECT 
  COUNT(*) AS employees_count
FROM 
  employee
WHERE 
  income > 50000;
```

**Output:**
![Screenshot 2025-04-29 175518](https://github.com/user-attachments/assets/b791f091-b68b-4d1e-8822-7197c8b827cc)


**Question 8**
---
-- 
![Screenshot 2025-04-29 175550](https://github.com/user-attachments/assets/0514d7e9-bbb2-43fe-93b7-28a961c159e7)

```sql
--
SELECT 
  address, 
  AVG(salary) AS "AVG(salary)"
FROM 
  customer1
GROUP BY 
  address
HAVING 
  AVG(salary) > 5000;
```

**Output:**
![Screenshot 2025-04-29 175604](https://github.com/user-attachments/assets/0ea3f7f9-546b-4de5-b9e3-3734fc39d3ac)

**Question 9**
![Screenshot 2025-04-29 175617](https://github.com/user-attachments/assets/e3f92782-bfda-4e27-bcf1-98351788a0be)

---
-- 
```sql
--
SELECT category_id, SUM(price) AS Total_Cost
FROM products
GROUP BY category_id
HAVING SUM(price) > 50;

```

**Output:**

![Screenshot 2025-04-29 175617](https://github.com/user-attachments/assets/502c8302-6956-4379-8e29-c88586df985a)


**Question 10**
---
--![Screenshot 2025-04-29 175624](https://github.com/user-attachments/assets/031f4943-4e7c-4067-94d2-145051d9284c)

```sql
SELECT 
  (age / 5) * 5 AS age_group,
  SUM(salary) AS "SUM(salary)"
FROM 
  customer1
GROUP BY 
  age_group
HAVING 
  SUM(salary) > 5000;
```

**Output:**



![Screenshot 2025-04-29 175631](https://github.com/user-attachments/assets/57528701-dfc0-4fad-b024-a267808a6771)

## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
