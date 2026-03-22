<img width="1188" height="657" alt="Screenshot 2026-03-22 181311" src="https://github.com/user-attachments/assets/c812f47a-5a3b-408c-8890-47afefe85924" />

https://app.powerbi.com/view?r=eyJrIjoiMDIyYTQ4MjUtYTY2MC00MDczLWFkMWYtZjAyNGQwNDAwYzFlIiwidCI6ImQzOGI4YmJiLTg0MDYtNDVhMC05M2JiLWI0MDZkMjAwY2YzYiJ9
📌 Project Story (End-to-End Journey)

This project started with a simple goal:
👉 “Can I convert raw API weather data into a fully interactive analytics dashboard?”

Instead of just visualizing data, I built a complete data pipeline + BI solution from scratch.

🔄 Step 1: Data Collection (API Integration)
Used Weather API to fetch:
🌡️ Current weather data
📅 Forecast (daily + hourly)
Collected data for multiple cities:
Mumbai, Pune, Sambhaji Nagar, Bangalore, Hyderabad, Delhi

Each city’s API response was initially handled separately to ensure data accuracy.

🧱 Step 2: Data Transformation (Power Query)

Performed full ETL process:

Extracted:
Current weather
Forecast (day-wise & hour-wise)
Combined all cities into a single Master Table
Removed duplicate records
Cleaned API issues (e.g., fixed // → https:// for icons)
Final Tables Created:
Current → real-time weather & AQI
Forecast_Day → daily trends + sunrise/sunset
Forecast_Hours → hourly data + rain probability
⭐ Step 3: Data Modeling (Star Schema)

Designed a clean and scalable model:

🔹 Dimension Table:
Location (Created using DAX)
Location = SUMMARIZE('Current', 'Current'[location.name])
🔹 Relationships:
Location → Current (1:1)
Location → Forecast_Day (1:M)
Location → Forecast_Hours (1:M)

This ensures:
✔ Fast filtering
✔ Clean structure
✔ Scalable model

📐 Step 4: Data Pipeline Architecture End-to-End Flow: Weather
& Air Quality data fetched using Weather APIs Secure API authentication 
using API keys Data cleaning and transformation Star Schema data modeling 
(Fact & Dimension tables) Dataset published to Power BI Service Dashboard 
created using the semantic model Scheduled refresh configured (once per day)

🎨 Step 5: Dashboard Design (UI/UX)

Designed a modern, dark-themed interactive dashboard

🔘 Key UI Elements:
City Selector (Button Slicer)
Background PNG (custom theme)
Dynamic Text:
Weather condition (Sunny, Cloudy, etc.)
Selected location name
Last updated timestamp
📊 Step 6: Visualizations
🌡️ Current Weather Cards
Temperature
Humidity
Visibility
UV Index
Wind Speed
Pressure
📅 Forecast Insights
7-Day Temperature Trend (Line Chart)
Forecast Cards (Temp + Icons)
Sunrise 🌅 / Sunset 🌇
🌧️ Rain Analytics
Chance of Rain (%)
🌫️ Air Quality Monitoring
CO, NO₂, SO₂, O₃, PM2.5, PM10
Color-coded AQI indicators
City-wise AQI comparison (Pie Chart)
🚀 Dashboard Features
🌍 Multi-city analysis
🔄 Dynamic filtering by city
📈 Forecast trend visualization
🌫️ AQI health monitoring
🎯 Clean & interactive UI
⚡ Real-time feel with API data
🎯 Business Value / Insights

This dashboard helps users:

Plan daily activities based on weather
Monitor pollution levels in different cities
Compare environmental conditions
Make health-conscious decisions
🛠️ Tech Stack
Data Source: Weather API
ETL Tool: Power Query
Modeling: Star Schema
Visualization: Power BI
Language: DAX
Deployment: Power BI Service
🔮 Future Improvements
📊 Historical trend analysis
🤖 AQI-based health recommendations
🚨 Weather alerts system
🌐 Real-time streaming data
📚 Skills Demonstrated
API Data Handling
Data Cleaning & Transformation
Data Modeling (Star Schema)
DAX Calculations
Dashboard Design (UI/UX)
Business Intelligence Development
