# cricket-analysis
An end-to-end analysis of  cricket  to uncover insights and players performance

# 🏏 T20 World Cup Cricket Data Analysis

## 🎯 Overview
This project is an **end-to-end sports data analytics** showcase, demonstrating proficiency in **data extraction**, **transformation**, and **interactive visualization**. The project processes T20 World Cup cricket data (16 Oct – 13 Nov 2022) from **raw, semi-structured JSON files** into a structured, analysis-ready format. The final deliverable is an **interactive Power BI dashboard** that provides insights into:

- **Batsmen and bowlers’ performance metrics**
- **Historical match results**
- **Overall team and player comparisons**

## 🛠️ Tools & Technologies

| **Category**         | **Tool / Library** | **Purpose**                                        |
|----------------------|--------------------|----------------------------------------------------|
| **Data Source**       | GitHub Repository  | Source of the raw T20 World Cup JSON files         |
| **Data Processing**   | Python             | Language for ETL and transformation                |
| **Data Manipulation** | Pandas             | Data cleaning, reshaping, and feature engineering  |
| **Data Storage**      | JSON (input), CSV / Excel (output) | Input and output data formats           |
| **Visualization**     | Power BI           | Building the final dashboard                      |

---

## 📊 Dataset

### Raw Data (Input):

- `t20_wc_match_results.json`
- `t20_wc_batting_summary.json`
- `t20_wc_bowling_summary.json`
- `t20_wc_player_info.json`

### Processed Data (Output):

- `fact_batting_summary.csv`
- `fact_bowling_summary.csv`
- `dim_players.xlsx`
- `dim_match_summary.xlsx`

---

## ⚙️ ETL Process (Python + Pandas)

All transformation steps were developed in Jupyter Notebook: `CRICKET_ETL.ipynb`.

### 1. Data Ingestion & Transformation
- Loaded four JSON files into Pandas DataFrames.
- Flattened nested JSON structures (e.g., player records).

### 2. Data Cleaning & Modeling
- Removed non-ASCII characters (â€, †, \xa0).
- Created `Match_ID` mapping for consistent joins.
- Derived Out/Not Out status using conditional logic.

### 3. Data Export
- Exported cleaned DataFrames to CSV and Excel for Power BI:
  - `fact_batting_summary.csv`, `fact_bowling_summary.csv`
  - `dim_players.xlsx`, `dim_match_summary.xlsx`

---

## 📈 Dashboard & Analysis (Power BI)

The Power BI report (`CRICKET_Analysis.pbix`) includes multiple analytical views segmented by player roles.

### 🧮 Custom DAX Measures

#### **Batting Metrics:**
- Total Runs
- Total Outs
- Total Balls Faced
- Batting Average
- Strike Rate
- Boundary %
- Batting Position
- Average Balls Faced (per Player/Team)

#### **Bowling Metrics:**
- Balls Bowled
- Runs Conceded
- Bowling Average
- Bowling Economy
- Bowling Strike Rate
- Dot Ball Percentage
- Total Innings

---

## 📊 Dashboard Pages

| **Page**           | **Focus**                                   | **Key Metrics**                                 |
|--------------------|---------------------------------------------|-------------------------------------------------|
| **Power Hitters**   | Aggressive batsmen during Powerplay/Death overs | Strike Rate, Boundary %, Avg Balls Faced      |
| **Anchors**         | Stable middle-order players                | Batting Average, Total Innings, Total Runs     |
| **Finishers**       | Players excelling in final overs           | Strike Rate, Runs per Match, Total Outs        |
| **Bowlers**         | Wicket-takers and economy controllers      | Bowling Average, Strike Rate, Dot Ball %, Economy |
| **Player Details**  | Granular, comprehensive view of individual performance | Batting and Bowling Metrics (History)       |

---

## ⭐ Results & Insights

The completed project successfully transforms **raw, unstructured data** into actionable intelligence, enabling users to:

- **Player Efficiency:** Compare strike rates, averages, and consistency.
- **Top Performers:** Identify top scorers and best bowlers.
- **Team Trends:** Analyze team performance trends, such as effectiveness at limiting opponents via runs conceded or dot ball %.
