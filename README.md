# Smoking Health Risk Analysis Dashboard

## Overview

This project is a Power BI dashboard designed to analyze the health risks associated with smoking. The objective of this dashboard is to visualize patient demographics, smoking habits (years of smoking, cigarettes per day), and their direct impact on organ health (heart, lungs, kidneys, liver) and other vital health metrics like BMI, blood pressure, and cholesterol levels.


## Objectives

*   **Apply Visual Encoding Principles:** Use Power BI features to encode risk levels, health conditions, and patient segmentation.
*   **Represent Categorical and Numerical Data:** Analyze patterns across categorical attributes (Smoking Status, Gender, Organ Condition) and numerical data (Age, BMI, Cholesterol Level, Cigarettes Per Day).
*   **Visualize Hierarchical/Relational Data:** Map health risks to specific organs (Heart, Lungs, Kidney, Liver) and general body conditions.
*   **Analyze Health Indicators:** Develop comparative measures to evaluate individual health metrics against population averages.
*   **Develop an Interactive Dashboard:** Enable healthcare analysts or users to explore custom subsets of the population using dynamic filtering.


## Tools & Technologies

*   **Power BI Desktop** (Dashboard creation, interactive reports)
*   **Power Query** (Data preparation and structural cleaning)
*   **DAX (Data Analysis Expressions)** (Calculated columns for age grouping, and measures comparing individual records against the average age or BMI)
*   **CSV Files** (Source datasets)


## Dataset

The analysis is based on the following key variables:
*   **Patient Demographics:** `Patient_ID`, `Age`, `Gender`
*   **Smoking Habits:** `Smoking_Status` (Never, Former, Current), `Years_of_Smoking`, `Cigarettes_Per_Day`
*   **Clinical & Risk Metrics:** `BMI`, `BP_Risk` (Low, Normal, High), `Cholesterol_Level`, `Family_History_Risk`, `Alcohol_Consumption`
*   **Organ Health Status:** `Organ_Name` (Heart, Lungs, Kidney, Liver, Human Body) and `Condition` (Healthy, Damaged)


## Dashboard Features

*   **Organ-Specific Health Status Visualizer:** A central, dynamic image container that updates to display realistic anatomical illustrations (Heart, Lungs, Kidney, Liver, or Human Body) in either **Healthy** or **Damaged** states depending on the user's filter selections.
*   **Key Performance Indicators (KPIs):**
    *   **Total Patient Count:** A card display showing the total number of patients within the selected category.
    *   **Demographic Comparisons:** Active comparisons of the cohort's average age and BMI against overall dataset averages using DAX measures (`vs Avg Age` and `vs Avg BMI`) with dynamic directional indicators (▲/▼).
*   **Smoking Status Analysis:** A donut chart showing the percentage distribution of patient smoking statuses (`Never`, `Current`, `Former`).
*   **Smoking Intensity Trend Chart:** A dual-axis line chart showing **Years of Smoking (YOS)** and **Cigarettes Per Day (CPD)** binned by **Age Group** on the x-axis.
*   **Demographic Cohort Flows:** A Ribbon chart showing patient distributions by **Smoking Status** and split by **Gender** (Male/Female).
*   **Cholesterol & Hypertension Risk:** A stacked column chart plotting **Average Cholesterol Level** by **Age Group**, segmented by blood pressure risk category (**High**, **Low**, **Normal**).
*   **Interactive Chiclet Slicers:**
    *   **Organ Slicer (Vertical navigation pane on the left):** Slices report visuals by selecting specific organs (Heart, Human Body, Kidney, Liver, Lungs) decorated with descriptive icons.
    *   **Condition Slicer (Top horizontal navigation):** Filter the data by **Healthy** or **Damaged** conditions.


## Project Structure

```text
PowerBI/
    Smoking Health Risk Analysis.pbix

Dataset/
    Background Viz.png
    Image Dataset.csv
    Measure and Column Forumula.txt
    Organ.csv
    condition.csv
    health_dataset.csv
    
Screenshots/
    Damaged-Health-Dashboard.png
    Healthy-Health-Dashboard.png
    Health-Kidney-Dashboard.png
```

## How to Use

1.  **Clone or Download:** Download all repository files, keeping the CSV files in the same relative directory.
2.  **Open in Power BI:** Open the `Smoking Health Risk Analysis.pbix` file in **Power BI Desktop**.
3.  **Update Data Source Paths** (If required):
    *   In Power BI, click **Transform Data** > **Data source settings**.
    *   For `health_dataset.csv`, `Organ.csv`, `condition.csv`, and `Image Datasets.csv`, click **Change Source...** and map them to their local paths in your repository folder.
    *   Click **Close & Apply**.
4.  **Refresh:** Click **Refresh** on the home ribbon to load the datasets.
5.  **Explore:** Interact with the charts, filter lists, and slicers to analyze health trends.


## References

1.  [YouTube Link References](https://www.youtube.com/watch?v=3upN1GzlESI) — This project is built exactly the same as this YouTube dashboard tutorial.
2.  [Smoking Health Risk Analysis PowerBI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiODNkNWU2NGYtZjRjYy00NWIyLTliYWEtMmY4Y2NmN2RjMzgwIiwidCI6ImQ0OTRlMTEzLTUyOGUtNDBhYi05MGQ5LTE2MmRlMmZjYTNmMyIsImMiOjEwfQ%3D%3D) — Live published interactive version of the dashboard.
