# cyclistic-bike-share-analysis

Exploratory and descriptive analysis of Cyclistic (Divvy) bike-share trips using Excel for data cleaning, R (tidyverse) for analysis, and Tableau Public for visualization.

**Author:** Royed Alberto Herrera Cano

---

## Executive Summary

This project analyzes Cyclistic bike-share trip data to understand how **annual members** and **casual riders** use the service differently. The goal is to generate actionable insights to support a marketing strategy focused on converting casual riders into annual members.

Using two datasets (**Divvy 2019 Q1** and **Divvy 2020 Q1**), I cleaned and standardized the data in **Excel**, then merged and analyzed the datasets using **R (tidyverse)**. Finally, I built an interactive dashboard in **Tableau** to visualize key ridership trends by weekday. The analysis reveals clear behavioral differences between both segments: annual members generate the majority of rides (higher frequency and consistency across weekdays), while casual riders take fewer rides but with longer average trip durationespecially on weekends.

Based on this, I recommend:

- Targeting casual riders with weekend-focused membership conversion campaigns
- Promoting membership benefits that align with commuting behavior (weekday usage)
- Using digital marketing to emphasize cost savings for frequent riders
- Designing offers that convert long-duration casual riders into members

---

## Dashboard Preview

![Cyclistic bike share tableau](https://github.com/royedherrera1/cyclistic-bike-share-analysis/blob/main/Dashboard%20Cyclistic%20bike-share.png?raw=true)


---


## Business Problem

Cyclistic’s marketing team aims to increase profitability by growing the number of annual memberships. Since annual members generate higher long-term value than casual riders, the company needs to identify key differences in usage patterns.

Key questions guiding this analysis:

- How do annual members and casual riders use Cyclistic bikes differently?
- What patterns (weekday behavior) can help drive conversion strategies?

**Business task:**  
Identify behavioral differences between casual riders and annual members to support marketing strategies that increase annual membership conversions.

---

## Dataset

- **Source:** Divvy / Cyclistic bike-share trip datasets (Google Data Analytics Capstone)
- **Files used:**  
  - Divvy_Trips_2019_Q1  
  - Divvy_Trips_2020_Q1
- **Scope:** Chicago bike-share trips (Q1 2019 and Q1 2020)
- **Granularity:** Individual trip-level data

---

## Methodology

### Tools
- **Excel / Google Sheets:** cleaning, transformation, pivot tables
- **R (tidyverse):** merging datasets, feature engineering, descriptive analysis
- **Tableau Public:** dashboard creation and storytelling

### Data Cleaning & Integrity Checks
- Standardized column names between 2019 and 2020 datasets:
  - `trip_id → ride_id`
  - `start_time → started_at`
  - `end_time → ended_at`
  - `usertype → member_casual`
- Standardized user types:
  - `Subscriber → member`
  - `Customer → casual`
- Created new variables:
  - `ride_length`
  - `day_of_week`
- Removed invalid or abnormal trips:
  - Negative ride durations
  - Zero-length rides
  - Casual rides longer than 24 hours (outliers / likely system anomalies)

---

## Analysis Performed

- Overall ride frequency by rider type (member vs casual)
- Average ride duration by rider type
- Weekly patterns:
  - Total rides by day of week and rider type
  - Average ride duration by day of week and rider type
- Summary table exported from R for Tableau dashboarding

---

## Key Insights

- **Members** generate significantly more rides than casual users across all weekdays
- **Casual riders** show the highest activity during weekends
- **Casual trips have longer average duration** than member trips on every day of the week
- The pattern suggests:
  - Members behave like frequent commuters
  - Casual riders behave more like leisure / recreational users

---

## Results & Business Implications

Cyclistic can increase membership conversions by tailoring strategies to the behavior of casual riders. Since casual users ride longer—particularly on weekends—conversion messaging should emphasize:

- Membership cost-benefit for frequent use
- Weekend membership bundles or trial membership campaigns
- Retargeting ads for casual users who ride repeatedly

These findings support:
- Marketing segmentation
- Campaign personalization
- Digital advertising strategy optimization

---

## Recommended Actions

- Launch weekend-focused campaigns aimed at high-duration casual riders
- Promote membership pricing as a long-term savings strategy
- Retarget casual riders after weekend trips using email + social media
- Test campaigns highlighting convenience and “unlimited ride value” messaging

---

## Next Steps

- Expand analysis to full 12 months of data for stronger seasonality trends
- Analyze station-level behavior (popular locations for casual vs member)
- Include time-of-day patterns (morning commute vs afternoon leisure)
- Build predictive features to classify riders likely to convert to membership

---

## Dashboard and Data Access

- **Tableau Public Dashboard:**  
  *https://public.tableau.com/views/CyclisticBike-Share_17684286176530/Dashboard1?:language=es-ES&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link*

- **Code:**  
  Available in the `code/` folder.

- **Aggregated Tableau-ready dataset:**  
  Available in the `data/` folder (e.g., `tableau_summary.csv`).

---

## Skills Used

- **Excel / Google Sheets:** cleaning, transformation, pivot tables
- **R / tidyverse:** data wrangling, aggregation, feature engineering
- **Tableau Public:** dashboard design, KPI reporting, storytelling
- **Data Analytics Process:** Ask, Prepare, Process, Analyze, Share, Act

---

## Data Source & License

This analysis uses public Divvy (Cyclistic) trip data provided in the Google Data Analytics Capstone project.

**Datasets used:**
- Divvy_Trips_2019_Q1 (Google Sheet): https://docs.google.com/spreadsheets/d/1uCTsHlZLm4L7-ueaSLwDg0ut3BP_V4mKDo2IMpaXrk4/template/preview?resourcekey=0-dQAUjAu2UUCsLEQQt20PDA#gid=1797029090
- Divvy_Trips_2020_Q1 (Google Sheet): https://docs.google.com/spreadsheets/d/179QVLO_yu5BJEKFVZShsKag74ZaUYIF6FevLYzs3hRc/template/preview#gid=640449855

**License:**
- Divvy Data License Agreement: https://divvybikes.com/data-license-agreement

The original raw datasets are not included in this repository due to size and licensing considerations.
Only cleaned/aggregated outputs and analysis scripts are provided for reproducibility.

This project is for educational purposes only and is not affiliated with Divvy or Motivate International Inc.

---

## Contact Me

- **Email:** royed.123@outlook.com  
- **LinkedIn:** https://www.linkedin.com/in/royed-alberto-herrera-cano/

