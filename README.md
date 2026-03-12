# 🌾 Global Crop Production Analysis (2000-2023)

![Dashboard Overview](images/dashboard_overview.png)

## 📌 Project Overview
This end-to-end data analytics project analyzes global crop production patterns using FAOSTAT data from 2000-2023. The analysis covers 13 major countries and 6 staple crops, providing insights into production trends, country specialization, and global food supply dynamics.

---

## 🎯 Business Questions Answered
- Which countries are the top producers of major crops?
- How has global crop production evolved over 23 years?
- What crops does each country specialize in?
- Which regions show the fastest production growth?

---

## 🛠️ Tools & Technologies
- **Python** (Pandas, NumPy) - Data cleaning and analysis
- **Jupyter Notebook** - Exploratory data analysis
- **Power BI** - Interactive dashboard creation
- **Git/GitHub** - Version control and portfolio hosting

---

## 📊 Key Insights

### KPI Cards
| Metric | Value |
|--------|-------|
| **Total Production** | 45.7 billion tonnes (2000-2023) |
| **Largest Producer** | China with 8.2 billion tonnes |
| **Most Produced Crop** | Maize (corn) at 27% of global production |
| **Fastest Growth** | Brazil with 245% increase over 23 years |

### Additional Insights
- **Global production grew 85%** from 2000 to 2023
- **China and USA** dominate over 40% of global production
- **Brazil specializes** in soybeans (60% of their production)
- **2021 was the most productive year** on record

---

## 🔄 Data Workflow

### 1. Data Acquisition
- Sourced from FAOSTAT (Food and Agriculture Organization)
- Selected 13 countries across 6 continents
- Time period: 2000-2023

### 2. Data Cleaning (Python)
```python
# Cleaned production data, handled missing values
import pandas as pd

df = pd.read_csv('crop_production_FAOSTAT.csv')
df['Production'] = pd.to_numeric(df['Value'], errors='coerce')
df = df.dropna(subset=['Production'])
df = df.rename(columns={'Area': 'Country', 'Item': 'Crop'})
