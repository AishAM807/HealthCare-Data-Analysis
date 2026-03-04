# HealthCare Data Analysis

### Dashboard Link : 

### Data Source: SQL Server 

## Problem Statement

This project examines healthcare data to uncover patterns in patient admissions, length of stay, readmissions, and treatment costs. The analysis focuses on transforming raw data into actionable insights that support operational efficiency, performance monitoring, and informed decision-making.


### Steps followed 

- Step 1 : Downloaded and installed SQL Server to create a reliable database environment for storing and managing healthcare data.

- Step 2 : Created a new database named Web_Fun and implemented dynamic SQL to define and manage tables efficiently.

- Step 3 : Executed SQL queries to create and validate database tables based on the defined schema, as shown below.

 
 <img width="384" height="550" alt="Image" src="https://github.com/user-attachments/assets/b9f12dbd-67ed-4480-8048-ceed736271e1" />


- Step 4 : Used the UNION ALL operation to combine data from multiple tables into a single unified dataset.


 <img width="491" height="547" alt="Image" src="https://github.com/user-attachments/assets/8a3318d7-1e9b-4288-860d-2dec627722c3" />


- Step 5 : Created a new database named Data_Profiling and successfully loaded employee data using SQL queries as shown below.

- Step 6 : Utilized the INFORMATION_SCHEMA views to examine column-level metadata, including data types, constraints, and structure.



<img width="1103" height="362" alt="Image" src="https://github.com/user-attachments/assets/95a17eda-0d12-482a-a331-f9e89d6f64bb" />


 - Step 7 : Created and executed a temporary hash table (#Table1) to store intermediate results during data processing.


<img width="887" height="534" alt="Image" src="https://github.com/user-attachments/assets/005f9a56-2f10-4574-af44-db17e713e8e7" />


- Step 8 : Modified the temporary hash table structure by adding new columns to support additional data attributes and calculated fields.



<img width="367" height="207" alt="Image" src="https://github.com/user-attachments/assets/d61d6a95-713e-446b-a53c-44f8fb760acb" />



- Step 9 : Executed SQL queries to compute essential statistical measures, including minimum, maximum, median, standard deviation, and distinct count of salary values.


<img width="669" height="552" alt="Image" src="https://github.com/user-attachments/assets/b4fb1789-1097-4080-af67-8201cca68414" />


- Step 10 : To calculate the median of the Salary column, I created temporary table #20 to select the Salary column, count the total number of rows, and arrange the records in ascending order. I also generated a column named row_num to assign sequential row numbers for accurate median calculation.


<img width="978" height="552" alt="Image" src="https://github.com/user-attachments/assets/99c828c3-9c92-430f-8cd5-e6e128f28971" />
  

- Step 11 : To determine whether the total number of records was odd or even, I declared three variables and applied the necessary conditional logic.


<img width="771" height="527" alt="Image" src="https://github.com/user-attachments/assets/c4379313-3f9b-45e3-95dc-b6c43dbd0553" />


- Step 12 : I also calculated the mode for the Department column to identify the most frequently occurring value.


<img width="751" height="557" alt="Image" src="https://github.com/user-attachments/assets/f21db38b-0724-4ff8-abe9-0fe1def71a34" />


- Step 13 : To update the #1 temporary table, I implemented dynamic SQL by declaring the required variables, as demonstrated in the script below.


<img width="446" height="144" alt="Image" src="https://github.com/user-attachments/assets/fa35a8a5-8bb1-4d92-9a19-db6d5d74a289" />



- Step 14 : Using a WHILE loop and conditional (IF) statements, I updated the column values, including Minimum, Maximum, Zero Value Count, Mean, Null Count, and Standard Deviation, as demonstrated below.


<img width="1299" height="561" alt="Image" src="https://github.com/user-attachments/assets/183af1d1-dbe2-459c-8ea3-2b452d630616" />


- Step 15 : The #1 temporary table reflects the updated values, as shown below.


<img width="1071" height="232" alt="Image" src="https://github.com/user-attachments/assets/72e62c06-d17c-4d41-958c-f305d2bec2b0" />
