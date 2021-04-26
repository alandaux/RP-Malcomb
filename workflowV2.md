---
layout: page
title: Malawi Workflow Version 2
---
Created: `12  April 2021`
Revised: `12 April 2021`

## Data
2004 - 2010 DHS w/ GPS
Demographic and health survey (assets & access)
UNEP/grid Europe (biophysical exposure)
Famine early warning network (livelihood)

## Preprocessing of Geographic Boundaries (Step 1)

DHS Households table (1 row/house) → ***field calc*** → conversion to 0-5 scale →
weighted A/C score → ***join by attribute*** w/ DHS data points (village level) →
***spatial join AND group by*** w/ traditional authorities (GADM adm_2) →
traditional authorities w/ Capacity Score → ***Raster***

Livelihood zones → ***copy #s from spreadsheet*** → ***rescale 0-5*** →  ***Rasterize*** → ***Raster Calc*** (w/ Drought Exposure and Flood Risk)

Drought exposure → ***rescale 0-5***

Flood risk → ***rescale 0-5***


## Step 3: Creating the Model of Vulnerability
***Calculate***: Household resilience = adaptive capacity + livelihood sensitivity - biophysical exposure
