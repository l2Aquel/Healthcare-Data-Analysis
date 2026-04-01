# Healthcare-Data-Analysis

## 1. Project Title / Headline
An end-to-end data analytics project that explores ride booking performance for Ola in Bengaluru, India. Built with Power BI for visual analytics and SQL for backend querying, this project uncovers insights on ride volume, cancellations, customer behavior, and revenue trends for over 100,000 simulated bookings.

## 2. Short Description / Purpose

## 3. Tech Stack
This project leverages the following technologies:
- **Power BI Desktop**   
- **Power Query**
- **DAX (Data Analysis Expressions)** 
- **Data Modeling** 
- **Excel** - 
- **SQL Server Studio Management/ SQL**  
- **File Types** – `.pbix`, `.sql`, `.pdf`,`.csv`

## 4. Data Source


## 5. Features / Highlights
### • Business Problem

### • Goal of the Dashboard



### • Walkthrough of Key Power BI Visuals


## 6. Screenshots / Demos



## SQL Logic & Insights

1. Patient Demographics: Provide a count of patients grouped by their RACE,GENDER,MARITAL STATUS AND ETHINICITY.
> SELECT gender,count(*) as patients_as_gender
FROM [hospital_db].[dbo].[patients]
GROUP BY gender;

> SELECT race,count(*) as patients_as_race
FROM [hospital_db].[dbo].[patients]
GROUP BY race;

> SELECT marital_status,count(*) as patients_as_marital_status
FROM [hospital_db].[dbo].[patients]
GROUP BY marital_status;

> SELECT ethnicity,count(*) as patients_as_ethnicity
FROM [hospital_db].[dbo].[patients]
GROUP BY ethnicity;

2. Patients Check: List the cities and no of patients from each city from high to low
> SELECT city,COUNT(*) AS total_patients
FROM [hospital_db].[dbo].[patients]
GROUP BY city
ORDER BY total_patients DESC;

3. Encounters over the years: Find the no of encounters over the years and order them according to years older to recent
> SELECT YEAR(start) as year,COUNT(*) AS total_encounters 
FROM [hospital_db].[dbo].[encounters]
GROUP BY  YEAR(start)
ORDER BY YEAR(start);

4. Top Healthcare Payers: List the Payers that have covered the highest number of encounters AND also the highest amount of encounters
> SELECT TOP 5 p.name as payer,COUNT(e.payer_coverage) AS total_encounters_covered
FROM [hospital_db].[dbo].[encounters] e
JOIN [hospital_db].[dbo].[payers] p ON e.payer = p.id
WHERE name != 'NO_INSURANCE'
GROUP BY p.name
ORDER BY total_encounters_covered DESC;

> SELECT TOP 5 p.name as payer,ROUND(SUM(e.payer_coverage),2) AS total_amount_covered
FROM [hospital_db].[dbo].[encounters] e
JOIN [hospital_db].[dbo].[payers] p ON e.payer = p.id
WHERE name != 'NO_INSURANCE'
GROUP BY p.name
ORDER BY total_amount_covered DESC;

5. Specific Condition Search: Find all patients (First and Last name) who have a REASONDESCRIPTION of 'Hyperlipidemia'.
> SELECT p.first_name,p.last_name,reason_description
FROM [hospital_db].[dbo].[encounters] e
JOIN [hospital_db].[dbo].[patients] p ON e.patient = p.id
WHERE reason_description = 'Hyperlipidemia'
GROUP BY p.first_name,p.last_name,reason_description;






## Business Impact & Insights

    
