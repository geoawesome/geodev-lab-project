# Minna flood-exposure mapping

A GeoDev Lab Africa (Cohort One) project, built over twelve months.

## Research question

Which built-up areas of Minna were repeatedly inundated during major rainy-season flood events between 2020 and 2026, and what terrain and drainage characteristics distinguish these areas?

## Why it matters

The result is meant to show where recurrent flooding overlaps human settlement, so that flood-prone built-up areas can be prioritised for drainage improvement, flood mitigation and further investigation. The planned deliverable is an interactive flood-exposure map of Minna: a user selects a flood event and sees where flooding occurred, which settlements were affected, how many people were potentially exposed, and which roads and buildings fall within the affected areas. See `project-brief.md` for the full brief.

## Study area

Chanchaga LGA, Niger State, Nigeria, extracted from GRID3 data. Some layers also cover the wider Chanchaga/Bosso area.

## Coordinate reference systems

All source layers arrived in EPSG:4326 (WGS 84). Working layers in `data/processed/` have been clipped to the study area and reprojected to EPSG:32632 (UTM Zone 32N). Raw files are kept untouched.

## Repository layout

```
geodev-lab-project/
├── README.md              this file
├── project-brief.md       full project brief, data plan and sources
└── my-project/
    └── data/
        ├── Chanchaga_LGA.gpkg          study-area boundary (GRID3)
        ├── Chanchag_Bosso_LGA.gpkg     wider boundary
        ├── project.qgz                 QGIS project
        ├── raw/                        original downloads, EPSG:4326, untouched
        │   ├── Highway.gpkg            OSM roads (5,878 lines)
        │   ├── LandUse.gpkg            OSM land use (620 polygons)
        │   └── data-notes.md           provenance and column notes
        └── processed/                  clipped + reprojected to EPSG:32632
            ├── StudyArea.gpkg
            ├── HighWay_reproj.gpkg
            ├── LandUse_reproj.gpkg
            └── data-notes.md
```

## Data in this repository

The vector layers below are downloaded and, where noted, processed:

- OSM roads (`raw/Highway.gpkg`): extracted via QuickOSM (`highway=*`), 13 Sep 2026. 5,878 line features. The `surface` tag is missing for most features (5,680 nulls), so paved and unpaved cannot be separated everywhere; `name` is populated for only 99 features.
- OSM land use (`raw/LandUse.gpkg`): extracted via QuickOSM (`landuse=*`), 13 Sep 2026. 620 polygon features; `description`, `building`, `religion` and `name` tags are nearly absent.
- Study-area boundaries and the QGIS project file.

## Data still to be added

The following are named in the brief but not yet in the repository:

- Sentinel-1 SAR (Copernicus Data Space) for flood mapping
- ~30 m DEM (OpenTopography) for elevation, slope and flow accumulation
- HydroSHEDS / HydroRIVERS drainage network
- CHIRPS v3 rainfall plus a daily Minna record, to pick major flood periods
- ESRI 10 m land cover for the built-up footprint
- ISRIC SoilGrids 250 m soil properties for infiltration/runoff
- WorldPop ~100 m population for exposure estimates
- JRC Global Surface Water to separate persistent water from event inundation

## Status

Project scaffolding, study-area boundaries and the OSM road and land-use layers are in place, with raw and reprojected copies. The satellite, terrain, rainfall, soil and population datasets, and the flood-mapping and exposure analysis, are still to come.
