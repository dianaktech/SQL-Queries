<h1>🛢️ Applying filters to SQL queries</h1>

<h2>Description</h2>
I am a security professional at a large organization. Part of my job is to investigate security issues to help keep the system secure. I recently discovered some potential security issues that involve login attempts and employee machines.
My task is to examine the organization’s data in their <b>employees</b>  and <b>log_in_attempts</b>  tables. I will use SQL filters to retrieve records from different datasets and investigate the potential security issues.
<br />


<h2>Retrieve after hours failed login attempts</h2>

 I recently discovered a potential security incident that occurred after business hours. To investigate this, I need to query the log_in_attempts table and review after hours login activity. I will be using filters in SQL to create queries that identify all failed login attempts that occurred after 18:00.
<p align="center">
<img src="https://imgur.com/A8O2dtN.png" height="700%" width="70%" alt="after hours"/> 
  
Using the command:

 <b>SELECT *

FROM log_in_attempts

WHERE login_time > '18:00' AND success = FALSE;</b> 

I was able to determine there were 19 failed login attempts that occurred after 18:00.

<h2>Retrieve login attempts on specific dates </h2>
A suspicious event occurred on 2022-05-09. To investigate this event, I want to review all login attempts which occurred on this day and the day before. Using filters in SQL I will create a query that identifies all login attempts that occurred on 2022-05-09 or 2022-05-08.
<img src="https://imgur.com/E6qvFM8.png" height="700%" width="70%" alt="after hours"/> 

Using the command:

<b>SELECT * 

FROM log_in_attempts 

WHERE login_date = '2022-05-09' OR login_date = '2022-05-08'; </b>  

I was able to determine there were 75 login attempts on these two days


<h2>Retrieve login attempts outside of Mexico</h2>

There’s been suspicious activity with login attempts, but the team has determined that this activity didn't originate in Mexico. I need to investigate login attempts that occurred outside of Mexico. 


<img src="https://imgur.com/tkPp0p7.png" height="80%" width="80%" alt="display"/>
<img src="https://imgur.com/FP4T7uk.png" height="40%" width="40%" alt="display"/>

Using the command:

<b>SELECT * 

FROM log_in_attempts 

WHERE NOT country LIKE 'MEX%';</b>  

I was able to determine that 144 login attempts did not originate in Mexico. </b>  

<h2>Retrieve employees in Marketing</h2>

The team wants to perform security updates on specific employee machines in the Marketing department. I am responsible for getting information on these employee machines and will need to query the employees table. Using filters in SQL I will create a query that identifies all employees in the Marketing department for all offices in the East building.


<img src="https://imgur.com/U03iV3V.png" height="80%" width="80%" alt="remove"/>

Using the command:

<b>SELECT * 

FROM employees 

WHERE department = 'Marketing' AND office LIKE 'East%';</b>  

I was able to determine there were 7 employee machines in the marketing department at the East building. </b>  

<h2>Retrieve employees in Finance or Sales</h2>
The team now needs to perform a different security update on machines for employees in the Sales and Finance departments  and I need to locate information on these employees.

<img src="https://imgur.com/7S6S4BH.png" height="80%" width="80%" alt="remove"/>

Using the command:

<b>SELECT * 

FROM employees 

WHERE department = 'Finance' OR department = 'Sales';</b>  

I was able to determine there were 71 employees in these departments located in different offices.

<h2>Retrieve all employees not in IT</h2>
The team needs to make one more update to employee machines. The employees who are in the Information Technology department already had this update, but employees in all other departments need it.

<img src="https://imgur.com/VzOe4Ai.png" height="80%" width="80%" alt="remove"/>

Using the command:

<b>SELECT * 

FROM employees 

WHERE NOT department= 'Information Technology’;</b> 

I was able to determine that 161 employees are not in the Information Technology department 

<h2>*All of the  screen shots with the results were not included for sizing purposes</h2>

<h2>Summary</h2>

 I applied filters to SQL queries to get specific information on login attempts and employee machines. I used two different tables, log_in_attempts and employees. I used the AND, OR, and NOT operators to filter for the specific information needed for each task. I also used LIKE and the (%) wildcard to filter for patterns.
