# Netflix_Dashboard
A Power BI dashboard analyzing Netflix content trends, genres, and ratings using Kaggle dataset.
# 🎬 Netflix Analytics Power BI Dashboard

## 📖 Overview
This project is a **Power BI dashboard** analyzing Netflix's global content library using the *Netflix Movies and TV Shows dataset* from Kaggle.  
It provides insights into the **distribution of content types**, **country contributions**, and **content growth trends** — styled with a dark Netflix-inspired theme.  

---

## 📊 Dashboard Pages

### 🟥 Page 1: Netflix Overview
![Netflix Overview Dashboard]

**Highlights:**
- **Total Movies, TV Shows, and Titles** – KPIs showing Netflix’s expansive catalog.  
- **Top Contributing Countries** – Visualized with line and donut charts.  
- **Title Distribution by Type** – Comparison of Movies vs TV Shows.  
- **Dynamic Filters** – For year and type, enabling interactive exploration.  

🧠 *Key Insight:*  
Netflix’s catalog is heavily led by the **United States**, followed by **India** and **the United Kingdom**, showing its broad global reach.

---

### ⚫ Page 2: Netflix Description *(In Progress)*
Planned to include:
- **Genre & Category Analysis**
- **Top Directors and Cast**
- **Average Duration Metrics**
- **Rating vs Genre Correlation**

---

## 🔄 Data Transformations
Performed in **Power Query Editor** before visualization:
- Removed null and duplicate values  
  
- Trimmed unnecessary spaces and unified text casing  

---

## 🧮 DAX Measures Used
CountTypes =

SUMMARIZECOLUMNS(

    'netflix_titles'[type],

    "Total_Count", COUNTROWS('netflix_titles'),

    "Movie_Count", CALCULATE(COUNTROWS('netflix_titles'), 'netflix_titles'[Type] = "Movie"),

    "TVShow_Count", CALCULATE(COUNTROWS('netflix_titles'), 'netflix_titles'[Type] = "TV Show"),

    "Sum_of_Type_Counts", 

        CALCULATE(COUNTROWS('netflix_titles'), 'netflix_titles'[Type] = "Movie") + 

        CALCULATE(COUNTROWS('netflix_titles'), 'netflix_titles'[Type] = "TV Show")

)

