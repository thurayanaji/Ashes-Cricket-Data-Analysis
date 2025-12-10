
# **Ashes 2017–18 Batting Performance Analysis**  
### *Text Data Cleaning, Tidy Data, and EDA in R*

---

## **1. Project Overview**
This project analyses batting performances in the 2017–18 Men’s Ashes series (Australia vs England). Starting from text-based descriptions of each innings, the data is cleaned, reshaped, and converted to tidy format, then explored using visualisation and summary statistics.

Completed as part of my **Postgraduate Certificate in Applied Data Science**.

---

## **2. Objectives**
- Transform raw text into a structured, tidy dataset  
- Extract key numeric features (batting position, runs, balls faced)  
- Explore scoring patterns and differences between teams  
- Investigate scoring rate (runs per ball) and its relationship with balls faced  
- Summarise team composition by player roles

---

## **3. Data Summary**
Source: Ashes 2017–18 batting records for each player and innings.  
Key variables after cleaning:
- **batter** – player name  
- **team** – Australia or England  
- **role** – batter, bowler, allrounder, wicketkeeper  
- **innings** – Test and innings identifier  
- **score** – runs scored  
- **balls_faced** – balls faced  
- **scoring_rate** – runs per ball  

Initial data was in wide format with performance stored as long text; it was converted to long, tidy format.

---

## **4. Methods**

### **Data Wrangling & Cleaning**
- Used `pivot_longer()` to convert wide to long structure (one row per player per innings)  
- Used `stringr::str_match()` to extract:
  - batting position  
  - runs scored  
  - balls faced  
- Converted variables to appropriate types (factors and integers)  
- Cleaned factor levels (e.g. “English” → “England”, “bowl” → “bowler”)

### **Exploratory Analysis**
- Histogram of **scores** to study distribution and outliers  
- Faceted histograms and boxplots of **scores by team**  
- Scatterplots:
  - **score vs balls_faced** (relationship between time at crease and runs)  
  - **scoring_rate vs balls_faced** (aggression vs innings length)  
- Bar charts and proportion tables for **roles by team**

---

## **5. Key Findings**
- Score distribution is **right-skewed**: many low scores, a few very high innings  
- Australia generally shows **higher median scores and more high outliers** than England  
- Strong positive relationship between **balls faced** and **runs scored**  
- Scoring rate tends to be more variable in very short innings and stabilises in longer ones  
- Team compositions differ slightly in how many batters, bowlers, and allrounders each side uses

---

## **6. Tools & Packages**
- **R**, **RStudio**  
- tidyverse: `dplyr`, `tidyr`, `ggplot2`, `stringr`, `forcats`

---

## **7. Repository Structure**
```text
/scripts              R code for wrangling and analysis
/report.pdf           Full written report
README.md             Project overview

8. How to Run This Project

Place the raw Ashes dataset (e.g. ashes.csv) in the project directory.

Open the main script (e.g. ashes_performance_analysis.R).

Run sections for:

data loading

tidying and feature extraction

visualisation and summaries

Open report.pdf for detailed interpretation and figures.

---



