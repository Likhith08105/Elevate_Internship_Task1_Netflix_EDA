# 🎬 Netflix Data Cleaning & Exploratory Analysis (Elevate Internship - Task 1)

## Project Overview

This repository documents the completion of **Task 1: Data Cleaning and Preprocessing** for the Elevate Data Analyst Internship, utilizing the **Netflix Movies and TV Shows** dataset. The primary objective was to transform the raw data into a clean, structured format suitable for robust downstream analysis and modeling.

The entire process, from data loading to visualization, is detailed in the accompanying Jupyter Notebook (`[your_notebook_name].ipynb`).

## 🛠️ Key Data Cleaning & Preprocessing Steps

The following critical issues were addressed using Python (Pandas):

* **Handling Missing Values (Nulls):**
    * Categorical fields (`director`, `cast`, `rating`) were filled using a constant value of **'Unknown'** or the **Mode** to preserve row integrity.
    * Rows with missing `date_added` were dropped, as imputation would compromise the timeline analysis.
* **Data Type Conversion:**
    * The crucial `date_added` column was converted to the `datetime` format using the `errors='coerce'` argument to handle inconsistent date strings robustly.
* **Duplicate Removal:** All exact duplicate rows across the dataset were identified and removed using `drop_duplicates()`.
* **Data Standardization:**
    * All column headers were standardized to **lowercase** and **snake_case** (e.g., `release_year`).
    * The `country` field was simplified to include only the primary country listed.

## 📊 Initial Exploratory Insights (EDA)

Post-cleaning, initial visualizations were generated to validate data integrity and extract immediate insights:

### Content Added Over Time

This chart confirms a significant ramp-up in content acquisition, particularly from 2018 onwards.



### Content Type Distribution

The dataset shows a clear preference for Movies, which account for the majority of the content catalog.



## 📦 Repository Contents

| File Name | Description |
| :--- | :--- |
| `[Netflix_data_CLEANING].ipynb` | The full Jupyter Notebook containing all cleaning code and visualizations. |
| `netflix_titles.csv` | The original, raw dataset. |
| `netflix_titles_cleaned.csv` | The final, structured, and cleaned dataset ready for analysis. |
| `requirements.txt` | Lists all necessary Python libraries and versions required to run the notebook. |
| `content_added_plot.png` & `content_type_plot.png` | Visual summaries of the key exploratory findings. |

***
