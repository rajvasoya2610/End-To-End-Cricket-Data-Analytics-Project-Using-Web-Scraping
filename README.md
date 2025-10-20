# End-To-End-Cricket-Data-Analytics-Project-Using-Web-Scraping

📘 Overview

This end-to-end analytics project showcases a full data journey — from web scraping and Python data cleaning to Power BI data modeling, DAX, and dashboard design.

It’s built on real-world data from the T20 Cricket World Cup 2022, creatively framed as a mission to help Team Earth pick the best XI players to defeat aliens on “Planet Sporta.”

The dashboard combines statistical logic, data modeling, and storytelling to deliver actionable insights — demonstrating how data analytics can solve complex selection and performance problems in sports.

🎯 Objectives

Collect and transform raw cricket data from ESPN Cricinfo using Bright Data.

Clean and model the data using Python (Pandas) and design a star schema in Power BI.

Apply DAX to create meaningful performance metrics.

Build an interactive dashboard to analyze player performances and select the Best XI.

Showcase real analytical thinking and business presentation skills in dashboard storytelling.

🧠 Project Workflow

1️⃣ Data Collection

Used Bright Data’s Data Collector to scrape detailed match data from ESPN Cricinfo.

Extracted multiple datasets:

Match summaries

Batting and bowling scorecards

Player profiles

Exported and consolidated CSVs for analysis.

2️⃣ Data Cleaning (Python)

Cleaned and standardized names, match labels, and team entries.

Added derived fields using lambda functions and regex.

Created unique match_id values to connect tables.

Produced structured CSV files:

dim_match_summary.csv

dim_players.csv

fact_batting_summary.csv

fact_bowling_summary.csv
