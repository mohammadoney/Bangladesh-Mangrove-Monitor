# Bangladesh-Mangrove-Monitor

Objective:
To create an interactive web application that enables users to dynamically explore and analyze mangrove forest health across Bangladesh using NDVI (Normalized Difference Vegetation Index). The app provides both spatial visualization of vegetation density and temporal analysis through point-and-click time series charts.

Data Acquisition:
Mangrove Boundary: Uses the pre-processed national mangrove geometry asset created in the previous project (All_Mangroves_Bangladesh_Asset).
Satellite Imagery: Leverages the MODIS/061/MOD13A2 dataset, which provides pre-computed NDVI values at regular 16-day intervals since 2000.
User Input: Interactive elements (dropdowns, text boxes) allow users to select specific months and years for analysis.

Data Processing:
The application implements a sophisticated processing pipeline:
Input Validation: Robust validation checks for year (2000-present) and month selection, including future-date prevention.
Data Availability Check: Queries the MODIS collection to verify data exists for the selected time period before processing.
NDVI Scaling: Applies the MODIS-specific scale factor (0.0001) to convert raw NDVI values to the standard -1 to 1 range.
Monthly Compositing: Generates a mean NDVI composite for the selected month and year.
Dynamic Visualization: Applies a color palette (red-yellow-green) to represent vegetation density levels.
On-Demand Charting: Creates 13-month time series charts when users click on specific locations within the mangrove area.

Data Analysis:
The application enables multiple analytical approaches:
Spatial Analysis: Visual interpretation of vegetation health patterns across the entire mangrove ecosystem.
Temporal Analysis: Point-specific NDVI time series showing seasonal patterns and long-term trends.
Comparative Analysis: Ability to examine vegetation conditions for any month/year combination since 2000.
Quantitative Assessment: NDVI values categorized into vegetation density classes (low: 0-0.33, moderate: 0.33-0.66, high: 0.66-1.0).

Potential Usage and Impact:
Educational Tool: Allows students and researchers to interactively explore mangrove dynamics without coding expertise.
Conservation Monitoring: Enables regular health checks of mangrove forests by forestry departments and NGOs.
Rapid Assessment: Quick evaluation of mangrove condition after extreme weather events or potential pollution incidents.
Policy Support: Provides accessible data visualization for decision-makers and stakeholders.
Public Awareness: Democratizes access to satellite-based environmental monitoring.

Link of the app: https://ee-mohammadoney.projects.earthengine.app/view/bangladesh-mangrove-monitor
