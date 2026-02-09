# GIS Workflow Steps

## Step 1: Define Study Area
- Selected Kayaderasseras Creek HUC-12 watershed boundary
- Rationale: hydrologically meaningful analysis unit
- Source: USGS Watershed Boundary Dataset

## Step 2: Prepare Wetlands Data
- Clipped NYS DEC freshwater wetlands to HUC-12 boundary
- Dissolved wetlands by Wetland ID to represent wetland complexes
- Recalculated wetland area using projected geometry

## Step 3: Baseline Wetland Metrics
- Calculated total mapped wetland area
- Calculated percent of watershed composed of wetlands
- Summarized number and size range of wetland complexes

## Step 4: Land-Use Pressure Analysis
- Generated 100-ft and 300-ft buffers around wetlands
- Clipped NLCD land cover to buffer extents
- Reclassified land cover into Developed vs Natural
- Calculated:
  - Area-weighted percent developed land
  - Per-wetland developed land percentages

## Step 5: Infrastructure Proximity Analysis
- Added NYS DOT statewide roads
- Identified roads within 100-ft and 300-ft buffers
- Spatial join to flag wetlands with nearby roads
- Compared surrounding development for wetlands with vs without roads

## Step 6: Synthesis and Interpretation
- Compared land-cover pressure and road proximity
- Evaluated patterns across buffer distances
- Interpreted results at screening level
