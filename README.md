# Kayaderasseras Creek Wetland Screening Analysis

## Project Overview

This project presents a **screening-level GIS analysis of freshwater wetlands** within the **Kayaderasseras Creek HUC-12 watershed** in Saratoga County, New York. The analysis evaluates **surrounding land-use pressure and road infrastructure proximity** to provide spatial context for understanding potential anthropogenic influences on mapped wetlands. All analysis was conducted in **ArcGIS Pro** using publicly available datasets.

This project is intended as a **portfolio example of applied environmental GIS workflows**, not as a regulatory or impact determination.

---

## Study Area

- **Location:** Kayaderasseras Creek HUC-12 watershed, Saratoga County, NY  
- **Boundary Type:** USGS Watershed Boundary Dataset (HUC-12)  
- **Rationale:** Watershed boundaries provide a hydrologically meaningful spatial unit commonly used in wetland and water-resources assessments.

---

## Data Sources

- **Freshwater Wetlands:** New York State DEC freshwater wetlands mapping  
- **Watershed Boundaries:** USGS Watershed Boundary Dataset (HUC-12)  
- **Land Cover:** National Land Cover Database (NLCD)  
- **Road Infrastructure:** New York State Department of Transportation statewide roads  

All datasets were projected to **NAD 1983 UTM Zone 18N** for spatial analysis.

---

## Methods Summary

The analysis was conducted in three primary phases:

### 1. Baseline Wetland Characterization
- Clipped mapped freshwater wetlands to the HUC-12 watershed
- Dissolved wetlands by Wetland ID to represent wetland complexes
- Recalculated wetland area using projected geometry
- Summarized total wetland area, percent of watershed, number of wetland complexes, and size range

### 2. Land-Use Pressure Analysis
- Generated 100-ft and 300-ft buffers around wetlands
- Clipped NLCD land cover to buffer extents
- Reclassified land cover into **Developed** and **Natural** categories
- Calculated:
  - Area-weighted percent developed land within buffers
  - Per-wetland developed land percentages

### 3. Infrastructure Proximity Analysis
- Identified road segments within 100-ft and 300-ft wetland buffers
- Used spatial joins to flag wetlands with nearby roads
- Compared surrounding development for wetlands with and without road proximity

---

## Key Results

- Wetlands are unevenly distributed across the watershed and vary in surrounding land-use context.
- Approximately **6–10% of land within wetland buffers** is classified as developed, depending on buffer distance.
- Wetlands with nearby roads exhibited **higher surrounding development** than wetlands without nearby roads at both 100-ft and 300-ft scales.
- Differences between per-wetland averages and area-weighted results highlight the importance of spatial scale and weighting assumptions.

All results are interpreted as **screening-level indicators**, not measures of ecological condition or regulatory compliance.

---

## Limitations and Assumptions

- Analysis relies on **mapped wetlands only**; unmapped wetlands were not included.
- NLCD land cover is generalized and may not capture fine-scale development.
- Road proximity is used as a **spatial indicator**, not a measure of impact severity.
- No field verification was performed.
- Results represent **associations**, not causal relationships.

---

## Repository Contents

├── report/
│ └── Kayaderasseras_Wetland_Screening_Report.pdf
├── maps/
│ ├── Map1_StudyArea_Wetlands.png
│ ├── Map3_LandCover_Buffer100ft.png
│ ├── Map3_LandCover_Buffer300ft.png
│ └── Map4_Roads_WetlandProximity.png
│ └── pdf_exports/
│     └── Map1_StudyArea_Wetlands.pdf
│     └── Map3_LandCover_Buffer100ft.pdf
│     └── Map3_LandCover_Buffer300ft.pdf
│     └── Map4_Roads_WetlandProximity.pdf
├── gis_project/
│ ├── Kayaderasseras_Wetlands.aprx
│ └── README_Project_Setup.txt
├── data/
│ └── README.Data.md
│ └── Wetland_Buffer_Analysis_Final.gdb.zip
│ └── developed_percent_by_wetland_100ft.csv
│ └── developed_percent_by_wetland_300ft.csv
└── methods/
│ └── Workflow_Steps.md


**Note:** Raw statewide datasets are not included. Only derived analysis products are provided.

---

## Software

- **ArcGIS Pro 3.6**
- Python (for field calculations within ArcGIS Pro)

---

## Intended Use

This repository is intended for:
- GIS and environmental science portfolios
- Demonstration of applied spatial analysis workflows
- Review by hiring managers and technical staff

It is **not intended for regulatory decision-making or site-specific assessment**.

---

## Author

Prepared by **Byron Peregrim**  
Bachelor’s degrees in Biology and Computer Science  
Environmental GIS portfolio project
