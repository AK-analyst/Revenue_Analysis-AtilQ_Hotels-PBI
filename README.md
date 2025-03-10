# Revenue Analysis - AtilQ Hotels - PBI
AtilQ Hotels - Revenue Insights Dashboard: provides key revenue analytics for hotel management. It tracks. occupancy rates, RevPAR, regional performance, and seasonal trends to optimize profitability. Built using **Power BI**, it features interactive visuals, KPIs, and DAX-based calculations for data-driven decisions. 📊🏨

---
### [View Live Dashboard--](https://app.powerbi.com/view?r=eyJrIjoiNjZkMDJjNTYtN2Q3Ni00ZjUyLWI5NWUtNzUwNDBmMzcyY2JjIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)
---
## Problem Statement

This dashboard provides insights into the revenue streams of AtilQ Hotels. It assists the hotel management in understanding revenue distribution across different segments and identifying areas for growth and improvement. By analyzing metrics such as room occupancy rates, revenue per available room (RevPAR), Region and City, the dashboard supports data-driven decision-making to enhance profitability.

Key areas of focus include:
- Identifying high and low-performing segments
- Tracking seasonal trends in revenue
- Assessing the impact of marketing campaigns
- Monitoring customer satisfaction and its correlation with revenue

### Steps Followed

- **Step 1:** Load data into Power BI Desktop from various sources including CSV files  .
- **Step 2:** Open Power Query Editor to clean and transform the data. Enable "Column distribution," "Column quality," and "Column profile" options under the View tab.
- **Step 3:** Ensure column profiling is based on the entire dataset.
- **Step 4:** Identify the relationships between these entities. For example, such as Bookings, Aggregated Bookings, Dates, Rooms, and Revenue.

- **Step 5:** Define relationships between tables using primary and foreign keys. Ensure referential integrity is maintained.
- **Step 6:** Used the "Manage Relationships" tool in Power BI to establish these connections.
- **Step 7:** Use card visuals to display key performance indicators (KPIs) such as total revenue, average daily rate (ADR), and RevPAR.

- **Step 8:** Select a suitable theme for the report under the View tab in the report view.
- **Step 9:** Add key visuals to represent various metrics. For example, use bar charts for Realisation % by metrics, line charts for trends over time, and Donut charts for Revenue by Category.
- **Step 10:** Add slicers for fields like "City", "Room Type", "months" and "Week No" to enable interactive filtering.
- **Step 11:** Create calculated columns and measures using DAX to derive additional insights. For example, calculating RevPAR as follows:


  ```DAX
  1) RevPAR = [Total Revenue] / [Total Available Rooms]

  
  2) Revpar WoW change % =
  VAR selv =
  IF(HASONEFILTER(dim_date[wn]),   
  SELECTEDVALUE(dim_date[wn]),
  MAX(dim_date[wn]))

  VAR revcw =
  CALCULATE([RevPAR], dim_date[wn]= selv)

  var revpw =
  CALCULATE([RevPAR], FILTER(ALL(dim_date), dim_date[wn]=selv-1))
  
  return

  DIVIDE(revcw,revpw,0)-1

- **Step 13:**  Add the company's logo and tagline for branding purposes.
- **Step 14:**  Publish the report to Power BI Service for easy sharing and collaboration.
---
# **Insights**
From the analysis, the following insights were drawn:

## Total Revenue and Occupancy Rates:

The total revenue for the months May, June, July was $1.69 billions.
The average occupancy rate was 57.8%, with the highest rates during the.

## Metrics by Weekday and Weekends: 
![Image](https://github.com/AK-analyst/Revenue_Analysis-AtilQ_Hotels-PBI/blob/main/Screenshot%202025-03-10%20232514.png)



## Top Performing Segments:

### Room Type Preferences:
Luxury rooms had the highest Revenue contribution at 1.04 billions.
whereas Business rooms had the highest Revenue contribution at 647.7 millions.

### Regional Performance:
The top three hotels in terms of revenue are all located in Mumbai. Specifically:

- AtilQ Exotica: This property achieved the highest revenue of 117 million with a total booking count of 7251 and a RevPAR (Revenue per Available Room) of 10629.
- AtilQ Palace: Following closely, this hotel generated 100 million in revenue from 6259 bookings, with a RevPAR of 10592.
- AtilQ Exotica (second listing): Another branch of AtilQ Exotica in Mumbai recorded 98 million in revenue from 6074 bookings, and a RevPAR of 10107.

# Snapshots

Report Snapshot ![Image1](https://github.com/AK-analyst/Revenue_Analysis-AtilQ_Hotels-PBI/blob/main/Screenshot%202025-03-10%20232350.png)
---

ToolTip Snapshot ![Image2](https://github.com/AK-analyst/Revenue_Analysis-AtilQ_Hotels-PBI/blob/main/Screenshot%202025-03-10%20232409.png)
---

