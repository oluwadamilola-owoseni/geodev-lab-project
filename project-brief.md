My project brief



The question

Which settlements in Ado-Ekiti are located on low-lying land near watercourses?

Why it matters


Ado-Ekiti has no accessible, up-to-date map showing which settlements are most exposed to flooding, despite flooding being a recurring hazard in the town. A static map goes stale the moment conditions change. Local planners, emergency responders, and residents could use a live view of current risk to prioritize drainage improvements, target flood preparedness efforts, and know which areas warrant caution right now, not just historically.


The data I need

Nigeria Settlement extents - GRID3 - [Settlement extents](https://data.grid3.org/datasets/GRID3::grid3-nga-settlement-extents-v4-1/about) 

Ward/LGA boundaries - GRID3 - [LGA\_Boundaries](https://stg-arcgisazurecdataprod3.az.arcgis.com/exportfiles-61962-878/NGA_LGA_Boundaries_2_2609687066015738692.zip?sv=2025-05-05&st=2026-09-04T10%253A45%253A47Z&se=2026-09-04T11%253A50%253A47Z&sr=b&sp=r&sig=bTxelESCJSp8sliv3sUL%252BrDEZuxujgtZIinOPQVTMic%253D) 

Watercourses (rivers/streams) - [Watercourses](https://s3.dualstack.us-east-1.amazonaws.com/production-raw-data-api/default/Ado_Ekiti_Ekiti_shp_uid_e7303b6f-8d46-4ae4-a518-b8322f8ad8d6.zip), via HOT export tool from OpenStreetMap, filtered to Ado-Ekiti

Elevation - Copernicus GLO-30 DEM  - [DEM](https://ot-data3.sdsc.edu/appRasterSelectService1788521792358832779767/rasters_COP30.tar.gz) - GeoTIFF, 30 m resolution

What I would build


A system with two parts working together. First, a base flood-vulnerability layer, built once from the static data: every settlement in Ado-Ekiti LGA flagged as within 200 metres of a watercourse and sitting in low-lying land. Second, a live layer that checks rainfall on a schedule (for example, hourly) and raises the flagged risk level for those same settlements when rainfall crosses a chosen threshold, then lowers it again once conditions ease. The output would be a dashboard or simple map a local planner, emergency responder, or resident could check at any time to see which settlements are at elevated risk right now, not just which ones were flagged in a one-time study. 
