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

#### <b>Result → Clean, relational model for advanced DAX and visuals.</b>

### 4️⃣ DAX Measures & Calculated Columns

Key measures:

Total Runs = SUM(fact_batting_summary[runs])
Total Innings = COUNT(fact_batting_summary[match_id])
Strike Rate = DIVIDE([Total Runs], [Balls Faced]) * 100
Batting Average = DIVIDE([Total Runs], [Innings Out])
Boundary % = DIVIDE([Boundary Runs], [Total Runs]) * 100

Calculated columns:

Boundary Runs = (fact_batting_summary[fours] * 4) + (fact_batting_summary[sixes] * 6)

Organized into folders:

⚔️ Batting

🎯 Bowling

🧤 Fielding

### 5️⃣ Dashboard Design (Power BI)

Developed a multi-page interactive dashboard with a clean, business-style layout.

#### 📄 Pages:

Power Hitters: Strike Rate > 140, Boundary% > 50, Avg > 30

Anchors & Middle Order: Consistency-focused players

All-Rounders & Bowlers: Wicket-takers with low economy

#### 📊 Visuals:

Scatter plots: Strike Rate vs Batting Average

Bar charts: Team-wise Runs & Boundaries

Player cards: Profile, Team, Batting Style, Key Stats

Dynamic slicers: Filter by Team, Stage, or Role

## 🧩 Selection Logic & Insights

### 🏏 Final XI (Team Earth)

| Role         | Player              | Key Strength             |
| ------------ | ------------------- | ------------------------ |
| Opener       | Jos Buttler (WK)    | Consistent & aggressive  |
| Opener       | Rilee Rossouw       | Explosive start          |
| Anchor       | Virat Kohli         | Stability & chase master |
| Anchor       | Suryakumar Yadav    | 360° stroke play         |
| Middle Order | Glenn Phillips      | Finisher                 |
| All-Rounder  | Marcus Stoinis      | Balance                  |
| All-Rounder  | Sikandar Raza       | Spin + Bat               |
| Spinner      | Shadab Khan         | All-round utility        |
| Bowler       | Sam Curran          | Wickets in powerplay     |
| Bowler       | Anrich Nortje       | Express pace             |
| Bowler       | Shaheen Shah Afridi | Death overs specialist   |


## Team Metrics:

Avg Score → 39.6

Strike Rate → 154.4

Economy → 6.0

Wicket Frequency → 1 per 11 balls

## ⚙️ Selection Parameters

Fast Bowlers: Economy < 7, Wickets/≤16 balls

All-Rounders: SR > 140, Bowling Avg < 25

Anchors: Avg > 35, SR > 130

Power Hitters: SR > 150, Boundary% > 60

## 💡 Learning Journey

This project was developed through self-learning and Codebasics resume challenges.
It reflects:

💻 Practical application of Power BI, DAX, and data modeling.

🤝 Collaboration with analysts on real dashboard projects.

🎓 Growth from learning to professional-grade delivery.

## 🎨 Dashboard Highlights

Custom visuals & player cards.

Clean Power BI theme with consistent colors.

Mockup-based layout planning for a corporate look.

Interactive KPIs and dynamic filters.

## 📊 Key Insights

Identified top performers through cross-metric analysis.

Developed a data-driven player selection model.

Showed how analytics can drive strategy in sports.

## 🧠 Tools & Technologies

| Category           | Tools                  |
| ------------------ | ---------------------- |
| Web Scraping       | Bright Data            |
| Data Cleaning      | Python (Pandas, Regex) |
| BI & Visualization | Power BI               |
| Data Source        | ESPN Cricinfo          |
| File Formats       | CSV, PBIX              |

## 🧩 Future Enhancements

🔄 Add live API-based updates.

📈 Include partnership and fielding analytics.

🎨 Introduce team-based color themes.

## 🏁 Outcome

✅ Fully functional interactive Power BI dashboard

✅ Demonstrated end-to-end analytics pipeline

✅ Showcased business storytelling and DAX mastery


# 🚀 Conclusion

This project bridges self-learning and professional BI practices — proving how determination and analytics can turn passion into results.

“Data doesn’t just tell a story — it builds champions.”

⭐ If you liked this project, star the repo and connect on LinkedIn!
