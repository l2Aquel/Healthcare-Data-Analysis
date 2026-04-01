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


## Business Impact & Insights

    
