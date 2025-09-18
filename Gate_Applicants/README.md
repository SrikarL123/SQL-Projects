Project Title: GATE 2019 Applicant Data Analysis
Executive Summary
This project is a data cleaning and analysis task designed to process a raw dataset of GATE (Graduate Aptitude Test in Engineering) applicants and extract a clear, concise list of the top 15 most popular papers based on application numbers in 2019. Using targeted SQL queries, the project transforms the initial dataset into a clean, insightful, and easy-to-understand report on engineering education trends.

The Objective
The primary goal was to answer a key question: "Which engineering disciplines were the most sought-after by GATE applicants in 2019?" The initial data contained extraneous columns (like id) and included information from multiple years. The objective was to refine this data to produce a clean, ranked list that specifically highlights the most popular fields for the year 2019.

The Process
The project was executed through a two-step SQL pipeline, demonstrating an efficient workflow for data cleaning and analysis.

Data Cleaning: The first step was to simplify the table for analysis. The id column, which served as a primary key but was irrelevant to the applicant count, was removed from the gate_applicants table. This made the dataset cleaner and more focused.

ALTER TABLE gate_applicants
DROP COLUMN id;

Analysis and Ranking: A single query was then used to filter, sort, and select the final data. This involved three key actions:

Filtering by Year: The data was filtered  WHERE year = 2019 to ensure the analysis was specific to the target year.

Ranking by Popularity: The results were sorted in descending order  ORDER BY applied DESC to rank the papers from most to least popular.

Limiting the Output: Finally, the query was limited to the LIMIT 15 results to produce a concise "Top 15" report.

SELECT * FROM gate_applicants
WHERE year = 2019
ORDER BY applied DESC
LIMIT 15;

The Result
The final output is a clean, organized table displaying the top 15 GATE papers from 2019, ranked by the number of applicants. The list reveals key insights into student preferences, showing that traditional disciplines like Mechanical Engineering, Civil Engineering, and Computer Science attracted the highest number of candidates.

Value and Application
This project serves as a practical example of how to derive meaningful insights from raw data:

For Educational Insights: This type of analysis can help educational institutions and policymakers understand trends in engineering. It highlights which disciplines are most in demand, which can inform decisions on resource allocation and curriculum focus.

As a Technical Showcase: It demonstrates fundamental SQL skills in data cleaning (ALTER TABLE) and data analysis (SELECT, WHERE, ORDER BY, LIMIT). It shows the ability to take a dataset, define a clear question, and write efficient code to deliver a valuable answer.
