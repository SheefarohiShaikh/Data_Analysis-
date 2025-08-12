# Shopify Sales Analysis - Power BI Project

## 📊 Project Overview

This Power BI project provides comprehensive analysis of Shopify sales data, delivering actionable insights into sales performance, customer behavior, product trends, and business growth metrics. The dashboard enables data-driven decision making for e-commerce operations.

## 🎯 Key Objectives

- **Sales Performance Analysis**: Track revenue trends, seasonal patterns, and growth metrics
- **Customer Analytics**: Understand customer behavior, segmentation, and lifetime value
- **Product Performance**: Identify top-performing products and category trends
- **Geographic Insights**: Analyze sales distribution across regions and markets
- **Inventory Management**: Monitor stock levels and product turnover rates
- **Marketing ROI**: Evaluate campaign effectiveness and channel performance

## 🏗️ Project Structure

```
shopify-sales-analysis/
├── data/
│   ├── raw/                    # Original Shopify export files
│   ├── processed/              # Cleaned and transformed data
│   └── sample/                 # Sample data for testing
├── reports/
│   ├── shopify-sales-dashboard.pbix    # Main Power BI report file
│   └── templates/              # Report templates
├── scripts/
│   ├── data-cleaning.py        # Data preprocessing scripts
│   └── export-automation.py    # Shopify API data extraction
├── documentation/
│   ├── data-dictionary.md      # Field definitions and descriptions
│   └── business-requirements.md
└── images/
    └── dashboard-screenshots/  # Visual documentation
```

## 📈 Dashboard Features

### Sales Overview
- **Revenue Metrics**: Total sales, average order value, sales growth rate
- **Time Series Analysis**: Daily, weekly, monthly, and yearly trends
- **Sales Funnel**: Conversion rates and drop-off points
- **Performance KPIs**: Year-over-year comparisons and target tracking

### Customer Analytics
- **Customer Segmentation**: RFM analysis (Recency, Frequency, Monetary)
- **Lifetime Value**: CLV calculations and customer retention rates
- **Geographic Distribution**: Sales by country, state, and city
- **Customer Acquisition**: New vs. returning customer metrics

### Product Analysis
- **Top Performers**: Best-selling products and categories
- **Inventory Insights**: Stock levels, turnover rates, and reorder points
- **Pricing Analysis**: Price optimization opportunities
- **Product Mix**: Revenue contribution by category

### Marketing & Channels
- **Traffic Sources**: Performance by marketing channel
- **Campaign ROI**: Cost per acquisition and return on ad spend
- **Conversion Rates**: Channel-specific conversion metrics
- **Attribution Analysis**: Multi-touch attribution modeling

## 🔧 Technical Requirements

### Software Requirements
- **Power BI Desktop** (Latest version recommended)
- **Power BI Pro/Premium** (for sharing and collaboration)
- **Microsoft Excel** (for data validation)
- **Python 3.8+** (for data preprocessing scripts)

### Data Sources
- **Shopify Admin API**: Real-time data connection
- **CSV Exports**: Manual data imports from Shopify admin
- **Google Analytics**: Web traffic and behavior data
- **Marketing Platforms**: Facebook Ads, Google Ads data

### Power BI Components Used
- Power Query for data transformation
- DAX measures for calculated metrics
- Custom visuals from AppSource
- Row-level security for data governance

## 🚀 Setup Instructions

### 1. Data Preparation
```bash
# Clone the repository
git clone https://github.com/yourusername/shopify-sales-analysis.git

# Install Python dependencies
pip install -r requirements.txt

# Run data cleaning script
python scripts/data-cleaning.py
```

### 2. Power BI Configuration
1. Open `shopify-sales-dashboard.pbix` in Power BI Desktop
2. Update data source connections:
   - Navigate to Transform Data > Data source settings
   - Update file paths to match your local directory structure
3. Refresh data to load latest information
4. Verify all visualizations are displaying correctly

### 3. Shopify API Integration (Optional)
```python
# Configure API credentials in config.py
SHOPIFY_API_KEY = "your_api_key"
SHOPIFY_PASSWORD = "your_password"
SHOP_NAME = "your_shop_name"

# Run automated data extraction
python scripts/export-automation.py
```

## 📊 Key Metrics & KPIs

### Sales Metrics
- **Total Revenue**: Sum of all completed orders
- **Average Order Value (AOV)**: Revenue / Number of Orders
- **Sales Growth Rate**: ((Current Period - Previous Period) / Previous Period) × 100
- **Conversion Rate**: Orders / Website Sessions × 100

### Customer Metrics
- **Customer Acquisition Cost (CAC)**: Marketing Spend / New Customers
- **Customer Lifetime Value (CLV)**: Average Order Value × Purchase Frequency × Customer Lifespan
- **Repeat Purchase Rate**: Customers with >1 Order / Total Customers × 100
- **Churn Rate**: Customers Lost / Total Customers × 100

### Product Metrics
- **Inventory Turnover**: Cost of Goods Sold / Average Inventory Value
- **Gross Margin**: (Revenue - COGS) / Revenue × 100
- **Product Performance Score**: Weighted score based on sales, margin, and velocity

## 🔍 Data Dictionary

| Field Name | Description | Data Type | Source |
|------------|-------------|-----------|---------|
| order_id | Unique order identifier | String | Shopify Orders API |
| customer_id | Unique customer identifier | String | Shopify Customers API |
| order_date | Date when order was placed | DateTime | Shopify Orders API |
| total_price | Total order value including tax | Decimal | Shopify Orders API |
| product_title | Name of the product | String | Shopify Products API |
| quantity | Number of items ordered | Integer | Shopify Orders API |
| customer_city | Customer's city | String | Shopify Customers API |
| traffic_source | Marketing channel source | String | UTM Parameters |

## 📋 Usage Guidelines

### Refreshing Data
- **Manual Refresh**: Use the Refresh button in Power BI Desktop
- **Scheduled Refresh**: Configure automatic refresh in Power BI Service
- **Real-time Updates**: Set up DirectQuery for live data connections

### Filtering and Slicing
- Use date slicers to analyze specific time periods
- Apply product category filters for focused analysis
- Utilize geographic filters for regional insights
- Implement customer segment filters for targeted analysis

### Exporting Reports
- Export to PDF for executive presentations
- Export to Excel for detailed data analysis
- Share via Power BI Service for collaborative access
- Embed in websites using Power BI Embedded

## 🎨 Customization Options

### Visual Customizations
- Modify color schemes to match brand guidelines
- Add company logos and branding elements
- Customize chart types based on preference
- Create additional calculated columns and measures

### Adding New Metrics
```dax
// Example: Customer Lifetime Value
CLV = 
DIVIDE(
    [Average Order Value] * [Purchase Frequency] * [Customer Lifespan],
    1,
    0
)
```
