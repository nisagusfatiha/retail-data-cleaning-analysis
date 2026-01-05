# Retail Data Cleaning & Analysis – DigitalOne Group

## Project Background
This project simulates a real-world case where I was hired as a **Junior Data Analyst** at **DigitalOne Group**, a retail technology company transitioning from offline stores to e-commerce.

The company operates through:
- Offline stores (Jakarta, Depok, Tangerang)
- Online shop (orders from multiple cities across Indonesia)

However, the data was **messy, incomplete, and spread across multiple files**, making it difficult for management to understand business performance.

---

## Data Sources
- **MasterData.xlsx**  
  Contains product, customer, store, and shipping cost data.
- **Transactions.xlsx**  
  Mixed daily transactions from offline & online channels, including returns.
- **Reporting_CaseStudy.xlsx**  
  Main reporting file created for management analysis.

---

## Business Objectives
Management requested a **combined report** to:
- Evaluate store and product performance
- Understand return rates
- Improve data accuracy for decision-making

---

## Data Cleaning & Preparation

### Offline Sales Data
**What I did:**
- Used `XLOOKUP` to retrieve product prices and names from MasterData
- Identified invalid StoreID and ProductID
- Flagged invalid records using `IF`
- Calculated Revenue = Quantity × Price

**Why it matters:**
Invalid IDs lead to incorrect revenue calculations and misleading reports.

---

### Online Sales Data
**What I did:**
- Retrieved product prices, customer tiers, and shipping costs using chained lookups
- Applied discount rates based on customer tier
- Calculated Net Revenue including shipping
- Flagged invalid customers and products

**Key logic:**
Revenue accuracy depends on correct customer, product, and shipping data.

---

## Analysis Performed

### Store Performance Analysis
- Total quantity and revenue per store
- Compared actual sales vs target
- Calculated achievement percentage
- Assigned performance level using `IFS`:
  - Pass
  - Almost
  - Needs Improvement

---

### Online Product Analysis
- Total quantity sold per product
- Return count and return rate
- Product performance level classification:
  - High
  - Medium
  - Low

---

## Business Insights

- Flagging invalid data is critical to avoid incorrect revenue reporting
- Discount programs can increase revenue but may reduce margins
- High shipping costs risk customer churn
- Stores missing targets may be affected by non-data factors such as stock issues or competition
- High return rates are often caused by operational issues, not product quality

---

## Tools & Skills Used
- Microsoft Excel / Google Sheets
- XLOOKUP, IF, IFS
- Data Cleaning & Validation
- Business Analysis
- Analytical Thinking & Storytelling

---

## Analyst Perspective
If this report is presented to the board of directors, the key narrative focuses on:
- Operational efficiency
- Revenue impact
- Customer retention
- Data reliability as the foundation for business decisions
