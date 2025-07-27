#  Uber Fares Dataset Analysis 




##  Student Information
 
**Name:** UMWALI Belyse  

**ID:** 27229

**Group:** A

---

##   Project Overview

This project analyzes historical Uber fare data to uncover trends in ride pricing, durations, peak times, and location patterns. It combines Python-based preprocessing with interactive Power BI visualizations to derive business insights that can support data-driven decision-making in urban transportation.


---

##  Methodology

### a. Data Collection:
- Source: Kaggle Uber Fares Dataset
- Key Features: `fare_amount`, `pickup_datetime`, `pickup_longitude`, `dropoff_latitude`, etc.

### b. Data Preparation (Python):
- Loaded dataset using **pandas**
- Cleaned data: removed nulls, outliers, and incorrect coordinates
- Converted timestamps to datetime format
- Feature Engineering:
  - Extracted `hour`, `day`, `month`, `day_name` from `pickup_datetime`
  - Added `peak_hour` (boolean flag for busy hours)
  - Created `ride_duration_minutes` from `dropoff - pickup`

### c. Export for Power BI:
- Saved enhanced dataset as `uber_enhanced.csv`
- Imported it into **Power BI Desktop**

---

##  Exploratory Data Analysis (EDA)

### a. Descriptive Statistics:
- **Average Fare:** $11.87  
- **Median Fare:** $8.50  
- **Fare Range:** $1 to ~$500  
- **Outliers:** Filtered for values above $100

### b. Visualizations in Power BI:
- Histogram: Fare Distribution
- Box Plot: Fare Amount (via Python Visual)
- Line Chart: Average Fare vs. Hour of Day
- Bar Chart: Rides by Day of Week
- Time Series Chart: Monthly Trends
- Map: Pickup Locations
- Pie Chart: Peak vs Off-Peak Rides
- KPI: Average Fare and Total Rides

---

##  Results

- **Peak Ride Hours:** 7–9 AM & 5–8 PM
- **Busiest Days:** Monday & Friday
- **High Fare Times:** 11 PM – 1 AM
- **Fare Distribution:** Most rides < $30
- **Spatial Insight:** Concentration around city centers

---

##  Conclusion

The analysis revealed clear temporal and geographic trends:
- Peak hours and days heavily influence pricing
- Urban hotspots dominate pickups
- Time-of-day and seasonality create predictable fare patterns

---

##  Recommendations

- **Dynamic Pricing:** Adjust fares during high demand periods (Friday evenings, Monday mornings)
- **Driver Allocation:** Target high-density pickup zones
- **Fraud Detection:** Investigate fare outliers regularly
- **Rider Incentives:** Offer discounts during slow hours (e.g., mid-afternoons)
- **Data Integration:** Enrich dataset with weather, events, or traffic data

---
