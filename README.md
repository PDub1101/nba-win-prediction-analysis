# NBA Team & Player Analytics: Predicting Winning Percentage

An end-to-end data analytics and statistical modeling project analyzing NBA team and player performance metrics to determine the key drivers of winning percentage in the modern NBA.

Created as the Final Project for **CS 2316: Data Manipulation & Analysis** at the **Georgia Institute of Technology**.

---

## Project Overview

What factors most strongly dictate team success in the modern NBA? This project builds a multi-source data extraction pipeline and statistical modeling framework to analyze the impact of offensive efficiency, defensive rating, shot selection (3-point volume and interior shooting), and game pace on winning outcomes.

### Core Research Questions & Hypotheses
1. **Offensive vs. Defensive Rating**: Does elite defense contribute more reliably to winning percentage than explosive offense?
2. **Three-Point Revolution**: How strongly does three-point volume and efficiency correlate with regular-season win totals?
3. **Shot Quality & Distance**: How do close-range (layups/dunks) vs. perimeter shot distributions affect overall team rating?

---

## Data Pipeline & Architecture

The project integrates three distinct data sources into clean, standardized datasets located in `data/`:

| Source | Collection Method | Description | Output File |
| :--- | :--- | :--- | :--- |
| **NBA Stats API** (`nba_api`) | REST API | Multi-season team advanced metrics (Offensive/Defensive Rating, Net Rating, Pace, eFG%) | `data/nba_api_team_stats.csv` |
| **Basketball Reference** | HTML Web Scraping (`pandas.read_html`) | Team shooting breakdowns by shot distance, layups, and dunks | `data/nba_shooting_cleaned.csv` |
| **Play-by-Play Data** | File parsing & regex transformation | Raw game event streams aggregated into individual player contributions | `data/cleaned_player_data.csv` |

---

## Repository Structure

```
nba-win-prediction-analysis/
├── NBA_Analytics_and_Win_Prediction.ipynb      # Main Phase 3 analysis and modeling notebook
├── Phase_II_Data_Collection_and_Cleaning.ipynb # Phase 2 data extraction and pipeline notebook
├── data/                                       # Cleaned datasets and API JSON samples
│   ├── cleaned_player_data.csv
│   ├── nba_api_team_stats.csv
│   ├── nba_shooting_cleaned.csv
│   └── nba_api_pretty.json
├── docs/                                       # Presentation slides and project overview
│   ├── CS 2316 Final Project.pptx
│   └── One Pager.pdf
├── visualizations/                             # Generated plots and figure exports
└── .gitignore
```

---

## Requirements & Setup

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/nba-win-prediction-analysis.git
cd nba-win-prediction-analysis
```

### 2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn nba_api lxml
```

### 3. Run the notebook
```bash
jupyter notebook NBA_Analytics_and_Win_Prediction.ipynb
```
