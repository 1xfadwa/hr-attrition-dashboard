HR Attrition Dashboard (Power BI)
An interactive two-page Power BI dashboard that analyzes employee attrition in the IBM HR Analytics dataset. Built as a hands-on HR analytics project: data cleaning in Power Query, DAX measures, dashboard design, and turning numbers into findings an HR Business Partner could act on.
 
 
Business question
Where is employee attrition concentrated? Which groups of employees are most likely to leave? What might explain it, and how should HR respond?
Data
•	Source: IBM HR Analytics Employee Attrition & Performance (Kaggle). A fictional dataset created by IBM data scientists, so no real employee data is used.
•	Size: 1,470 employees, 35 columns.
•	Cleaning (Power Query): 
o	Checked every column for empty values and errors (none found).
o	Dropped DailyRate, HourlyRate, MonthlyRate because their definitions are unclear and they do not track MonthlyIncome.
o	Dropped Over18 and StandardHours because they hold a single value for every employee.
o	Shortened department names to HR, R&D, Sales for readable charts.
Tools and techniques
Power BI Desktop, Power Query, DAX (CALCULATE, DIVIDE, ALL, SWITCH), calculated columns, filter context, custom theme (JSON).
Key measures
Measure	Idea
Attrition rate	Leavers divided by employees, using DIVIDE
High Performer Attrition Rate	Leavers with the top performance rating divided by all top performers
Share of Leavers	Each group's leavers divided by all leavers, using ALL to ignore the group filter
Age Group (calculated column)	SWITCH(TRUE(), ...) bands: 18-29, 30-39, 40-49, 50+
Dashboard pages
1.	Attrition Overview: headline numbers, attrition by department, age group and marital status, plus key findings.
2.	Details: department breakdown table with headcount, leavers, rates and share of leavers.
Key findings
•	Overall attrition is 16.1% (237 of 1,470 employees).
•	By department: Sales has the highest rate (20.6%). R&D has the largest share of leavers (56.1%) but the lowest rate (13.8%) because it is the largest department. HR shows 19.0% but has only 63 employees.
•	By age: employees aged 18-29 leave at 27.9%. They are 22% of employees but about 38% of leavers.
•	By marital status: single employees leave at 25.5%, versus 12.5% for married and 10.1% for divorced. The gap remains inside the 18-29 group, so age alone does not explain it.
•	High performers leave at 16.4%, close to the company average of 16.1%.
Limitations
•	The data is a single snapshot with no dates, so trends over time cannot be analyzed.
•	It is a fictional dataset.
•	Small groups (for example HR, with about 9 high performers) produce unstable rates and should be read with caution.
•	Findings show association, not causation. Age and marital status were used to understand patterns, not to guide decisions about individuals.
Recommendations
1.	Sales: Because Sales has the highest attrition rate (20.6%), I recommend first checking workload, then offering targeted incentives and more flexible working hours, and I would track Sales attrition every quarter.
2.	Early-career employees: Because employees aged 18-29 leave at 27.9% (about 38% of all leavers), I recommend comparing their pay with the market and holding one-to-one conversations to uncover hidden reasons (such as a planned career change), and I would track attrition in this group together with the reasons given.
3.	Next analysis: Because promotion and work-life balance are plausible explanations that this dashboard does not test, I recommend analyzing years since last promotion and work-life balance for leavers versus stayers, and I would track the gap between the two groups.
How to open
Open hr-attrition-dashboard.pbix with Power BI Desktop (Windows). A PDF export is included as dashboard.pdf.
Author
Fadwa Abdullah Barnawi · www.linkedin.com/in/fadwa-abdullah · https://github.com/1xfadwa



In which sectors is the turnover concentrated?
Which employee categories are leaving the most?
What might explain this, and how does HR respond?
