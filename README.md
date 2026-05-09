# 🚦 Road Accident Analysis Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

An interactive Power BI dashboard analyzing road accident data across the UK, providing insights into casualty trends, vehicle types, road conditions, and geographic hotspots for data-driven safety decision-making.

---

## 📊 Dashboard Preview

> *Open `ADHEETHI_project_dax.pbip` in Power BI Desktop to view the full interactive dashboard.*

---

## 🎯 Key KPIs (Current Year)

| KPI | Value | YoY Change |
|-----|-------|------------|
| Total Casualties | 195.7K | ▼ -11.9% |
| Total Accidents | 144.4K | ▼ -11.7% |
| Fatal Casualties | 2.9K | ▼ -33.3% |
| Serious Casualties | 27.0K | ▼ -16.2% |
| Slight Casualties | 165.8K | ▼ -10.6% |

---

## 📈 Dashboard Features

### Visualizations Included
- **KPI Cards** — Current Year vs Previous Year casualties with trend indicators
- **Monthly Trend Line Chart** — CY vs PY casualties comparison (Jan–Dec)
- **Casualties by Vehicle Type** — Breakdown across Cars, Bikes, Buses, Vans, Agricultural, Others
- **Casualties by Urban/Rural** — Donut chart (Urban: 61.95% | Rural: 38.05%)
- **Casualties by Road Type** — Bar chart (Single carriageway, Dual carriageway, Roundabout, etc.)
- **Casualties by Light Condition** — Donut chart (Day: 73.84% | Dark: 26.16%)
- **Casualties by Location** — Geographic map of the UK showing accident hotspots

### Filters / Slicers
- **Road Surface** (All / Dry / Wet / Snow-Ice)
- **Weather Conditions** (All / Fine / Rain / Snow / Fog)

---

## 🔍 Key Insights

- **Cars** account for the highest casualties at **155,804** — making up the majority of all vehicle-related accidents
- **Single carriageway roads** are the most dangerous road type with **145K** casualties
- **Daytime accidents** dominate at **73.84%**, suggesting high-traffic hours as a key risk factor
- **Urban areas** account for nearly **62%** of all casualties
- Significant **year-on-year improvement** observed — fatal casualties dropped by **33.3%**

---

## 🛠️ Tech Stack

| Tool | Usage |
|------|-------|
| Power BI Desktop | Dashboard design & visualization |
| DAX | Calculated measures, KPIs, YoY comparisons |
| Power Query | Data transformation & cleaning |

---

## 📁 Project Structure

```
ADHEETHI_project_dax/
│
├── ADHEETHI_project_dax.pbip          ← Open this in Power BI Desktop
├── .gitignore
│
├── ADHEETHI_project_dax.Report/       ← Report visuals & page definitions
│   ├── report.json
│   └── pages/
│
└── ADHEETHI_project_dax.SemanticModel/ ← Data model, tables & measures
    └── definition.bim
```

---

## 🚀 How to Use

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/ADHEETHI_project_dax.git
   ```

2. **Open in Power BI Desktop**
   - Launch Power BI Desktop
   - Open `ADHEETHI_project_dax.pbip`

3. **Refresh Data** (if needed)
   - Go to `Home → Refresh`
   - Update data source path if prompted

4. **Explore the Dashboard**
   - Use the **Road Surface** and **Weather Conditions** slicers to filter
   - Hover over charts for detailed tooltips
   - Click on visuals to cross-filter across the dashboard

---

## 📐 DAX Measures Used

```dax
-- Example KPI measures
CY Casualties = TOTALYTD(SUM(Data[Number_of_Casualties]), 'Calendar'[Date])

PY Casualties = CALCULATE([CY Casualties], SAMEPERIODLASTYEAR('Calendar'[Date]))

YoY % Change = ([CY Casualties] - [PY Casualties]) / [PY Casualties]
```

---

## 👩‍💻 Author

**Adheethi**  
Business Analyst | Power BI Developer  
- Designed interactive dashboards for stakeholder reporting
- Developed KPI documentation and data source mapping
- Applied BA deliverable standards for client-facing reporting

---

## 📄 License

This project is for educational and portfolio purposes.
