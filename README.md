# Uber_Data_PowerBI_Project

📘 1. Introduction
This project aims to analyze Uber ride fare patterns using a dataset obtained from Kaggle. The goal is to uncover insights regarding fare distribution, ride timings, and peak activity periods. Using Python for preprocessing and Power BI for interactive visualization, this analysis supports data-driven decision-making in urban mobility and pricing strategies.

🧪 2. Methodology
a. Data Collection:
Dataset: Uber Fares Dataset from Kaggle

Features included: fare amount, pickup and dropoff times/locations, and ride identifiers

b. Data Preparation in Python:
Loaded the dataset using pandas

Conducted initial data profiling (shape, nulls, data types)

Cleaned missing values in fare_amount, pickup_datetime, and coordinates

Engineered new features:

hour, day, month from pickup_datetime

day_name (day of week)

peak_hour indicator (1 = peak time)

c. Export and Use in Power BI:
Saved the cleaned dataset as uber_enhanced.csv

Imported into Power BI for visualization and dashboard development

📊 3. Analysis
a. Descriptive Statistics:
Mean fare: ~$11.87

Median fare: $8.50

Fare range: $1 – $500

Majority of fares are under $50

Outliers detected: Extremely high fare values filtered for clarity

b. Key Visuals Created:
Histogram of fare amounts

Line charts for:

Fare amount vs hour of day

Fare amount by month

Bar chart of day_name frequency by year

Pie chart showing distribution between peak/off-peak rides

Table of ride counts by day/hour

Map showing spatial pickup density

Fare bin analysis showing volume by fare ranges

🧠 4. Results
Busiest Ride Hours: Peak between 7–9 AM and 5–8 PM

Most Common Ride Days: Mondays and Fridays

High Fare Times: Late night rides (~11 PM – 1 AM) have slightly higher averages

Fare Patterns:

Most fares fall below $30

Outliers above $100 likely represent airport or long-distance trips

Geographic Insight: Pickup concentration mainly in urban centers (NYC assumed)

✅ 5. Conclusion
The Uber fare dataset reveals strong time-based patterns:

Peak hours significantly impact ride volume and fare averages.

Seasonal and daily variations show predictable trends.

Spatial pickup patterns can guide future resource allocation (e.g., driver distribution).

💡 6. Recommendations
Dynamic Pricing Adjustments:
Increase surge pricing sensitivity during peak hours (especially Friday evenings and Monday mornings).

Driver Allocation Strategy:
Prioritize urban centers with high pickup density during busy periods.

Outlier Monitoring:
Regularly review extremely high fares for fraud, errors, or pricing anomalies.

Marketing Campaigns:
Incentivize riders during low-demand periods (e.g., mid-afternoon weekdays).

Further Data Enrichment:
Combine with weather, traffic, and event data for improved forecasting and trend analysis.
