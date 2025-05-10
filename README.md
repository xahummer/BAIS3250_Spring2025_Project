# Moneyball MLB Analysis (1962-2012)

## Overview
Inspired by the “Moneyball” philosophy of Billy Beane, this project examines how specific baseball statistics affect team success. Using historical MLB data from 1962–2012, we analyze relationships between hitting metrics and outcomes like total wins, playoff appearances, and World Series victories. We aim to provide data-driven insights into what truly contributes to winning baseball.

## Group Members
* Xavier Hummer
* Jacob Kronlage
* Ryan Perry

## Files Included

| File Name                              | Description                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| `baseball.csv`                         | Cleaned dataset from Kaggle (1962–2012)                                     |
| `project_proposal_dataset.csv`         | Merged dataset with early home run data                                     |
| `final_project_dataset.csv`            | Fully cleaned, final dataset with all features used in modeling             |
| `attendance_df.csv`                    | Team-level total home attendance figures scraped from The Baseball Cube     |
| `homerun_df.csv`                       | Season-level home run data scraped from Baseball Reference                  |
| `project_final_code.ipynb`             | Final Jupyter Notebook with full analysis and models                        |
| `SP25 Project Proposal - Data Wrangling.docx` | Original proposal and data prep notes                                |
| `Final Project - Wrangling.docx`       | Full project write-up with detailed methodology and visuals                 |
| `Project Check-In Wrangling.pdf`       | Interim progress update and scraping summary                                |

---

## Analysis Questions

1. **Do Home Runs Predict Postseason Success?**     
   Explore whether teams with more home runs are more likely to make or advance in the playoffs.

2. **What Statistics Predict Team Wins Best?**  
   Evaluate whether On-Base Percentage (OBP), Batting Average (BA), Slugging Percentage (SLG), or other metrics best predict team success using regression.

3. **Is There a Relationship Between Attendance and Performance?**  
   Investigate whether there is any relationship between total home attendance and team success, including wins and playoff qualification.

## Data Cleaning Summary

* Mapped abbreviated team names to full names.  
* Removed irrelevant columns (e.g., opponent OBP/SLG, season rank).  
* Encoded the `Playoffs` column as binary (`Yes` = made playoffs, `No` = did not).  
* Scraped home run data from Baseball Reference and merged.  
* Scraped team-level home attendance from The Baseball Cube and added as a new column.  

## Data Dictionary

| Field                   | Type    | Description                                                                 |
|------------------------|---------|-----------------------------------------------------------------------------|
| `Team`                 | Text    | Abbreviation of full team name.                                             |
| `Team Name`            | Text    | Full name of the team.                                                      |
| `League`               | Text    | Which league the team is in (American or National).                         |
| `Year`                 | Numeric | Which year the season was played in.                                        |
| `Games`                | Numeric | Number of regular season games played.                                      |
| `Wins`                 | Numeric | Number of regular season wins.                                              |
| `Home Runs`            | Numeric | Total number of regular season home runs hit collectively as a team.        |
| `RS`                   | Numeric | Total number of runs scored as a team. (Regular Season Only)                |
| `RA`                   | Numeric | Total number of runs allowed as a team. (Regular Season Only)               |
| `OBP`                  | Numeric | On Base Percentage – The percentage of a team’s plate appearances that result in a player reaching base. (Regular Season Only) |
| `SLG`                  | Numeric | Slugging Percentage – A team’s average number of total bases earned per at-bat. (Regular Season Only) |
| `BA`                   | Numeric | Batting Average – The team’s percentage of at-bats that result in a hit. (Regular Season Only) |
| `Playoffs`             | Logical | Yes or no if the team made the playoffs.                                    |
| `PlayoffsFinish`       | Numeric | Final team ranking in postseason – e.g., World Series Winner = 1.0          |
| `Total Home Attendance`| Numeric | Total number regular season home game attendance.                           |
| `Attendance Bin`       | String  | Labeled groupings of total regular season home attendance.                  |

---

## References

- **Kaggle Dataset**: [Baseball Reference MLB Team Stats (1962–2012)](https://www.kaggle.com/datasets)  
- **Baseball Reference**: [https://www.baseball-reference.com](https://www.baseball-reference.com)  
- **The Baseball Cube**: [https://www.thebaseballcube.com](https://www.thebaseballcube.com)  
