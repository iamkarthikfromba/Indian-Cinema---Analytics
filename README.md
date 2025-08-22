# 🎬 Indian Cinema Analytics (2010 → onwards)

A Streamlit-based research module analyzing **Indian Cinema industries** (Bollywood, Kollywood, Tollywood, Mollywood, Sandalwood) from 2010 onwards.  
This project focuses on **collecting, cleaning, and visualizing** movie data including budgets, box office collections, crew, and ratings.

---

## 📌 Objectives
- Track the **number of movies released** per year (by industry & language).  
- Compare **budget vs box office collections**.  
- Categorize **actors, directors, production houses, musicians, storytellers** into earning brackets.  
- Explore **genre combinations** and their performance.  
- Compare **IMDb ratings vs box office success**.  
- Provide **snapshot views** at 14 days, 30 days, and 90 days post-release.  

---

## 📊 Data Collection Approach
- **Primary Sources**:  
  - [TMDb API](https://www.themoviedb.org/documentation/api) for metadata (titles, dates, genres, crew).  
  - IMDb/Wikipedia/BoxOfficeIndia for collections and budgets.  
- **Gap Filling**:  
  - Google **Gemini Pro API** is used to approximate or cross-check missing values.  
- **Inclusions**:  
  - Both **theatrical** and **OTT-only releases** are considered.  
- **Standardization Rules**:  
  - IDs:  
    - Movies → `MO-##########`  
    - Crew → `CO-###############`  
  - All values in **INR crore (₹)**.  
  - Rounded to nearest **₹25 crore** (min = ₹1 cr).  
  - Conflicting reports resolved by **median/mode**.  
  - `created_on` & `updated_on` fields track refreshes.  

---

## 🔄 Data Refresh Workflow
- **Manual trigger** inside Streamlit app.  
- Refresh fetches new data (Gemini + APIs).  
- Snapshots stored for each movie at:  
  - 14 days  
  - 30 days  
  - 90 days after release  

---

## 🚀 Streamlit Dashboard Features
- Yearly release trends (by industry).  
- Budget vs Box Office bar/line charts.  
- Crew-based earning brackets (actors, directors, production houses, etc.).  
- Genre combination analysis.  
- IMDb ratings vs collections scatterplot.  
- Snapshot view with collection growth at 14d / 30d / 90d.  

---

## 🛠 Tech Stack
- **Data Retrieval**: Google Gemini Pro API, TMDb, IMDb, Wikipedia.  
- **Data Management**: Python (Pandas), SQLite/CSV.  
- **Visualization**: Streamlit + Plotly/Altair.  

---

## 📜 Current Scope
- Focus: **Data collection + visualization**.  
- Not included yet:  
  - Visitor tracking  
  - Licensing / Open Data release  
  - External contributions  

These will be considered in later phases.  

---

## 🙏 Acknowledgements
- **Google** – for providing free access to **Gemini Pro API** under the *Gemini Student Program*, enabling gap-filling and enrichment of cinema data.  
- **OpenAI** – for **ChatGPT support** in structuring project design, definitions, and research workflow.  

---

## 📧 Maintainer
Maintainer: *Balaraj B Gulabal*
