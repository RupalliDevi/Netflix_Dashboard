# Netflix_Dashboard
A Power BI dashboard analyzing Netflix content trends, genres, and ratings using Kaggle dataset.
# 🎬 Netflix Analytics Power BI Dashboard

## 📖 Overview
This project presents an interactive **Power BI dashboard** analyzing Netflix’s global content catalog.  
It is built for **learning and practice purposes**, focusing on **data visualization, transformation, and storytelling**.  

The report is created in **Power BI Desktop**, published on **PowerBI.com**, and uses the *Netflix Movies and TV Shows dataset* from Kaggle.
It visualizes insights about **content distribution**, **type mix**, and **country contributions** — styled with a signature Netflix black-and-red theme.

---

## 🟥 Page 1: Netflix Overview Dashboard
![Netflix Overview Dashboard]

### 🔍 Key Highlights:
- **KPI Cards**
  - 🎞️ **Sum of Movie Count:** 25K  
  - 📺 **Sum of TV Show Count:** 11K  
  - 🎬 **Sum of Titles:** 9K  
- **Line Chart:** *Sum of Titles by Country*  
  - Highlights how the **United States**, **India**, and **United Kingdom** dominate content creation.
- **Donut Chart:** *Title Count by Country and Type*  
  - Shows proportional contribution by region and type.
- **Netflix Branding:** Styled with a dark background, bold red titles, and minimalist layout for a premium, cinematic feel.

🧠 *Insight:*  
Netflix’s content is majorly led by **Movies** from the **U.S.**, followed by **India** and **the U.K.** in both production volume and variety.

---

## ⚫ Page 2: Netflix Description *(In Progress)*
The second page is planned to display deeper insights such as:
- **Genre and Category Analysis**
- **Top Directors and Actors**
- **Average Duration Metrics**
- **Ratings and Genre Correlation**

---

## 🔄 Data Transformations
Performed in **Power Query Editor** to prepare and clean the dataset:
- Removed null and duplicate rows  
- Cleaned up inconsistent text casing and spacing  

These transformations ensured accuracy and consistency in the dashboard visuals.

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

© 2025 Rupalli Devi. All Rights Reserved.

 
