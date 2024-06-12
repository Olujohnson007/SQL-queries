# SQL-queries
Project Description
My organization is committed to enhancing the security of our systems. My role involves ensuring system safety, investigating potential security issues, and updating employee computers as necessary. Below are examples of how I utilized SQL with filters to perform security-related tasks.

Retrieve After-Hours Failed Login Attempts
To investigate a potential security incident that occurred after business hours (post 18:00), I needed to filter and review all failed login attempts during this period. The following SQL query on top in the screen shots demonstrates how I filtered for these specific failed login attempts:
 ![image](https://github.com/Olujohnson007/SQL-queries/assets/169572108/b40f4469-0902-4d74-9728-b14eb14bfd3b)


The first part of the screenshot is my query, and the second part is a portion of the output. This query filters for failed login attempts that occurred after 18:00. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with an AND operator to filter my results to output only login attempts that occurred after 18:00 and were unsuccessful. The first condition is login_time > '18:00', which filters for the login attempts that occurred after 18:00. The second condition is success = FALSE, which filters for the failed login attempts. 
Retrieve login attempts on specific dates
A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or on the day before needs to be investigated.

The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates.
![image](https://github.com/Olujohnson007/SQL-queries/assets/169572108/1975f906-d6ee-4d48-bb69-0c72aebf98c6)


 

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with an OR operator to filter my results to output only login attempts that occurred on either 2022-05-09 or 2022-05-08. The first condition is login_date = '2022-05-09', which filters for logins on 2022-05-09. The second condition is login_date = '2022-05-08', which filters for logins on 2022-05-08.
Retrieve login attempts outside of Mexico
After investigating the organization’s data on login attempts, I believe there is an issue with the login attempts that occurred outside of Mexico. These login attempts should be investigated.
The following code demonstrates how I created a SQL query to filter for login attempts that occurred outside of Mexico.
 ![image](https://github.com/Olujohnson007/SQL-queries/assets/169572108/0df62c55-30b6-4b97-8e32-613bf45bf8b7)
![image](https://github.com/Olujohnson007/SQL-queries/assets/169572108/bdc2302f-c9a0-4af5-a301-79553d186dcf)
![image](https://github.com/Olujohnson007/SQL-queries/assets/169572108/fbacec6d-e1dd-4b99-ad20-18c5ebc50bbe)
![image](https://github.com/Olujohnson007/SQL-queries/assets/169572108/1011fd0d-55c6-4506-88dd-2d4ae6a8c107)

 
 
 

The first part of the screenshot shows my SQL query, and the second part displays a portion of the output. This query retrieves all login attempts made from countries other than Mexico. Initially, I selected all data from the log_in_attempts table. Then, I applied a WHERE clause using NOT and LIKE to exclude entries where the country is represented as 'MEX' or 'MEXICO'. The LIKE operator with the pattern 'MEX%' was used because it matches any string that starts with 'MEX', and the percentage sign (%) serves as a wildcard for any number of unspecified characters.

Retrieve Employees in Marketing
My team needs to update the computers for specific employees in the Marketing department. To accomplish this, I need to identify which employees' machines require updates.

The following SQL query filters for employees in the Marketing department located in the East building:
![image](https://github.com/Olujohnson007/SQL-queries/assets/169572108/25f4d202-984c-4b85-8ad5-896558e67641)

 

The first part of the screenshot shows my SQL query, and the second part displays a portion of the output. This query returns all employees in the Marketing department located in the East building. Initially, I selected all data from the employees table. Then, I applied a WHERE clause using AND to filter for employees who work in the Marketing department and are located in the East building. I used the LIKE operator with the pattern 'East%' because the data in the office column represents the East building with specific office numbers. The first condition, department = 'Marketing', filters for employees in the Marketing department. The second condition, office LIKE 'East%', filters for employees in the East building.

Retrieve Employees in Finance or Sales
The machines for employees in the Finance and Sales departments also need to be updated. Since a different security update is required, I need to gather information on employees only from these two departments.

The following SQL query demonstrates how I filtered for employee machines from employees in the Finance or Sales departments:

![image](https://github.com/Olujohnson007/SQL-queries/assets/169572108/98d179d5-4cdb-48b4-95be-aa90e8ce44e5)
![image](https://github.com/Olujohnson007/SQL-queries/assets/169572108/bda9d724-4106-4e0a-b5cc-cf4cec8f91ab)


 

 


The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all employees in the Finance and Sales departments. First, I started by selecting all data from the employees table. Then, I used a WHERE clause with OR to filter for employees who are in the Finance and Sales departments. I used the OR operator instead of AND because I want all employees who are in either department. The first condition is department = 'Finance', which filters for employees from the Finance department. The second condition is department = 'Sales', which filters for employees from the Sales department.
Retrieve all employees not in IT
My team needs to make one more security update on employees who are not in the Information Technology department. To make the update, I first have to get information on these employees.
The following demonstrates how I created a SQL query to filter for employee machines from employees not in the  Information Technology department.
![image](https://github.com/Olujohnson007/SQL-queries/assets/169572108/1dfce39d-82da-4682-b801-ccd58318f10e)
![image](https://github.com/Olujohnson007/SQL-queries/assets/169572108/91c90436-26d8-43fc-acdd-5c4657b309e2)
![image](https://github.com/Olujohnson007/SQL-queries/assets/169572108/b6eaa882-c8e7-4a5f-98e0-c85d0a81cdd1)
![image](https://github.com/Olujohnson007/SQL-queries/assets/169572108/37deded3-5a4b-4acb-8a02-1fd20982404b)

 
 
 

 The first part of the screenshot shows my SQL query, and the second part displays a portion of the output. This query retrieves all employees who are not in the Information Technology department. Initially, I selected all data from the employees table. Then, I applied a WHERE clause with the NOT operator to filter out employees from the Information Technology department.


Project Description
In this project, I utilized SQL queries to enhance the security and efficiency of my organization's IT systems. The tasks involved retrieving specific data on login attempts and employee machines, using various SQL filtering techniques. By applying conditions such as AND, OR, NOT, and LIKE, I was able to isolate relevant information from the log_in_attempts and employees tables to address different security and operational requirements.

Summary
Throughout the project, I applied filters to SQL queries to extract targeted information from the log_in_attempts and employees tables. I used logical operators like AND, OR, and NOT to filter the data precisely. Additionally, the LIKE operator with the % wildcard allowed me to match specific patterns efficiently. These techniques ensured that I obtained the necessary data to support the organization's security measures and system updates.
