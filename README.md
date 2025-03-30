# AtliQ Grands – Power BI Revenue Intelligence Dashboard

## Project Overview

AtliQ Grands is a luxury five-star hotel chain operating across India for over 20 years. Due to increasing competition and ineffective decision-making, the company has been experiencing a decline in both market share and revenue within the luxury/business hotel segment.

To enable data-driven decision-making, a revenue intelligence system was developed to analyze historical hotel performance and identify key areas for improvement. This project involved the creation of a structured and interactive Power BI dashboard, based on stakeholder requirements and industry-standard KPIs.

---

## Objective

- Develop and visualize key metrics impacting revenue performance.
- Build an interactive dashboard to provide visibility into operational and booking trends.
- Enable stakeholders to explore multiple layers of insights to identify root causes and opportunities.
- Extend the analysis beyond the stakeholder mock-up to include additional insights and recommendations.

---

## Project Deliverables

1. **Data Cleaning and Preparation**  
   - Imported and transformed raw data using Power Query.  
   - Created calculated columns and measures using DAX.  
   - Ensured consistency and accuracy of metrics across time, channel, and hotel locations.

2. **Key Performance Indicators (KPIs)**

| KPI | Formula |
|-----|---------|
| Revenue per Available Room (RevPAR) | `Total Revenue / Total Rooms Available` or `ADR * OCC%` |
| Occupancy Percentage (OCC%) | `Total Rooms Occupied / Total Rooms Available` |
| Average Daily Rate (ADR) | `Total Revenue / Total Rooms Sold` |
| Daily Sellable Room Nights (DSRN) | Based on property-level room inventory |
| Realization | `URN (Utilized Room Nights) / BRN (Booked Room Nights)` |

3. **Dashboard Design**

The dashboard is structured to provide insights at multiple levels:

- **Overview (Level 1):** High-level KPIs with time and location filters.
- **Breakdown (Level 2):** Channel-level, hotel-level, and time-series analysis.
- **Drill-down (Level 3):** Realization, room categories, and channel-specific performance insights.

4. **Filters and Segmentation**
   - Date range (monthly/quarterly)
   - Hotel location
   - Room type
   - Booking channel (Direct, OTA, Corporate, etc.)
   - Weekend vs Weekday performance (Weekend defined as Friday–Saturday)

5. **Insights and Observations**
   - Identified underperforming channels with low realization rates.
   - Detected ADR increase not translating into higher occupancy.
   - Pinpointed seasonal trends and booking behavior differences between weekdays and weekends.

---

## Data Model

The data model follows a star schema with two fact tables and three supporting dimension tables:

- **Fact Tables:**
  - `fact_bookings` – Raw booking-level data
  - `fact_aggregated_bookings` – Aggregated room-level data by date and hotel

- **Dimension Tables:**
  - `dim_date` – Calendar data (day, week, month)
  - `dim_hotels` – Hotel metadata (property ID, name, city, category)
  - `dim_rooms` – Room class and room ID

All tables are connected through proper relationships using keys such as `property_id`, `room_category`, and `check_in_date`.

### Data Model Diagram

![Data Model](https://github.com/eshitakundu/PowerBI-Hospitality-Revenue-Insights/blob/main/Assets/data_model.png)

---

## Features

- Custom DAX measures for accurate and dynamic KPI calculation  
- Drill-through pages for root cause analysis and multi-layered insights  
- Conditional formatting to highlight performance gaps and trends  
- Trend analysis to monitor business movement across time  

---

## Tools Used

- Power BI Desktop – Data modeling, DAX, visualization  
- Power Query – Data transformation and integration  
- Microsoft Excel 

---

## Data Source

The dataset and dashboard mock-up were provided as part of a simulation designed to reflect real-world business challenges in the hotel industry.

---

## Outcome

The final dashboard enables the revenue management team at AtliQ Grands to monitor KPIs in real-time, track performance across various dimensions, and identify root causes for underperformance. The layered design allows stakeholders to explore both high-level summaries and detailed breakdowns efficiently.

---

## Dashboard Preview

