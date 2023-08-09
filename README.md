# Apply Filters to SQL Queries

## Project Description
Within my fictional organization, the paramount objective is to enhance the security of our system. As the designated custodian of security, my responsibilities encompass safeguarding the system, meticulously probing potential security vulnerabilities, and effecting necessary updates to employee computers. The ensuing steps illustrate instances where I harnessed SQL alongside filters to execute security-oriented assignments.

## Retrieve After Hours Failed Login Attempts
A prospective security incident transpired beyond regular business hours, specifically after 18:00. It is imperative to scrutinize any unsuccessful login attempts that transpired during this after-hours period.

Below is an example of the code illustrating my creation of a SQL query aimed at filtering for unsuccessful login attempts that took place beyond standard business hours.

<p align="center">
<img src="https://i.imgur.com/D31zGPE.png" height="70%" width="70%" alt="Azure Free Account"/>

The initial segment of the screenshot showcases my query, while the subsequent portion presents a snippet of the output. This query is tailored to isolate unsuccessful login attempts that took place post 18:00. To initiate the process, I retrieved all data from the ```log_in_attempts``` table. I subsequently employed a ```WHERE``` clause featuring an ```AND``` operator to refine the results, exclusively displaying login attempts that unfolded after 18:00 and were unsuccessful. The initial condition, ```login_time > '18:00'```, serves to filter login attempts post 18:00, whereas the second condition, ```success = FALSE```, isolates failed login attempts.

## Retrieve Login Attempts on Specific Dates
An event of concern transpired on 2022-05-09. It is imperative to scrutinize any login activities that transpired on both 2022-05-09 and the preceding day.

Here's an example of the code illustrating my creation of a SQL query designed to filter for login attempts that took place on particular dates.

<p align="center">
<img src="https://i.imgur.com/8cmBnt1.png" height="70%" width="70%" alt="Azure Free Account"/>

The initial segment of the screenshot displays my query, while the subsequent part presents a segment of the output. This query is tailored to retrieve all login attempts that transpired on either 2022-05-09 or 2022-05-08. To commence, I initiated the process by selecting all data from the ```log_in_attempts``` table. Subsequently, I utilized a ```WHERE``` clause featuring an ```OR``` operator to refine the output, exclusively showcasing login attempts from either 2022-05-09 or 2022-05-08. The initial condition, ```login_date = '2022-05-09'```, serves to extract logins from 2022-05-09, while the second condition, ```login_date = '2022-05-08'```, does the same for logins on 2022-05-08.

## Retrieve Login Attempts Outside of Mexico
Upon scrutinizing the organization's login attempt data, I have identified a concern regarding the login activities conducted beyond Mexico's geographical borders. It is imperative to thoroughly investigate these login attempts for potential anomalies or security issues.

Here is an example of the code illustrating my creation of a SQL query aimed at filtering for login attempts that took place outside of Mexico.

<p align="center">
<img src="https://i.imgur.com/5j9AP74.png" height="70%" width="70%" alt="Azure Free Account"/>

The initial section of the screenshot displays my query, while the subsequent segment presents a portion of the output. This query is designed to retrieve all login attempts that transpired in countries apart from Mexico. To initiate, I commenced by selecting all data from the ```log_in_attempts table```. Subsequently, I employed a ```WHERE``` clause with ```NOT``` to refine the results, targeting countries other than Mexico. For this purpose, I utilized the ```LIKE``` operator with the pattern ```MEX%```, accommodating both ```MEX``` and ```MEXICO``` representations. The percentage sign (```%```) within ```LIKE``` signifies any number of unspecified characters.

## Retrieve Employees in Marketing
My team's objective is to upgrade the computers of specific employees within the Marketing department. This entails gathering information about the employees whose machines require updates.

Here's an example of the code illustrating my creation of a SQL query designed to filter for employee machines belonging to individuals within the Marketing department located in the East building.

<p align="center">
<img src="https://i.imgur.com/U8kAbvY.png" height="70%" width="70%" alt="Azure Free Account"/>

The initial section of the screenshot showcases my query, while the subsequent part presents a segment of the output. This query is intended to retrieve all employees situated within the Marketing department in the East building. To initiate, I commenced by selecting all data from the ```employees``` table. Following that, I incorporated a ```WHERE``` clause with an ```AND``` operator to refine the results, focusing on employees who are part of the Marketing department and are stationed in the East building. For this purpose, I utilized the ```LIKE``` operator with the pattern ```East%```, which accommodates the specific office numbers within the East building. The initial condition, ```department = 'Marketing'```, serves to filter employees in the Marketing department, and the second condition, ```office LIKE 'East%'```, does the same for employees in the East building.

## Retrieve Employees in Finance or Sales
The requirement extends to updating machines for employees within the Finance and Sales departments. Given the distinct security update requirements, the task involves obtaining information solely from employees belonging to these two departments.

Here's an example of the code illustrating my creation of a SQL query designed to filter for employee machines belonging to individuals within the Finance or Sales departments.

<p align="center">
<img src="https://i.imgur.com/iqwXXIx.png" height="70%" width="70%" alt="Azure Free Account"/>

The initial segment of the screenshot showcases my query, while the subsequent portion presents a segment of the output. This query is formulated to retrieve all employees affiliated with the Finance and Sales departments. To commence, I initiated by selecting all data from the ```employees``` table. Subsequently, I employed a ```WHERE``` clause with an ```OR``` operator to refine the results, capturing employees who belong to either the Finance or Sales departments. The choice of the ```OR``` operator is deliberate, aiming to encompass employees from either department. The initial condition, ```department = 'Finance'```, targets employees in the Finance department, and the second condition, ```department = 'Sales'```, does the same for employees in the Sales department.

## Retrieve All Employees not in IT
My team is required to implement an additional security update for employees who are outside the Information Technology department. Before executing the update, my initial task involves gathering relevant information about these employees.

Here's an example illustrating the creation of a SQL query designed to filter for employee machines belonging to individuals who are not part of the Information Technology department.

<p align="center">
<img src="https://i.imgur.com/H45W9rC.png" height="70%" width="70%" alt="Azure Free Account"/>

The initial segment of the screenshot showcases my query, while the subsequent part presents a segment of the output. This query is intended to retrieve all employees who are not part of the Information Technology department. Commencing the process, I selected all data from the ```employees``` table. Subsequently, I employed a ```WHERE``` clause featuring the ```NOT``` operator to refine the results, capturing employees who do not belong to the specified department.

## Summary
I employed filters in SQL queries to extract precise details from both the ```log_in_attempts``` and ```employees``` tables. Employing the ```AND```, ```OR```, and ```NOT``` operators, I tailored the filters to match the exact information required for each task. Additionally, I harnessed the ```LIKE``` operator in conjunction with the percentage sign (```%```) wildcard to isolate patterns in the data.
