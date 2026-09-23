# ✈️ Airline Dashboard - Power BI

## 📌 Project Overview

This project presents a comprehensive **Airline Operations Dashboard** built in Power BI. It analyzes flight performance, customer satisfaction, route profitability, and delay patterns to help airline management make data-driven decisions.

The dashboard has **3 interactive pages**: Flights, Customer, and Routes.

---

## 🎯 Business Objectives

- Track total flights, revenue, and average ticket prices
- Identify delay patterns and root causes
- Analyze customer satisfaction by flyer type
- Compare route profitability and on-time performance
- Find busiest and most delayed routes

---

## 📊 Dashboard Pages & Features

### 1. Flights Page
- **KPI Cards**: Total Flights (1000), Avg Duration (4 hr), Avg Distance (1375 km), Avg Ticket Price (₹7303), Total Revenue (1185M)
- **Map Visual**: Flight routes across India with city markers
- **Max Delayed Flights**: Line chart showing delay trends by airline
- **Flights Status**: Stacked bar chart showing Cancelled vs Completed flights
- **Delay Reasons**: Column chart showing ATC, Crew, On-Time, Technical, Weather
- **Highest Used Flights**: Donut chart showing market share by airline

### 2. Customer Page
- **KPI Cards**: Total Revenue (1185M), Total Passengers (165K), Total Frequent Flyers (501), Avg Satisfaction Score (6.02)
- **Revenue by Flyers**: Bar chart comparing Regular vs Frequent Flyer revenue
- **Avg Satisfaction by Flyers**: Donut chart (Regular: 6.07, Frequent: 5.96)
- **Passengers by Month**: Line chart showing monthly passenger trends (May-Sep)
- **Passengers by Airline**: Bar chart (SkyHigh: 36K, BlueSky: 35K, JetNova: 33K, StarConnect: 31K, AeroFly: 30K)
- **Frequent Flyers by Airline**: Bar chart (SkyHigh: 113, BlueSky: 107, AeroFly: 102, JetNova: 90, StarConnect: 89)

### 3. Routes Page
- **KPI Cards**: Total Revenue (1185M), Avg Ticket Price (₹7303), Total Passengers (165K), Sum of Max Delayed (614), Satisfaction Score Hyderabad (6.39)
- **Max Delayed Routes**: Bar chart (Goa: 75, Bengaluru: 72, Kolkata: 64, Mumbai: 61, Pune: 61, Ahmedabad: 58, New Delhi: 57, Hyderabad: 56, Kochi: 56, Chennai: 54)
- **Profitable Routes**: Line chart (Bengaluru: 135M, Mumbai: 134M, Goa: 134M, Kolkata: 119M, Hyderabad: 116M, Chennai: 114M, Ahmedabad: 112M, Kochi: 108M, New Delhi: 107M, Pune: 107M)
- **On-Time Routes**: Treemap (Mumbai: 49, Kolkata: 46, Bengaluru: 43, Chennai: 40, Hyderabad: 40, Kochi: 37, Goa: 35, New Delhi: 33, Ahmedabad: 33, Pune: 30)
- **Busiest Route**: Bar chart (Goa: 19K, Bengaluru: 19K, Mumbai: 18K, Kolkata: 17K, Chennai: 16K, Ahmedabad: 16K, Hyderabad: 16K, Pune: 15K, Kochi: 15K, New Delhi: 14K)

---

## 🛠️ Tools & Technologies Used

| Tool | Purpose |
| :--- | :--- |
| **Power BI Desktop** | Dashboard creation and visualization |
| **Power Query** | Data cleaning and transformation |
| **DAX** | Calculated measures and KPIs |
| **Excel** | Source data preparation |

---

## 🧮 DAX Measures Used

-- Total Flights
Total Flights = COUNTROWS(Airline)

-- Total Revenue
Total Revenue = SUM(Airline[Revenue])

-- Avg Ticket Price
Avg Ticket Price = AVERAGE(Airline[Ticket_Price])

-- Avg Duration
Avg Duration = AVERAGE('Flight duration hr'[avg duration hr])

-- Total Passengers
Total Passengers = SUM(Airline[Passengers])

-- Total Frequent Flyers
Total Frequent Flyers = SUM(Airline[Frequent_Flyer])

-- Avg Satisfaction Score
Avg Satisfaction Score = AVERAGE(Airline[Satisfaction_Score])

-- Max Delayed
Max Delayed = SUM(Airline[Max Delayed])

-- Flights Count
Flights Count = COUNTROWS(Airline)
