# HealthCare Data Analysis

### Dashboard Link : 

### Data Source: SQL Server 

## Problem Statement

This project examines healthcare data to uncover patterns in patient admissions, length of stay, readmissions, and treatment costs. The analysis focuses on transforming raw data into actionable insights that support operational efficiency, performance monitoring, and informed decision-making.

### Important Note: 
The Dynamic SQL logic was initially developed and tested using an employee dataset for demonstration purposes. The same logic will later be implemented on healthcare (clinical) data by replacing the employee dataset.

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



<img width="1210" height="566" alt="Image" src="https://github.com/user-attachments/assets/efd7e162-1b1a-477a-b3c8-999df9c6fa58" />


- Step 15 : The #1 temporary table reflects the updated values, as shown below.


<img width="1071" height="232" alt="Image" src="https://github.com/user-attachments/assets/72e62c06-d17c-4d41-958c-f305d2bec2b0" />


- Step 16 : Additionally, I implemented dynamic SQL to update the Distinct Count column. As shown below, the column values were successfully updated.


<img width="1241" height="563" alt="Image" src="https://github.com/user-attachments/assets/2b9dae1a-917b-4043-b7aa-2baae6b468d2" />


- Step 17 : Finally, I implemented the logic to calculate the Median and Mode values. The computed results are reflected in the table below.

<img width="604" height="191" alt="Image" src="https://github.com/user-attachments/assets/a61f71b3-d0e9-4a62-b3d0-e59fc7b745a7" />


<img width="834" height="228" alt="Image" src="https://github.com/user-attachments/assets/9c911d50-5606-42d9-8038-8fd5e7ef99be" />


<img width="1170" height="274" alt="Image" src="https://github.com/user-attachments/assets/e8535173-cdcf-49aa-9301-3759d9e8e370" />



- Step 18 : Implemented logic to handle Date-type columns by replacing NULL values with appropriate default values.


<img width="1268" height="504" alt="Image" src="https://github.com/user-attachments/assets/09e8a146-01ce-4da1-82d9-96852b6bbe62" />


- Step 19: Comparing this table with the previously mentioned table shows that the NULL values in the date column have been updated with the calculated metrics such as Minimum, Maximum, Distinct Count, Zero Value, and Null Count.


<img width="1084" height="259" alt="Image" src="https://github.com/user-attachments/assets/114163b8-f34e-47a6-94b7-4fb84de91a27" />

- Step 20 : Similar arrangements were implemented for Text data type columns using Dynamic SQL, where NULL values were successfully replaced with the corresponding calculated metrics.


<img width="1136" height="264" alt="Image" src="https://github.com/user-attachments/assets/92766e03-a786-45a0-aae7-d0566a16bf16" />


<img width="1237" height="568" alt="Image" src="https://github.com/user-attachments/assets/65f368ea-9a10-4137-bf5b-9eec512a4a9a" />


- Step 21 : An error occurred while processing the Zero Value column; however, after identifying and fixing the issue, the column was successfully updated.

- Step 22 : Implemented separate logic for BIT data type columns by excluding MIN and MAX calculations and adding logic to compute Null Count, Distinct Count, Mode, and Zero Value metrics.


<img width="1088" height="270" alt="Image" src="https://github.com/user-attachments/assets/3b9bc848-efb8-4dba-8f92-d40d4b0c9a2a" />


- Step 23 : Created a sample table using SQL to analyze and understand the concept of column distribution.


<img width="1129" height="567" alt="Image" src="https://github.com/user-attachments/assets/ac204dfd-2364-4a95-9019-a19d0a3498c8" />


- Step 24 : Upon executing the SQL code, the resulting table structure and data can be observed as shown below.

<img width="759" height="255" alt="Image" src="https://github.com/user-attachments/assets/444a9135-795d-4c2b-a911-79cebc33d9eb" />

- Step 25 : Queried INFORMATION_SCHEMA to obtain detailed information about the table columns, and the resulting output is shown below.



<img width="1337" height="337" alt="Image" src="https://github.com/user-attachments/assets/87fb4360-22f5-4ad2-8645-24a25d696134" />


- Step 26 : After executing the Dynamic SQL code for column distribution, different columns along with their frequency counts can be observed in the small tables shown below.


<img width="1215" height="352" alt="Image" src="https://github.com/user-attachments/assets/55efc783-54f1-4ace-aa7d-5b8a29790b2b" />



<img width="319" height="497" alt="Image" src="https://github.com/user-attachments/assets/1452be94-a9cf-49cd-9c95-cd7a6718cf5b" />
<img width="194" height="405" alt="Image" src="https://github.com/user-attachments/assets/53fe2aaa-3422-4968-976b-0b04500f132c" />
<img width="205" height="489" alt="Image" src="https://github.com/user-attachments/assets/28e52ef5-6ca0-4618-a29d-2094110ece66" />


- Step 27 : Created a new database called "Healthcare" for data analysis purposes.

- Step 28 : Developed a SQL query to create a blank table containing the following columns: Hospital_ID, Admission_Date, Total_Admissions, Readmissions, Infections, Total_Deaths, and Average_Length_of_Patient_Stay.

<img width="580" height="382" alt="Image" src="https://github.com/user-attachments/assets/66c02a3a-70ec-4dc7-96cb-9bfff10085be" />

- Step 29 : Defined appropriate data types for each column to ensure proper data storage and integrity.

- Step 30 : Declared several variables to check and validate the data types of the columns.

 
 <img width="475" height="206" alt="Image" src="https://github.com/user-attachments/assets/8a86d0f2-0a8f-46a5-ba60-8ad126e73e17" />


- Step 31 : Used a WHILE loop to generate data for each hospital. Additionally, the ABS (Absolute) function was applied to ensure that all generated values are in positive form.

- Step 32 : Used dynamic SQL to generate 2 million records per hospital, creating a large-scale dataset of 20 million records for analysis.

<img width="1213" height="566" alt="Image" src="https://github.com/user-attachments/assets/e5e2ecc3-9004-4cea-b3a1-e0b87161fcb5" />

- Step 33 : Queried the top 10 records from the Clinical Data table to review the generated dataset, as shown below.

<img width="658" height="350" alt="Image" src="https://github.com/user-attachments/assets/114d4686-ddfc-4893-ab75-c1e32309947f" />






