# 📦 Sales Forecasting & Inventory Optimization

> End-to-end data analytics pipeline combining **time-series forecasting** with an **interactive Power BI dashboard** — built on the Superstore dataset to drive smarter inventory decisions.

---

## 🚀 Project Overview

Retailers lose billions annually to stockouts and overstock. This project tackles that problem head-on by:

- **Analyzing 4 years** of transactional sales data (~9,994 orders across the US)
- **Forecasting the next 90 days** of sales using Meta's **Prophet** time-series model
- **Visualizing demand patterns** and inventory insights in a **Power BI dashboard**

The result is a data-driven system that tells you *what will sell*, *when*, and *how much to stock*.

---

## 🛠️ Tech Stack

| Layer | Tools |
|---|---|
| Data Wrangling | Python, Pandas |
| Visualization | Matplotlib, Seaborn |
| Forecasting | Facebook Prophet |
| Dashboard | Power BI |
| Notebook | Jupyter Notebook |

---

## 📁 Repository Structure

```
📦 AI-Powered-Sales-Forecasting-Business-Insights-Dashboard/
├── 📁 Notebook/
│   └── 📓 Sales_Forecasting_Inventory_Optimization_Analysis.ipynb   # Full forecasting, analysis & modeling workflow
│
├── 📁 Dashboard/
│   ├── 📊 Sales_Forecast_Inventory_Optimization_Dashboard.pbix      # Interactive Power BI dashboard
│   └── 🖼️ Dashboard_Images/                                         # Dashboard screenshots
│
├── 📁 Data/
│   ├── 📄 Cleaned_Superstore.csv                                    # Cleaned & transformed dataset
│   ├── 📄 sales_forecast.csv                                        # Complete Prophet forecast output
│   └── 📄 Future_Forecast.csv                                       # 90-day future sales predictions
│
└── 📄 README.md

```

---

## 📊 Key Features

### 🔍 Exploratory Data Analysis
- Category distribution and sub-category demand ranking
- Monthly and yearly sales trend analysis with peak detection
- Shipping time computation (`Ship Date − Order Date`)
- Duplicate detection and data quality checks

### 📈 Time-Series Forecasting with Prophet
- Trained Meta's **Prophet** model on daily aggregated sales (2014–2017)
- Generated **90-day forward forecast** with confidence intervals (`yhat_lower`, `yhat_upper`)
- Captured **weekly and yearly seasonality** components
- Exported forecast data for seamless Power BI integration

### 📉 Inventory Demand Insights
- Identified **top-demand sub-categories** by total quantity sold
- Ranked products to prioritize restocking decisions
- Shipping time trends to optimize fulfillment SLAs

### 📊 Power BI Dashboard
- Interactive filters by Region, Category, Segment, and Ship Mode
- KPI cards for total Sales, Profit, and Quantity
- Forecast vs. Actuals comparison chart
- Sub-category demand heatmap for inventory planning

---

## 📌 Dataset

**Source:** Superstore Sales Dataset (commonly used benchmark dataset)

| Feature | Detail |
|---|---|
| Records | ~9,994 orders |
| Time Range | 2014 – 2017 |
| Columns | 21 (Order ID, Customer, Product, Sales, Profit, Discount, Region, etc.) |
| Engineered Features | `Month-Year`, `Year_Month`, `Shipping Time` |

---

## 🔮 Forecast Snapshot

The Prophet model was trained on daily sales and predicts the next 90 days with:

- **`yhat`** — point forecast (expected sales)
- **`yhat_lower` / `yhat_upper`** — 80% confidence interval
- **Weekly & Yearly seasonality** decomposed separately

```
Forecast horizon: 90 days beyond 2017-12-30
Peak predicted period: Q4 (consistent with historical holiday seasonality)
```

---

## ⚙️ How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/Girishh99/AI-Powered-Sales-Forecasting-Business-Insights-Dashboard.git
cd AI-Powered-Sales-Forecasting-Business-Insights-Dashboard
```

### 2. Install Dependencies
```bash
pip install pandas matplotlib seaborn prophet jupyter
```

### 3. Run the Notebook
```bash
jupyter notebook Sales_Forecasting_Inventory_Optimization_Analysis.ipynb
```

### 4. View the Dashboard
Open `Sales_Forecast_Inventory_Optimization_Dashboard.pbix` in **Power BI Desktop**.

---

## 💡 Business Impact

| Insight | Action |
|---|---|
| Q4 demand spikes identified | Pre-stock high-demand SKUs 6–8 weeks ahead |
| Binders & Paper are top quantity movers | Prioritize warehouse space for office supplies |
| Average shipping time tracked | Flag delayed orders; optimize carrier contracts |
| 90-day sales forecast with confidence bands | Set dynamic reorder points with safety stock buffer |

---

## 📸 Dashboard Preview

> *Open Dashboard/Sales_Forecast_Inventory_Optimization_Dashboard.pbix in Power BI Desktop to explore the full interactive dashboard.*

---

## 🙋 Author

**Girish Kumar**
📧 girish1999k.gk@gmail.com
🔗 https://www.linkedin.com/in/girishhkumar/

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).

---

*If you found this project helpful, drop a ⭐ — it helps others discover it!*
