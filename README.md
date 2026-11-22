# North Atlantic Fishing Data Analysis Case Study (SQL & Python)

## Project Overview
This end-to-end data analysis case study examines over **1.6 million commercial fishing records** (`full_dataset.csv`) from the North Atlantic to identify how operational factors (vessel length, engine power, engine age, distance), spatial/temporal variables (landing port, fishing patch, month, year), and environmental indicators (`surf_temp`, `nao_index`) relate to catch weight (`weight`) and inflation-adjusted catch value (`value_cpi`)[cite: 12].

## Analytical Process
1. **Ask:** Defined the business task and core metrics for fisheries planners, fleet operators, and marine equipment stakeholders[cite: 12].
2. **Prepare:** Audited `full_dataset.csv` (`1,601,870 rows × 22 columns`) and documented missing values (`surf_temp` missing ~8.01%, while 21 columns are 100% complete)[cite: 12].
3. **Process:** Loaded data into an in-memory **SQLite** database and created a validated table (`fishing_clean`) filtering out invalid negative values[cite: 12].
4. **Analyze (SQL):** Executed structured SQL queries (`GROUP BY`, `HAVING`, `CASE WHEN`, aggregations) across top landing ports, vessel size tiers, engine age groups, and sea surface temperature bands[cite: 12].
5. **Share & Act:** Visualized top-performing landing ports and summarized key operational and environmental findings[cite: 12].

## Tools Used
* **SQL** (`SQLite` in Python)
* **Python** (`pandas`, `matplotlib`)
* **Jupyter Notebook / Kaggle**

## Files in This Repository
* `fishing-data-north-atlantic.ipynb`: Complete SQL and Python analysis notebook with queries, outputs, and visualizations[cite: 12].
