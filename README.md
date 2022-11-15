# Pewlett-Hackard-Analysis

## Overview of the analysis
Pewlett Hackard is a large company boasting several thousand employees and it's been around for a long time.
It is looking toward the future in two ways.  First, it's offering a retirement package for those who meet certain criteria.
Second, it's starting to think about which positions will need to be filled in the  near future. 
The number of upcoming retirements will leave thousands of job openings.
This analysis will help future-proof Pewlett Hackard by generating a list of all employees eligible for the retirement package.
The epployee data we need is only available in the form of six CSV files because Pewlett Hackard has been mainly using Excel and VBA to work with their data.
Our task is to build an employee databasee with SQL.
In this assignment we need to determine the number of retiring employees per title, and identify employees who are eligible to participate in a mentorship
program to help the manager prepare for the upcoming "silver tsunami."  

## Results
- To visualize and identify the relationship of the data from 6 different files we needed to create ERDs (Entity Relationship Diagrams).
![pic](https://github.com/ElenaMasarsky/Pewlett-Hackard-Analysis/blob/main/Resources/EmployeeDB.png)  

- Using the ERD we created, we built a Retirement Titles table that holds all the titles of employees who were born between January 1, 1952 and December 31, 1955.
Because some employees may have multiple titles in the database—for example, due to promotions - we used the DISTINCT ON statement to create a table that contains the most recent title of each employee.
Then, we used the COUNT() function to create a table that has the number of retirement-age employees by most recent job title.
Finally, because we wanted to include only current employees in our analysis, we excluded those employees who have already left the company by filtering on to_date to keep only those dates that are equal to '9999-01-01'.  
![pic](https://github.com/ElenaMasarsky/Pewlett-Hackard-Analysis/blob/main/Resources/Retirement%20Titles%20table.png)  

- Then we retrieved the number of employees by their most recent job title who are about to retire. This table shows us how that 72,458 positions Pewlett Hackard needs to fill in the next few years.  
![pic](https://github.com/ElenaMasarsky/Pewlett-Hackard-Analysis/blob/main/Resources/retiring_titles.png)  

- Using the ERD we created a mentorship-eligibility table that holds the current employees who were born between January 1, 1965 and December 31, 1965 and who are eligible to participate in mentorship program.
![pic](https://github.com/ElenaMasarsky/Pewlett-Hackard-Analysis/blob/main/Resources/mentorship_eligibility.png)



## Summary

How many roles will need to be filled as the "silver tsunami" begins to make an impact?

Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?

As the "silver tsunami" begins to make an impact there are 72,458 roles will need to be filled.

