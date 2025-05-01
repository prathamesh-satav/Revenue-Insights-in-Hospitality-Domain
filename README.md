**🏨 Revenue Insights in the Hospitality Domain**
This Power BI project provides a comprehensive analysis of revenue data within the hospitality industry. By leveraging interactive dashboards and DAX calculations, it offers valuable insights into booking patterns, revenue streams, and occupancy trends to aid in strategic decision-making.

📈 Project Overview
The objective of this project is to analyze historical booking data to:

Identify revenue trends across different time periods.

Understand occupancy rates and booking patterns.

Classify days into weekdays and weekends based on business logic.

Provide actionable insights to optimize revenue management.

🧰 Tools and Technologies
Power BI Desktop: For data visualization and dashboard creation.

DAX (Data Analysis Expressions): For creating calculated columns and measures.

CSV Files: As data sources for the analysis.

📂 Dataset Description
The analysis is based on the following datasets:

dim_date.csv: Contains date-related information.

dim_hotels.csv: Details about hotel properties.

dim_rooms.csv: Information on room types and capacities.

fact_bookings.csv: Raw booking data.

fact_aggregated_bookings.csv: Aggregated booking metrics.

🔍 Key Metrics and DAX Implementations
1. Weekday Type Classification
Categorizes each date as a 'Weekday' or 'Weekend' based on custom business logic where Fridays and Saturdays are considered weekends.

dax
Copy
Edit
Weekday Type = 
IF(
    WEEKDAY('dim_date'[date], 2) IN {5, 6}, 
    "Weekend", 
    "Weekday"
)
2. Day Number Extraction
Assigns a numerical value to each day of the week, starting from Monday as 1 through Sunday as 7.

dax
Copy
Edit
Day Number = WEEKDAY('dim_date'[date], 2)
📊 Dashboard Features
Revenue Overview: Visual representation of total revenue over selected time frames.

Occupancy Trends: Insights into room occupancy rates and patterns.

Booking Analysis: Breakdown of bookings by day type and room categories.

Custom Filters: Interactive slicers for dynamic data exploration.

🚀 Getting Started
Clone the repository:

bash
Copy
Edit
git clone https://github.com/prathamesh-satav/Revenue-Insights-in-Hospitality-Domain.git
Open the PowerBI_Weekday_Analysis.pbix file in Power BI Desktop.

Ensure that the data sources (CSV files) are correctly linked. If prompted, update the file paths to match your local directory structure.

Refresh the data to load the latest information into the dashboard.

📌 Use Cases
Revenue Management: Identify peak revenue periods and optimize pricing strategies.

Operational Planning: Allocate resources effectively based on occupancy trends.

Strategic Decision-Making: Use insights to inform marketing campaigns and promotional offers.

🤝 Contributing
Contributions are welcome! If you have suggestions for improvements or additional features, feel free to fork the repository and submit a pull request.

📄 License
This project is licensed under the MIT License.
