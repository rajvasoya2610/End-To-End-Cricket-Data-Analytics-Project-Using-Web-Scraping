# 🏏 Cricket Data Analytics Project – T20 World Cup 2022 (End-to-End Power BI Dashboard)

## 📘 Overview

This end-to-end analytics project demonstrates a complete data journey — from web scraping and Python cleaning to Power BI modeling, DAX calculations, and interactive dashboard design.

It uses real-world data from the T20 Cricket World Cup 2022, framed through a creative storyline:

“Team xxxx must select the best XI to face Team yyyy  — using pure data analytics.”

This project showcases technical precision, analytical logic, and storytelling — a perfect example of how data can power decision-making in sports.


## 🎯 Objectives

🕸️ Collect and transform cricket data from ESPN Cricinfo using Bright Data.

🧹 Clean, structure, and merge data with Python (Pandas).

🧩 Design a star schema data model in Power BI.

📊 Build DAX measures and visualizations for insight generation.

🏆 Create an interactive dashboard to select Team Earth’s Best XI.

This project showcases technical precision, analytical logic, and storytelling — a perfect example of how data can power decision-making in sports.

## 🧠 Project Workflow

### 1️⃣ Data Collection

Used Bright Data’s Data Collector to scrape detailed match data.

Extracted multiple datasets:

🏟️ Match summaries

🏏 Batting and bowling scorecards

👥 Player profiles

Exported data as CSVs for cleaning and transformation.

### 2️⃣ Data Cleaning (Python)

Tech stack: Python, Pandas, NumPy, Regex

Key cleaning steps:

#### Example: Clean team names and handle reversed labels
df['Team'] = df['Team'].str.replace('*', '', regex=False)
df['match_id'] = df['Team1'] + "_vs_" + df['Team2']

Tasks performed:

Removed unwanted symbols and standardized names.

Created match_id as a unique relational key.

Merged datasets into clean CSVs:

dim_match_summary.csv  
dim_players.csv  
fact_batting_summary.csv  
fact_bowling_summary.csv

### 3️⃣ Data Modeling (Power BI)

Built a star schema with:

🧮 Fact Tables: Batting, Bowling, Match Summary

👤 Dimension Tables: Players, Matches

Relationships:

fact_batting_summary  ➜  dim_players  
fact_bowling_summary  ➜  dim_players  
fact_batting_summary  ➜  dim_match_summary  
fact_bowling_summary  ➜  dim_match_summary

#### <b>Result → Clean, relational model for advanced DAX and visuals.<\B>
