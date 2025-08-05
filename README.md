# 🌱 Carbon Footprint Tracker

A web-based dashboard built using **R Shiny** and **PostgreSQL** to monitor and reduce carbon emissions on a college campus. This project helps visualize sustainability efforts and identify key contributors to environmental impact.

---

## 🎯 Objective

To track, visualize, and reduce carbon emissions in real-time through an interactive dashboard that informs eco-conscious decisions across departments and utilities.

---

## 🧰 Tools & Technologies

| Category        | Tools Used                    |
|-----------------|-------------------------------|
| Language        | R                             |
| Dashboard       | R Shiny                       |
| Database        | PostgreSQL                    |
| Libraries       | tidyverse, shiny, plotly, DBI |
| Hosting (opt)   | shinyapps.io or RStudio Connect |

---

## 🧪 Project Workflow

1. **Data Collection**
   - Monthly emissions data from utilities (electricity, gas, water, waste)
   - Manually entered + automated via scripts

2. **Data Storage**
   - PostgreSQL database structured by building, utility type, and time
   - Scheduled data ingestion (cron job optional)

3. **Dashboard Development**
   - R Shiny app with dynamic filters and tabs
   - Live database connection using `DBI` and `RPostgres`
   - Real-time updates and visual KPIs

4. **Insights & Actions**
   - Highlighted buildings/departments with high emissions
   - Suggested interventions based on trends

---

## 📈 Key Features

- 📊 Live charts showing emissions by source and time
- 🌍 Geo-location map of emission contributors (optional via `leaflet`)
- 📉 Comparative view for before/after intervention impact
- 🧾 Downloadable reports in PDF/CSV

---

## 📁 Project Structure


---

## 🚀 How to Run

### 1. Setup PostgreSQL

```sql
-- Inside PostgreSQL
CREATE DATABASE carbon_tracker;
\c carbon_tracker
-- Run create_tables.sql and insert_sample_data.sql
# In R console
install.packages(c("shiny", "DBI", "RPostgres", "plotly", "dplyr", "shinydashboard"))
shiny::runApp("carbon-footprint-tracker/app")
