# Texas Crash-Data-Analysis – Interactive Power BI Report

This project explores **1.15 M+** crash records from Texas (2015 - 2025) to uncover temporal, spatial, demographic and behavioural patterns behind road-traffic accidents.  
The analysis is delivered as an interactive Power BI report with two pages:

1. **State-wide Overview** – macro trends, injury severity and a crash-location map.  
2. **Demographic & Contributing-Factor Deep-Dive** – who, when and why accidents happen most.

---

## 1. Data & Preparation  

| Item | Details |
|------|---------|
| **Source** | Texas Department of Transportation Crash Records Information System (CRIS) |
| **Time span** | Jan-2015 → Mar-2025 |
| **Raw fields** | 70+ columns covering crash timestamp, weather, location (lat/lon & jurisdiction), driver/passenger demographics, injury severity, contributing factors, etc. |
| **Cleaning steps** | • removed rows with missing geo-coordinates<br>• standardised text fields (county, city, weather)<br>• derived formatted **`Hour of Day`** and **`Month`** dimensions<br>|

---

## 2. Report Navigation  

### Global Filters
| Filter | Purpose |
|--------|---------|
| **City slicer** *(both pages)* | Focus the report on one municipality (default = All) |
| **County slicer** *(Page 2)* | Drill further into a county |
| **Year slider** *(Page 1)* | Scrub through 2015 - 2025 to see year-on-year trends |

---

## 3. 📄 Page 1 – *“Texas Road Accidents Data Analysis”*  

| Visual | What it tells you | Tips |
|--------|------------------|------|
| 🗺 **Bing Map** – blue crash dots | Geographic distribution of every recorded crash | Zoom / pan or use the City slicer to isolate hotspots |
| 📊 **Column chart – Crashes by Month** | Seasonality: January is consistently highest (~340 crashes); March dips slightly (≈ 310) | Hover for exact counts |
| 🍕 **Donut chart – Injury Severity split** | Proportion of **Fatal (K)** vs **Non-injury (N)** vs **Possible/Suspected** outcomes | Click a slice to filter all other visuals |
| 📅 **Year timeline slider** | Long-term trend; total crashes peaked in 2019, dipped during COVID 2020-21, rebound after | Drag the handles to analyse a sub-period |
| 🧾 **Detail table** | Row-level detail (time band, deaths, weather, county, role, intersection flag) | Sort any column; combine with map for spatial-temporal context |

---

## 4. 📄 Page 2 – *“Demographic & Contributing-Factor Insights”*  

| Visual | Insight | Notes |
|--------|---------|-------|
| 📊 **Top 15 Ages by Crash Count** | 18-25 year-olds dominate; Age 21 is highest (~2.5 k crashes) | Dynamic – respects City/County slicers |
| 📈 **Hour-of-Day bar chart** | Evening rush (18:00-21:59) is risk-iest; early afternoon lull (13:00-15:59) | Ordered descending for quick scanning |
| 🏷 **Horizontal bar – Top 5 Contributing Factors** | “Wrong Way – One Way Road” is 10× more common than #2 cause | Shows counts; hover for % of total |

---

## 5. Key Findings  

1. **Temporal spikes** – Weekday evenings (18-22h) and January months record the highest crash volumes.  
2. **Young drivers** – 18-25 age bracket contributes >20 % of all incidents, mirroring national statistics.  
3. **Fatality share** – Although fatal injuries make up just **7 %** of crashes, they cluster heavily around inter-city highways.  
4. **Driver behaviour** – Wrong-way driving on one-way roads is the single most cited contributing factor, signalling signage or enforcement gaps.  

---

## 6. Using the Report  

| Action | Result |
|--------|--------|
| **Ctrl + Click a bar, slice or map area** | Cross-filters every visual for rapid “slice-&-dice” exploration |
| **Multi-select** (*Ctrl + Click multiple items*) | Build compound filters (e.g., *City = Dallas* **AND** *Hour of Day = 18:00-18:59*) |

Screenshots:

![Report 1](https://github.com/user-attachments/assets/a82f63d6-e99b-46ec-a8d6-cc3a1cc47e75)

![Report 2](https://github.com/user-attachments/assets/fe45690d-fb10-4de9-8ddb-0c0cc9f2c090)

