# COVID-19-Global-Impact-Vaccination-Analysis

 Project Overview

This project delivers an automated end-to-end data analytics pipeline that ingests raw, cumulative global time-series pandemic logs, cleans anomalies using Python, and builds an interactive, executive-level dashboard in Power BI.
The goal of this dashboard is to provide public health stakeholders with a unified view to track daily infection waves, evaluate global mortality balances, and analyze the direct impact of vaccine distribution campaigns.

Technology Stack

•	Data Pipeline & Cleaning: Python via Google Colab

•	Business Intelligence & Visualization: Power BI Desktop

•	Data Modeling: DAX Time-Intelligence Measures


Data Transformation Pipeline Steps

Because raw pandemic repositories record numbers as cumulative totals, loading the raw CSV directly causes mathematical errors and duplicate counting. The automated Python pipeline handles the following heavy lifting:

1.	Ingestion & Filtering: Loads the core dataset and isolates essential tracking fields (total_cases, new_cases, total_deaths, total_vaccinations, etc.).

2.	Handling Gaps: Removes messy regional aggregate entries (like 'World' or 'Europe') to protect map accuracy, and zero-pads empty cells from early-pandemic timelines.

3.	Data Type Correction: Converts arbitrary text elements into unified system date and numeric classifications.

4.	Delta Calculation: Employs rolling window .diff() calculations grouped by country to extract true standalone daily increments from cumulative milestones.


Key Analytical Insights


•	Vaccines Flatten the Curve: The dashboard line chart clearly shows that daily new infection waves started dropping quickly once a country reached a 60% vaccination coverage milestone.

•	Low Global Death Rate: The global Case Fatality Rate stabilized at a low 0.15%, though early data showed temporary spikes in regions with limited hospital testing capacity.

•	Massive Case Spikes in Densely Populated Nations: Large, highly populated countries like the United States (99M cases) and India (45M cases) saw the highest overall numbers due to large population centers.

•	Successful Booster Drive Acceleration: Global vaccine deployment quickly reached a massive baseline scale of 10 billion administered doses, which acted as a major defense layer against newer variant spikes later in the timeline.
 
 How to Run and View the Project
 
1.	Python Scripting: Run the cleaning script in Google Colab to output the streamlined covid_final_cleaned.csv.
2.	Power BI Load: Open Power BI Desktop, select Get Data ➔ Text/CSV, and select the cleaned file.
3.	Interactive Exploration: Use the Country Dropdown Dropdown and Timeline Slider at the top right of the dashboard canvas to dynamically cross-filter all cards, charts, and global maps.

