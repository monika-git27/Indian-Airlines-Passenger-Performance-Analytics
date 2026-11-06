
# Indian Airlines Passenger & Performance Analytics | Power BI

## Project Overview

This project focuses on analyzing passenger traffic, airline performance, customer satisfaction, estimated profitability, and operational efficiency across five Indian airlines using Microsoft Power BI.

An interactive dashboard was developed to compare airline performance, identify monthly passenger demand patterns, evaluate operational KPIs, and provide insights into passenger capacity, fuel consumption, and environmental impact.

## Business Objectives

- Compare passenger traffic and seat capacity across Indian airlines.
- Analyze monthly passenger trends to identify demand fluctuations and seasonal patterns.
- Evaluate customer satisfaction through airline ratings.
- Compare estimated profitability across airlines.
- Assess operational efficiency using fuel consumption, flight duration, and passenger capacity utilization.
- Analyze estimated carbon emissions per passenger to understand environmental performance.

## Dashboard Features

### 1. Interactive Airline Analysis

- Airline selection to explore individual airline performance.
- Dynamic route and destination city slicers.
- Passenger capacity and total passenger KPIs.
- Dynamic aircraft image selection.

### 2. Passenger Traffic Analysis

- Monthly passenger trend analysis.
- Airline-wise passenger volume comparison.
- Comparison of passenger traffic across selected airlines.

### 3. Customer Satisfaction

- Airline-wise average customer ratings.
- Comparative analysis of customer satisfaction across carriers.

### 4. Financial Performance

- Estimated profit comparison across airlines.
- Identification of differences in airline profitability.

### 5. Operational & Environmental Performance

- Passenger capacity and utilization analysis.
- Fuel consumption efficiency.
- CO₂ emissions per passenger.
- Average flight duration comparison.

## Key DAX Measures

The following DAX measures were developed to calculate and analyze key performance indicators.

**Total Passengers**
```dax
Total_Passengers =
SUM(Flight_Data[Passengers])
```

**Seat Capacity**
```dax
Seat_capacity =
SUM(Flight_Data[Seat_Capacity])
```

**Average Flight Duration**
```dax
Avg_flight_duration =
AVERAGE(Flight_Data[Flight_Duration_Min])
```

**CO₂ Emissions per Passenger**
```dax
CO2_per_passenger =
DIVIDE(
    SUM(Flight_Data[CO2_Emissions_Tonnes_Est]) * 1000,
    SUM(Flight_Data[Passengers]),
    0
)
```

**Fuel Consumption per 100 km**
```dax
Fuel_Efficiency =
DIVIDE(
    SUM(Flight_Data[Fuel_Used_Litres_Est]) * 100,
    SUM(Flight_Data[Distance_km]),
    0
)
```

## Key Analytical Findings

- IndiGo recorded the highest passenger volume among the five airlines, followed by Air India.
- Monthly passenger trends revealed fluctuations in airline demand throughout the year.
- Customer ratings highlighted differences in passenger satisfaction across airlines.
- Estimated profitability comparisons revealed variations in financial performance.
- Operational KPIs provided insights into fuel consumption, flight duration, and environmental performance.

## Tools & Technologies

- **Power BI Desktop:** Interactive dashboard development and data visualization.
- **DAX:** KPI calculations, analytical measures, and dynamic reporting.
- **Power Query:** Data preparation and transformation.
- **Data Analysis:** Airline performance comparison, passenger traffic analysis, and operational KPI evaluation.

## Business Value

This project demonstrates how airline operational, passenger, customer satisfaction, and financial data can be transformed into interactive visual insights to support performance monitoring and business decision-making.

## Project Deliverables

- Interactive Power BI dashboard.
- Custom DAX measures for airline performance analysis.
- Airline-wise and monthly comparative visualizations.
- Operational and environmental KPI analysis.

---


