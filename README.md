# AtliQ Unified Business Insights Dashboard
Engineered a scalable Business Intelligence solution that transitioned legacy Excel reporting into an automated Power BI ecosystem, leveraging Star Schema modeling and advanced DAX to provide real-time visibility into net sales, fiscal performance, and profit margins across massive datasets.

## Dashboard Preview 
<img width="841" height="502" alt="image" src="https://github.com/user-attachments/assets/f03b6eed-7d5c-4a96-a337-7feb60f66b50" />

## Data Architecture & Modeling (Star Schema)
<img width="720" height="450" alt="Project_Screenshot2_updated" src="https://github.com/user-attachments/assets/87d80eb8-162c-4575-93dc-3b5a82b0c8fc" />

The backbone of this project is a high-performance Star Schema (with Snowflake extensions) designed to handle "huge" datasets while maintaining fast report interactivity. By transitioning from flat Excel files to a relational model, I ensured data integrity and optimized calculation speeds.

####Core Modeling Strategy

**Fact Tables**: Centralized transactional data including fact_actual_estimates and fact_forecast_monthly to track sales and predictions separately.

**Dimension Tables**: Created entity-based tables for dim_customer, dim_product, dim_market, and dim_date to act as primary filters.

**Snowflake Normalization**: Further refined the model by connecting dim_market to sub_zones and dim_product to category tables, reducing data redundancy and improving granularity.

By implementing this architecture, I successfully mimicked an OLAP (Online Analytical Processing) system, allowing for seamless drill-down from global KPIs to specific sub-zone performance.

## Project Overview
#### The Business Challenge
In the original Excel environment, data was siloed and reporting was reactive. Key challenges included:

**Scalability Issues**: Excel struggled to process "huge" volumes of transactional data (OLTP-style), leading to slow performance.

**Complex Deductions**: Calculating post-invoice deductions and net sales involved manual, error-prone lookups.

**Fiscal Misalignment**: The business operated on a September-start Fiscal Year, requiring tedious manual adjustments to standard calendar exports.

#### The Solution: An End-to-End BI Pipeline
I developed a robust analytical pipeline following the professional ETL (Extract, Transform, Load) framework:

**Data Extraction & Cleaning**: Used M-Language to build dynamic date tables and optimized the load by disabling staging tables to keep the model lean.

**Data Modeling (OLAP)**: Implemented a Star Schema to connect Fact (transactions) and Dimension (entities) tables for high-performance filtering.

**Advanced Analytics (DAX)**: Leveraged DAX for sophisticated measures, including custom Fiscal Year logic and automated deduction calculations.

## Key Business Insights
Looking at your data for 2020, here are few insights:

#### 1. Profitability Warning (Net Profit %)
   
•	**Insight**: Despite a strong Net Sales of $136.04M, the Net Profit % is -0.94%, which is a massive 142.7% drop compared to the benchmark.

•	**Business Impact**: This indicates that while the company is generating high revenue, the operational costs or deductions are far too high, leading to a net loss.

•	**Actionable Recommendation**: Investigate the "Sub-Region Performance" table, specifically India, which has the highest sales ($33.9M) but a deep negative Net Profit of -14.7%.

#### 2. Supply Chain Inefficiency (Forecast Accuracy)
   
•	**Insight**: Forecast Accuracy stands at 67.28%, which is 22.3% lower than last year.

•	**Business Impact**: The "Sub-Region Performance" table shows many zones marked with EI (Excess Inventory) or OOS (Out of Stock).

•	**Actionable Recommendation**: The high "Net Error %" in regions like NE (22.7%) and SE (24.9%) suggests a need for better demand planning to reduce storage costs of excess inventory.

#### 3. Revenue Concentration

•	**Insight**: The Top 5 Customers account for 54.4% of total Revenue Contribution (RC%).

•	**Business Impact**: High dependency on a few clients (Amazon, Atliq e Store, etc.) poses a risk if any single partnership is terminated.

•	**Observation**: Most top customers and products show a declining trend (red arrows) in Gross Margin %, suggesting pricing pressure or increased cost of goods sold.

#### Technical Stack

**Power BI Desktop**: Core development and visualization.

**Power Query & M-Language**: Data transformation and custom fiscal calendar scripting.

**DAX**: Advanced business logic and time intelligence (YTD, YTG, LE).

**Excel**: Source data and UAT (User Acceptance Testing) via "Analyze in Excel".

**Power BI Service**: Leveraged for cloud-based distribution, configuring scheduled data refreshes to ensure real-time reporting.










