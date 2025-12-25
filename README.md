*# AtliQ Unified Business Insights Dashboard
Engineered a scalable Business Intelligence solution that transitioned legacy Excel reporting into an automated Power BI ecosystem, leveraging Star Schema modeling and advanced DAX to provide real-time visibility into net sales, fiscal performance, and profit margins across massive datasets.

## Dashboard Preview 
<img width="841" height="502" alt="image" src="https://github.com/user-attachments/assets/f03b6eed-7d5c-4a96-a337-7feb60f66b50" />

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

#### Key Business Insights
Looking at your data for 2020, here are few insights:

1. **Profitability Warning (Net Profit %)**
   
•	**Insight**: Despite a strong Net Sales of $136.04M, the Net Profit % is -0.94%, which is a massive 142.7% drop compared to the benchmark.

•	**Business Impact**: This indicates that while the company is generating high revenue, the operational costs or deductions are far too high, leading to a net loss.

•	**Actionable Recommendation**: Investigate the "Sub-Region Performance" table, specifically India, which has the highest sales ($33.9M) but a deep negative Net Profit of -14.7%.

3. **Supply Chain Inefficiency (Forecast Accuracy)**
•	Insight: Forecast Accuracy stands at 67.28%, which is 22.3% lower than last year.
•	Business Impact: The "Sub-Region Performance" table shows many zones marked with EI (Excess Inventory) or OOS (Out of Stock).
•	Actionable Recommendation: The high "Net Error %" in regions like NE (22.7%) and SE (24.9%) suggests a need for better demand planning to reduce storage costs of excess inventory.

5. Revenue Concentration
•	Insight: The Top 5 Customers account for 54.4% of total Revenue Contribution (RC%).
•	Business Impact: High dependency on a few clients (Amazon, Atliq e Store, etc.) poses a risk if any single partnership is terminated.
•	Observation: Most top customers and products show a declining trend (red arrows) in Gross Margin %, suggesting pricing pressure or increased cost of goods sold.


