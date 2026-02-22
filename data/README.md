# Data

## Folder Structure

- **`raw/`** — Unprocessed sensor data from monitoring stations (available after station deployment in 2027)
- **`processed/`** — Cleaned, analysis-ready datasets produced through the data exploration notebooks
- **`public-sources/`** — Publicly available water quality datasets used for Phase 0 prototyping

## Public Data Sources

Until campus monitoring stations are operational, we use publicly available South Florida water quality data for prototyping and instruction:

| Source | Description | URL |
|--------|-------------|-----|
| **EPA STORET / WQX** | Water Quality Exchange — national water quality monitoring data | https://www.epa.gov/waterdata/storage-and-retrieval-and-water-quality-exchange |
| **USGS NWIS** | National Water Information System — real-time and historical water data | https://waterdata.usgs.gov/nwis |
| **SFWMD DBHYDRO** | South Florida Water Management District environmental database | https://www.sfwmd.gov/science-data/dbhydro |

## Data Privacy & QA/QC

- **No student personally identifiable information (PII)** is stored in this repository
- All environmental data collection follows the EPA-approved Quality Assurance Project Plan (QAPP)
- Raw sensor data undergoes validation before use in instruction (see notebooks in `01-data-exploration/`)

*Note: Large data files may be stored using Git LFS or hosted externally with download links in the notebooks.*
