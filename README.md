# 🎬 Greenlight Analytics — Phase 2 Project

## 📖 Executive Summary  
This project analyzes movie industry data from **Box Office Mojo** and **IMDb (via SQLite)** to guide strategic decisions for a new film studio.  
The analysis focuses on three key business questions:

1. **Which genres and runtimes are most successful?**  
2. **Do ratings correlate with revenue?**  
3. **How do domestic vs. foreign markets vary by studio?**  

---

## 🔑 Key Insights  
- **Action, Adventure, and Fantasy** films consistently generate the highest box office revenues.  
- Studios differ significantly in their **domestic vs. foreign revenue mix** — release strategies matter.  
- **Runtimes between 95–120 minutes** correlate with stronger ratings and solid box office performance.  

---

## 💡 Recommendations  
1. Prioritize high-performing genres.  
2. Balance domestic and international release strategies.  
3. Greenlight films with strong audience signals (ratings, genre fit, runtime).  

---

## 🗂️ Data Sources  
- **Box Office Mojo (CSV):** Domestic and foreign grosses.  
- **IMDb (SQLite):** Movie basics and ratings tables.  

The datasets were merged on keys such as `title / primary_title`, `year / start_year`, and `movie_id`.  

---

## ⚙️ Data Preparation  
Before analysis, the following steps were performed:  
- Removed duplicate rows.  
- Dropped records with critical null values.  
- Converted `foreign_gross` to numeric and filled missing values with 0.  
- Added a `total_gross` column (`domestic_gross + foreign_gross`).  

---

## 📊 Analysis & Visuals  
- **Genres & Runtimes:**  
  - Aggregated revenues by genre.  
  - Explored correlations between runtime and ratings.  

- **Ratings & Revenue Correlation:**  
  - Scatter plots and regression lines with log-scale transformation on revenues.  

- **Domestic vs. Foreign Markets:**  
  - Compared studio-level performance with stacked bar charts.  

---

## 🛠️ Tech Stack  
- **Python**: `pandas`, `numpy`, `sqlite3`  
- **Visualization**: `matplotlib`, `seaborn`  
- **Data sources**: CSV (Box Office Mojo), SQLite (IMDb)  

---

## ▶️ How to Run  
1. Clone this repository.  
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Place `bom.movie_gross.csv.gz` and `im.db` in the project folder.  
4. Open the notebook:  
   ```bash
   jupyter notebook notebook.ipynb
   ```

---
