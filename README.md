# 🇮🇳 Indian Crime Analytics Dashboard (2020–2024)

📊 A recruiter-ready Power BI project analyzing national crime trends in India.  
Includes headline KPIs, case resolution rates, victim demographics, and city-wise geographic insights.

---

## 🔹 Project Overview
This project demonstrates an end-to-end data analytics workflow — starting from a raw CSV dataset through Python-based cleaning, feature engineering, and finally a professional 4-page Power BI dashboard.  

- Dataset: **40,160 crime records** across 29 major Indian cities (Jan 2020 – May 2024)  
- Tools: **Claude AI (data cleaning), Python, Power BI Desktop, DAX, Bing Maps**  
- Goal: Extract actionable insights on crime patterns, victim demographics, case resolution efficiency, and geographic distribution.

---

## 🔹 Features
- **KPI Cards** → Total Cases, Open Cases, Closed Cases, Avg Victim Age  
- **Case Resolution Analysis** → Closure % by crime type and city  
- **Victim Demographics** → Gender, age group, weapon used  
- **Geographic Maps** → Crime volume and closure rate by city  
- **Interactive Slicers** → Year, Victim Gender  

---

## 🔹 Data Preparation
- Fixed mixed date formats (DD-MM-YYYY vs MM-DD-YYYY)  
- Filled blanks with descriptive labels (e.g., “Not Yet Closed”, “Unknown”)  
- Standardized gender codes (M → Male, F → Female, X → Other/Unknown)  
- Engineered new columns: Hour, Year, Month, Day of Week, Days to Close, Age Group  
- Zero null values in final dataset → `crime_india_powerbi_ready.csv`

---

## 🔹 DAX Measures
Key measures created in Power BI:
- `Total Cases = COUNTROWS(CrimeData)`  
- `Closed Cases = COUNTROWS(FILTER(CrimeData, CrimeData[Case Closed] = "Yes"))`  
- `Closure Rate % = DIVIDE([Closed Cases], [Total Cases], 0) * 100`  
- `Avg Victim Age = AVERAGE(CrimeData[Victim Age])`  
- `Avg Days to Close = AVERAGEX(FILTER(CrimeData, CrimeData[Case Closed]="Yes"), CrimeData[Days to Close])`

---

## 🔹 Dashboard Pages
1. **Overview** → KPIs, crime domain, crime description, annual trend, domain/weapon split  
2. **Case Resolution** → Open vs Closed cases, closure % by crime type & city  
3. **Victims** → Weapon usage, gender distribution, age group analysis  
4. **Geography** → City-wise crime volume & closure rate maps  

---

## 🔹 Key Insights
- National closure rate: **50%** (20,062 closed vs 20,098 open)  
- **Thane** → highest closure rate (53.7%)  
- **Srinagar** → lowest closure rate (44.7%)  
- Female victims: **55.8%** of cases  
- Most affected age group: **36–50 years**  
- Knife → most used weapon (5,835 cases)  
- Delhi → highest crime volume (5,400 cases)  

---

## 🔹 Repository Contents
- **data/** → Raw & cleaned datasets  
- **dashboards/** → Power BI `.pbix` file  
- **docs/** → Project documentation (`India_Crime_Analytics_Documentation_v2.docx`)  
- **screenshots/** → Dashboard visuals  
- **README.md** → Project overview & insights  

---

## 🔹 How to Use
1. Download `crime_india_powerbi_ready.csv` and `.pbix` file  
2. Open in **Power BI Desktop**  
3. Explore dashboards with slicers and filters  
