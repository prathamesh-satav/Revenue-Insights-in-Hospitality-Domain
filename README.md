# 🏨 Revenue Insights in the Hospitality Domain

This Power BI project provides a comprehensive analysis of revenue data in the hospitality industry. It uses interactive visuals and DAX-based calculations to reveal booking trends, occupancy patterns, and revenue behavior—helping drive smarter business decisions.

## 📈 Project Overview

- Analyze bookings and revenue trends over time
- Classify weekdays vs weekends (custom business logic)
- Identify peak performance periods for hotels and room types
- Use aggregated metrics for quick business insights

## 🧰 Tech Stack

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **.CSV files** as data sources (fact and dimension tables)

## 📂 Datasets Used

- `fact_bookings.csv`: Raw transactional bookings
- `fact_aggregated_bookings.csv`: Pre-aggregated metrics
- `dim_date.csv`: Calendar table with day info
- `dim_hotels.csv`: Hotel dimension
- `dim_rooms.csv`: Room types and metadata

## 🧠 DAX Measures & Calculated Columns

### ✅ Weekday Type
Classifies each date as `Weekday` or `Weekend` (Friday & Saturday = Weekend):

```dax
Weekday Type = 
IF(
    WEEKDAY('dim_date'[date], 2) IN {5, 6}, 
    "Weekend", 
    "Weekday"
)
✅ Day Number
Returns the day of the week as a number (Monday = 1, Sunday = 7):
Day Number = WEEKDAY('dim_date'[date], 2)
📊 Report Features
Revenue and booking visualizations across day types

Slicers by room type, hotel, and booking date

Comparison between weekdays and weekends

Trendlines and aggregated KPIs for business performance

🚀 Getting Started
Clone this repository:

bash
Copy
Edit
git clone https://github.com/prathamesh-satav/Revenue-Insights-in-Hospitality-Domain.git
Open the .pbix file using Power BI Desktop

Ensure local file paths are correct for the data sources (CSV files)

Click Refresh to load the latest data

📌 Use Cases
Revenue forecasting and trend analysis

Hotel staffing and resource allocation

Marketing timing for weekday/weekend promotions

🙌 Contributions
Feel free to fork this project and submit pull requests. Any contributions to expand functionality or optimize the model are welcome.

📄 License
This project is licensed under the MIT License.

css
Copy
Edit

Would you like me to generate a sample badge section (for stars, license, etc.) at the
