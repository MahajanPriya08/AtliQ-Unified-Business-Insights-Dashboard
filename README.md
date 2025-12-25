# AtliQ Unified Business Insights Dashboard
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

