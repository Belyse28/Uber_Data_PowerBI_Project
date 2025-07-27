🚖 Uber Fares Dataset Analysis
👩‍🎓 Student Information
Name: UMWALI Belyse

ID: 27229

Group: A

 Project Overview
This project aims to analyze historical Uber ride data to extract meaningful insights about fare trends, ride durations, peak hours, and spatial distribution. With growing urban mobility challenges, data analytics can enhance decision-making in transportation services. The dataset used was obtained from Kaggle and contains detailed records of Uber trips, including timestamps, geographic coordinates, and fare amounts.

Python was used for initial data cleaning, transformation, and feature engineering. Then, Power BI was used to design interactive visualizations and dashboards for exploratory and business analysis. The project concludes with a set of data-driven recommendations to improve operational and strategic decisions.

 Methodology
a. Data Collection
Source: Kaggle – Uber Fares Dataset

File Format: CSV

Key Features:

fare_amount – Fare paid for the trip

pickup_datetime – Timestamp of pickup

pickup_longitude / pickup_latitude – Pickup location

dropoff_longitude / dropoff_latitude – Dropoff location

passenger_count – Number of passengers

b. Data Preparation (Python)
Data preparation steps were executed in Jupyter Notebook using the pandas and datetime libraries:

python
Copy
Edit
import pandas as pd

# Load the dataset
df = pd.read_csv("uber_fares.csv")

# Convert datetime
df['pickup_datetime'] = pd.to_datetime(df['pickup_datetime'])

# Feature engineering
df['hour'] = df['pickup_datetime'].dt.hour
df['day'] = df['pickup_datetime'].dt.day
df['month'] = df['pickup_datetime'].dt.month
df['day_name'] = df['pickup_datetime'].dt.day_name()

# Peak hour indicator
df['peak_hour'] = df['hour'].apply(lambda x: 1 if (7 <= x <= 9) or (17 <= x <= 20) else 0)
➡ Data Cleaning Tasks:

Removed rows with missing or zero values in fare, coordinates

Filtered unrealistic fares (e.g., over $500 or less than $1)

Dropped invalid latitude/longitude entries

c. Ride Duration Feature (if dropoff available)
python
Copy
Edit
df['dropoff_datetime'] = pd.to_datetime(df['dropoff_datetime'])
df['ride_duration_minutes'] = (df['dropoff_datetime'] - df['pickup_datetime']).dt.total_seconds() / 60
d. Exporting to Power BI
python
Copy
Edit
df.to_csv("uber_enhanced.csv", index=False)
This enhanced dataset was then imported into Power BI Desktop for visualization and dashboard creation.

 Exploratory Data Analysis (EDA)
a. Descriptive Statistics
Metric	Value
Mean Fare	~$11.87
Median Fare	~$8.50
Fare Range	$1 to ~$500
Most Common Fare	$6–$15

The majority of fares fell below $30.

Fares exceeding $100 were treated as outliers and analyzed separately.

Peak times showed slightly higher fare averages due to demand surges.

b. Power BI Visualizations
Visualization	Description
Histogram	Distribution of fare amounts
Box Plot	Outlier detection and spread of fares
Line Chart	Average fare trends over hour of the day
Bar Chart	Count of rides by day of the week
Time Series	Monthly trend in average fares
Map	Pickup locations by latitude and longitude
Pie Chart	Share of rides during peak vs. off-peak hours
KPI Card	Key metrics like Average Fare and Total Rides
Table	Ride counts grouped by day/hour

 Results & Insights
a. Temporal Insights
Peak Ride Hours: 7–9 AM and 5–8 PM (morning/evening commutes)

High Fare Times: Slight increase in late-night rides (11 PM – 1 AM)

Busiest Days: Mondays and Fridays showed the highest volume of rides

Weekend Patterns: Slightly lower ride volume but more spread across the day

b. Geographic Insights
High concentration of rides in urban areas, likely within NYC

Consistent pickup clusters around central business districts and transit hubs

c. Fare Patterns
A large portion of fares clustered between $6 and $15

A small set of rides were extremely high in fare, possibly due to airport transfers or longer trips

 Conclusion
This analysis revealed several important patterns in Uber fare behavior:

Temporal dynamics (time of day, day of week) significantly affect ride volume and pricing

Urban regions dominate pickup activity, reinforcing the importance of location-based planning

Fare outliers can distort averages and require special handling during analysis

Feature engineering using timestamps can dramatically improve business understanding

 Recommendations
Area	Suggestion
Pricing	Implement dynamic pricing during busy hours (Friday evenings, Monday mornings)
Driver Allocation	Assign more drivers to zones with high pickup density during rush hours
Fraud Monitoring	Investigate rides with unusually high fares for potential fraud or system errors
Rider Engagement	Offer promotions during off-peak hours to boost demand
Data Enrichment	Integrate additional data sources such as weather or city events to improve forecasting models

