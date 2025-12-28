# Olympic-Athletes-Performance-Analysis-Power-BI
📌 Project Overview

This project explores 120 years of Olympic Games data (1896–2016) using Power BI. The goal is to analyze athlete participation, medal distribution, gender trends, country performance, and historical Olympic patterns through interactive dashboards.

The project focuses on direct data visualization in Power BI without prior SQL cleaning, demonstrating strong skills in:
- Data modeling
- DAX measures
- Dashboard design
- Business-style analytical storytelling

 📂 Dataset

Source: Kaggle – 120 Years of Olympic History: Athletes and Results

Files Used:

- athlete_events.csv

- noc_regions.csv (optional – for country mapping)

- Key Columns

- Name, Sex, Age, Height, Weight

- Team, NOC

- Year, Season, City

- Sport, Event

- Medal (Gold, Silver, Bronze, Blank)

🛠 Tools & Technologies

- Power BI Desktop

- DAX (Data Analysis Expressions)

- Kaggle Dataset

🔄 Data Preparation (Power BI)

- No SQL preprocessing was used.

- Minor transformations were done directly in Power BI:

- Changed data types (Year, Age, Height, Weight)

- Removed blank or null medals for medal-specific visuals

- Created relationships between athlete_events and noc_regions using NOC

📊 DAX Measures
Total Medals
```
Total Medals =
CALCULATE(
COUNTROWS('athlete_events'),
NOT(ISBLANK('athlete_events'[Medal]))
)
```
Total Athletes
```
Total Athletes = DISTINCTCOUNT('athlete_events'[ID])
```
Unique Countries
```
Unique Countries = DISTINCTCOUNT('athlete_events'[Team])
```
Total Events
```
Total Events = DISTINCTCOUNT('athlete_events'[Event])
```

## 📈 Dashboard Features
🔹 KPI Cards

- Total Athletes

- Total Medals

- Number of Participating Countries

- Total Olympic Events

🔹 Visualizations

- Line Chart: Medal trends over time

- Bar Chart: Top countries by medal count

- Stacked Column Chart: Medals by gender and sport

- Map: Global medal distribution


<img width="911" height="508" alt="Screenshot (48)" src="https://github.com/user-attachments/assets/2045186d-5c25-43f2-aede-4dfa2fdd4a4a" />


## 🔍 Key Insights

- Male participation historically dominated early Olympics, with steady female growth over time

- A small number of countries consistently dominate medal counts

- Certain sports contribute disproportionately to total medals

- Summer Olympics account for the majority of medals and athlete participation

