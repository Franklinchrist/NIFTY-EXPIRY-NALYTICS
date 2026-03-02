# FRANKY QUANTY | Nifty Expiry Analytics Dashboard

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Nifty 50](https://img.shields.io/badge/Data-Nifty%2050-orange.svg)](https://www.nseindia.com/)

A professional-grade historical analytics dashboard for **Nifty 50 Expiry Day** behavior. This project analyzes over 300+ expiry sessions (2019-2025) to provide quantitative insights into hourly volatility, directional efficiency, and session classification.

![Dashboard Preview](https://raw.githubusercontent.com/placeholder-image.png)

## 🌟 Key Features

- **Directional Efficiency Ratio (DER)**: Quantifies how "trending" or "rotational" a session is.
- **Hourly Heatmaps**: Visualizes Range %, Range (Pts), and Absolute Move (Pts) for every 1-hour slot of the expiry day.
- **Session Classification**: Automatically classifies sessions into **Trending 🚀**, **Mixed ⚖️**, or **Rotational 🌀**.
- **Historical Database**: Pre-baked with all expiry sessions from 2019 to Present.
- **Password Protected**: Built-in SHA-256 session gate for secure public hosting.

## 📊 Analytics Methodology

### Directional Efficiency Ratio (DER)
The DER is used to measure the quality of a trend during a session:
`DER = abs(Close - Open) / (High - Low)`
- **Trending (> 0.6)**: Clean directional move.
- **Mixed (0.3 - 0.6)**: Choppy with directional bias.
- **Rotational (< 0.3)**: Pure sideways/mean-reversion behavior.

### Hourly Range Calculation
For every 1-hour slot (e.g., 09:15 - 10:15), the dashboard calculates:
- **Range (Pts)**: `High - Low` for that hour.
- **Abs Move (Pts)**: `abs(Close - Open)` for that hour.

## 🛠 Tech Stack

- **Data Processing**: Python (Pandas/JSON)
- **Frontend**: Vanilla HTML5, CSS3 (Custom Design System), JavaScript (ES6+)
- **Security**: SHA-256 Crypto API for session gating.

## 🚀 How to Use

### 1. Local Exploration
Simply open `expiry_heatmap.html` in any modern browser.
- **Access Key**: `nifty` (Default)

### 2. Updating Data
If you have new Nifty 1-minute CSV data:
1. Update your CSV files in the data source.
2. Run the processing scripts.
3. Run `python generate_final_dashboard.py` to bake the new data into the HTML.

### 3. Public Hosting
This project is designed to be hosted on **GitHub Pages**, **Vercel**, or **Netlify**. 
- It is a single-file application (`expiry_heatmap.html`).
- No backend server required.

## 📜 License
This project is licensed under the **MIT License** - meaning it's free to use, modify, and distribute for personal and commercial purposes.

---
**Created by FRANKY QUANTY**
*Quantitative Option Trading Analytics*
