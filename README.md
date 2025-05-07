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
| `project_proposal_dataset.csv`         | Final merged dataset with scraped home runs data                            |
| `project_proposal.ipynb`               | Updated analysis including regression and hypothesis testing                |
| `SP25 Project Proposal - Data Wrangling.docx` | Project description and data preparation notes                       |
| `Project Check-In Wrangling.pdf`       | Summary of findings and additional scraping details                         |

---

1. **Home Runs vs. Postseason Success**     
   Explore whether teams with more home runs are more likely to make or advance in the playoffs.

2. **Characteristics of Championship Teams**  
   Analyze the statistics of World Series champions to identify performance patterns.

3. **Key Batting Metrics for Wins**  
   Evaluate whether On-Base Percentage (OBP), Batting Average (BA), or Slugging Percentage (SLG) best predicts team success using regression.

4. **Predicting Team Wins**  
   Build machine learning models (e.g., linear regression) to identify which features—such as OBP, BA, SLG, HR, and RA—are most influential in determining team win totals.

5. **Attendance vs. Performance**  
   Investigate whether there is any relationship between **total home attendance** and team success, including wins and playoff qualification.

6. **Feature Evaluation and Model Refinement**  
   Use hypothesis testing and feature selection methods to determine which stats most meaningfully impact team outcomes and refine models accordingly.

## Data Cleaning Summary

* Mapped abbreviated team names to full names.  
* Removed irrelevant columns (e.g., opponent OBP/SLG, season rank).  
* Encoded the `Playoffs` column as binary (`Yes` = made playoffs, `No` = did not).  
* Scraped home run data from Baseball Reference and merged.  
* Scraped team-level home attendance from The Baseball Cube and added as a new column.  

## Data Dictionary

| Field                   | Type    | Description                                                                |
|------------------------|---------|----------------------------------------------------------------------------|
| `Team`                 | Text    | Abbreviation of team name (e.g., OAK, BOS)                                 |
| `Team Name`            | Text    | Full team name (e.g., Oakland Athletics)                                   |
| `League`               | Text    | American or National League                                                |
| `Year`                 | Numeric | Year of the season (excludes 1972, 1981, 1994, 1995 due to player strikes) |
| `Games`                | Numeric | Number of games played that season                                         |
| `Wins`                 | Numeric | Total wins by the team                                                     |
| `Home Runs`            | Numeric | Total home runs hit by the team                                            |
| `RS`                   | Numeric | Runs Scored                                                                |
| `RA`                   | Numeric | Runs Allowed                                                               |
| `OBP`                  | Numeric | On-Base Percentage (reaching base rate)                                    |
| `SLG`                  | Numeric | Slugging Percentage (total bases per at-bat)                               |
| `BA`                   | Numeric | Batting Average (hits per at-bat)                                          |
| `Playoffs`             | Logical | Binary indicator for playoff appearance (1 = Yes, 0 = No)                  |
| `PlayoffsFinish`       | Numeric | Final rank in the postseason (1 = World Series Winner)                     |
| `Total Home Attendance`| Numeric | Total fans attending home games (scraped and added)                        |

## Sources

* [Kaggle Dataset (Moneyball MLB Stats)](https://www.kaggle.com/datasets/wduckett/moneyball-mlb-stats-19622012)  
* [Baseball Reference (2012 Stats)](https://www.baseball-reference.com/leagues/majors/2012.shtml)  
* [The Baseball Cube (Attendance)](https://www.thebaseballcube.com/content/mlb_attendance/)  
