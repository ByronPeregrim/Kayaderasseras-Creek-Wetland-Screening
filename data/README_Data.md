# Data Folder Contents

This folder contains **derived datasets and summary tables** produced as part of the Kayaderasseras Creek wetland screening analysis. Only final or near-final outputs are included. Raw statewide datasets are intentionally excluded.

---

## Vector Data

### Wetland_Buffer_Analysis_Final.gdb.zip
Zipped File Geodatabase containing final derived spatial layers used for analysis and mapping, including:
- Kayaderasseras Creek HUC-12 study area boundary
- Dissolved freshwater wetland complexes
- 100-ft and 300-ft wetland buffers
- Road proximity layers identifying roads within wetland buffers

All feature classes are projected to **NAD 1983 UTM Zone 18N**.

---

## Summary Tables

### developed_percent_by_wetland_100ft.csv
Summary table containing the percentage of developed land within **100 ft** of each mapped wetland complex. Values were calculated using reclassified NLCD land cover clipped to wetland buffer extents and summarized by Wetland ID.

### developed_percent_by_wetland_300ft.csv
Summary table containing the percentage of developed land within **300 ft** of each mapped wetland complex. Values were calculated using the same method as the 100-ft analysis, using the larger buffer distance.

These tables were used to calculate descriptive statistics reported in the Results section and were also joined to spatial feature classes for proximity analysis.

---

## Excluded Data

The following data are **not included** in this repository:
- Raw NLCD raster datasets
- Original statewide freshwater wetlands datasets
- Statewide road network source data
- Intermediate or temporary processing layers

These datasets are publicly available from their respective agencies and are cited in the project report and README.
