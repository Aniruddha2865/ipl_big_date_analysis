# 🏏 IPL Data Analysis with PySpark

> End-to-end exploratory data analysis of IPL matches (2008–2017) using Apache Spark  — covering player performance, team statistics, toss correlations, and season trends.

---

## 📌 Overview

This project analyzes Indian Premier League (IPL) data across multiple seasons using **PySpark** for large-scale data processing and **Matplotlib/Seaborn** for visualization. The dataset consists of 5 relational CSV files that are ingested, joined, and queried using the Spark DataFrame API and Window functions.

---

## 🗂️ Dataset

| File | Description |
|------|-------------|
| `Ball_By_Ball.csv` | Delivery-level match data (runs, extras, wickets) |
| `Match.csv` | Match metadata (teams, venue, toss, winner, MoM) |
| `Player.csv` | Player profiles (batting hand, bowling skill, country) |
| `Player_Match.csv` | Player-match participation and role details |
| `Team.csv` | Team names and IDs |

> Data covers IPL seasons **2008 to 2017**.

---

## 🛠️ Tech Stack

- **Apache Spark / PySpark** — DataFrame API, SparkSQL, Window Functions
- **Python** — Pandas, Matplotlib, Seaborn
- **Google Drive** — Dataset storage (mounted in Colab/Databricks)

---

## 🔍 Analysis Performed

### Match-Level
- Total matches per season
- Most wins by team across all seasons
- Toss winner vs match winner correlation
- Win type distribution (by runs vs by wickets)
- Top Man of the Match award winners

### Player-Level
- Top 10 run scorers overall
- Most boundaries (4s and 6s) hit
- Average runs per match per team
- Season-wise top scorers using **Window functions** (`rank`, `dense_rank`)

### Multi-Table Joins
- Ball-by-ball data enriched with match and player details
- Player names resolved via join with Player table
- Man of the Match linked with player country data

### Visualizations
- 📊 Top 10 teams by total wins (bar chart)
- 📈 Total runs scored per season (trend line)
- 🏅 Player performance breakdowns

