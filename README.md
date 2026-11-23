# North Atlantic Fishing Data Analysis Case Study (SQL & Python)

## Project Overview
This end-to-end data analysis case study examines over **1.6 million commercial fishing records** (`full_dataset.csv`) from the North Atlantic to identify how operational factors (vessel length, engine power, engine age, distance), spatial/temporal variables (landing port, fishing patch, month, year), and environmental indicators (`surf_temp`, `nao_index`) relate to catch weight (`weight`) and inflation-adjusted catch value (`value_cpi`).

## Analytical Process
1. **Ask:** Defined the business task and core metrics for fisheries planners, fleet operators, and marine equipment stakeholders.
2. **Prepare:** Audited `full_dataset.csv` (`1,601,870 rows × 22 columns`) and documented missing values (`surf_temp` missing ~8.01%, while 21 columns are 100% complete).
3. **Process:** Loaded data into an in-memory **SQLite** database and created a validated table (`fishing_clean`) filtering out invalid negative values.
4. **Analyze (SQL):** Executed structured SQL queries (`GROUP BY`, `HAVING`, `CASE WHEN`, aggregations) across top landing ports, vessel size tiers, engine age groups, and sea surface temperature bands.
5. **Share & Act:** Visualized top-performing landing ports and summarized key operational and environmental findings.

## Tools Used
* **SQL** (`SQLite` in Python)
* **Python** (`pandas`, `matplotlib`)
* **Jupyter Notebook / Kaggle**

## Files in This Repository
* `fishing-data-north-atlantic.ipynb`: Complete SQL and Python analysis notebook with queries, outputs, and visualizations.

## Educational Context, Data Sources and Reuse

This is an independent educational portfolio analysis of a compiled public dataset. It is not commissioned by or endorsed by the data publishers.

Compilation: Alexander Bader, Fishing Data North Atlantic, https://www.kaggle.com/datasets/alexanderbader/fishing-data-north-atlantic . The Kaggle page labels the compilation CC0 and links this source summary: https://raw.githubusercontent.com/ambader/aa_map/main/data_summary.pdf .

The summary identifies catch and vessel data from Fiskeridirektoratet, the Norwegian Directorate of Fisheries, alongside environmental and geographic inputs. Source raw data: Fiskeridirektoratet. The publisher's reuse conditions require attribution under the Norwegian Licence for Open Government Data (NLOD): https://www.fiskeridir.no/statistikk-tall-og-analyse/lisens-for-bruk-av-fiskeridirektoratets-data . License reference: https://data.norge.no/nlod/en/1.0 . Original source category: https://www.fiskeridir.no/statistikk-tall-og-analyse/data-og-statistikk-om-yrkesfiske/apne-data-fangstdata-seddel-koblet-med-fartoydata .

This analysis loads the compilation into SQLite, filters invalid negative measures, groups records and produces aggregate comparisons and charts. These transformations and interpretations are the portfolio author's work, not recommendations by the original publishers. The CC0 compilation label is not presented as removing rights or conditions belonging to upstream sources.

The compilation summary also references sea-surface-temperature, NOAA and geocoding inputs. One referenced SST product is openly shared by NASA Earthdata: https://www.earthdata.nasa.gov/data/catalog/pocloud-amsre-remss-l3u-v7a-7a . The precise provenance and historic terms for every environmental/geocoding component have not been fully verified. OpenCage's current terms require respecting the licenses of returned results: https://opencagedata.com/terms . Its source list is at https://opencagedata.com/credits .

This repository should link to the compilation and official sources rather than rehost the compiled raw dataset while those details remain unresolved. The notebook's code license does not override upstream data terms.
