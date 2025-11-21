📊 PhonePe Pulse — India Digital Payments Dashboard
Data Analytics Project | Power BI | Labmentix Internship
📁 Project Overview

This project presents an interactive Power BI dashboard built using the PhonePe Pulse dataset, showcasing insights into India's rapidly growing digital payment ecosystem.
The dashboard analyzes ₹121.41T worth of transactions, 5B+ user registrations, and provides a detailed breakdown of payment types, state-level performance, and year-on-year growth.

This project was completed as part of my Data Analytics Internship at Labmentix.

🎯 Objective

To transform raw PhonePe Pulse data into a meaningful and visually compelling analytics dashboard that helps stakeholders:

Understand digital payment growth in India

Compare state-level performance

Identify transaction behavior patterns

Analyze user adoption trends

Derive actionable insights using data

🧩 Dataset Summary

The project uses two key datasets:

1. aggregated_transaction.csv

Contains:

states

year

quarter

trans_type

trans_counts

amount

2. aggregated_user.csv

Contains:

states

year

quarter

brand

user_counts

🏗️ Data Processing

Performed in Power Query:

Cleaned and transformed raw CSVs

Converted data types

Removed noise and inconsistencies

Created a date hierarchy (Year → Quarter)

Built calculated columns and measures using DAX

🧮 Key DAX Measures

Some of the important measures used:

Total Amount = SUM(aggregated_transaction[amount])

Total Transactions = SUM(aggregated_transaction[trans_counts])

Average Transaction Value =
DIVIDE([Total Amount], [Total Transactions])

Total Users = SUM(aggregated_user[user_counts])

CAGR Calculation
CAGR =
VAR MinYear = CALCULATE(MIN(aggregated_transaction[year]), ALL(aggregated_transaction))
VAR MaxYear = CALCULATE(MAX(aggregated_transaction[year]), ALL(aggregated_transaction))
VAR Years = MaxYear - MinYear
VAR StartVal = CALCULATE([Total Amount], aggregated_transaction[year] = MinYear)
VAR EndVal = CALCULATE([Total Amount], aggregated_transaction[year] = MaxYear)
RETURN
(POWER(EndVal / StartVal, 1 / Years) - 1)

📊 Dashboard Features
🔹 1. KPI Cards

Total Amount

Total Users

CAGR %

Total Transactions

Avg. Ticket Size

🔹 2. India Geo Map

Visualizes transaction intensity across states.

🔹 3. Year-on-Year Transaction Growth

Bar chart showing exponential rise from 2018–2022.

🔹 4. Transaction Type Split

Pie chart showing dominance of Peer-to-Peer payments.

🔹 5. State-wise Transaction Amount

Horizontal bar chart ranking top-performing states.

🔹 6. Brand-wise User Summary

Table showing user counts, total amount, and transaction counts across smartphone brands.

🔹 7. Interactive Filter Panel

Year

Quarter

States

Transaction Type

Top-N Slider

Clear All button

🧠 Insights & Findings

India’s digital payments grew 150% CAGR, driven by UPI adoption.

Peer-to-Peer payments contribute 80%+ of total amount.

States like Telangana, Maharashtra, and Karnataka lead in transaction volume.

Registered user base shows strong growth with consistent penetration across regions.

🛠️ Tools & Technologies

Power BI (Primary Tool)

Power Query

DAX

CSV Processing

Data Modeling

PhonePe Pulse Dataset

📸 Dashboard Preview

(Add your dashboard screenshot here)

📦 Project Structure
📁 phonepe-dashboard/
│── 📄 aggregated_transaction.csv
│── 📄 aggregated_user.csv
│── 📄 phonepe_pulse_dashboard.pbix
│── 📄 README.md
│── 📄 dashboard_screenshot.png

🚀 How to Use

Clone this repository

Download the .pbix file

Open using Power BI Desktop

Explore filters and interactive visuals

💼 About the Intern

This project was completed during my Data Analytics Internship at Labmentix, where I worked on real-world analytics scenarios, dashboard design, and business intelligence concepts.

🔗 Connect With Me

If you’d like to collaborate, discuss this project, or explore analytics solutions, feel free to reach out!