# My project brief

## The question

Which built-up areas of Minna were repeatedly inundated during major rainy-season flood events between 2020 and 2026, and what terrain and drainage characteristics distinguish these areas?

## Why it matters

The answer could help identify neighbourhoods and built-up areas where flooding repeatedly intersects with human settlement. The resulting map could support local planning by showing where flood-prone settlement areas should receive priority for drainage improvement, flood mitigation and further investigation.

## The data I need
- Sentinel-1 SAR imagery for selected pre-flood and flood-period dates in Minna. - https://dataspace.copernicus.eu/data-collections/copernicus-sentinel-missions/sentinel-1

- Digital Elevation Model (DEM) for elevation, slope and flow-accumulation analysis. - https://portal.opentopography.org/raster?opentopoID=OTSDEM.032021.4326.3

- Drainage/river network for distance to drainage and drainage-density analysis.  - https://www.hydrosheds.org/hydrosheds-core-downloads

- CHIRPS rainfall data for identifying major rainfall/flood periods. - https://chc.ucsb.edu/data/chirps3

- Daily rainfall record for Minna

- Land-cover data to identify built-up areas and other surface-cover classes. - https://livingatlas.arcgis.com/landcoverexplorer/

- Soil properties to represent infiltration/runoff conditions.
- https://soilgrids.org/

- Population data to estimate the number of people exposed within flood-affected areas.
- https://hub.worldpop.org/geodata/summary?id=74733

- Road/building data to assess infrastructure exposure.
- https://download.geofabrik.de/africa/nigeria.html

- Historical surface-water data to distinguish recurrent water bodies from event-related inundation. - https://global-surface-water.appspot.com/download

## Where each dataset comes from
1. Sentinel-1 SAR

Source: Copernicus Data Space Ecosystem
Resolution: Sentinel-1 GRD products suitable for flood mapping
Coverage: Global, 2014–present

2. DEM

Source: OpenTopography
Resolution: 1 arc-second (~30 m) available for Africa

OpenTopography provides DEM, flow direction and flow accumulation products, so one source can support several of our terrain/hydrological variables.

3. Drainage

Source: HydroSHEDS / HydroRIVERS

HydroSHEDS provides derived river and hydrological products in addition to its DEM-based products.

4. Rainfall

Source: CHIRPS v3, Climate Hazards Center, UC Santa Barbara
Resolution: 0.05°
Temporal coverage: 1981–near present

CHIRPS v3 provides daily and other temporal products and specifically incorporates satellite rainfall estimates with station observations.

5. Land cover

Source: ESRI Landcover
Resolution: 10 m

WorldCover provides global 10 m land-cover products and is particularly useful for extracting the built-up footprint required by this question.

6. Soil

Source: ISRIC SoilGrids
Resolution: 250 m

SoilGrids provides global soil-property maps, including sand, silt, clay, bulk density and other properties, at 250 m resolution.

7. Population

Source: WorldPop
Resolution: approximately 100 m for the Nigeria population product

WorldPop provides downloadable Nigeria population rasters. The current 2023 product is approximately 100 m and gives estimated population per grid cell.

8. Roads and buildings

Source: OpenStreetMap / Geofabrik Nigeria extract

The Nigeria OSM extract is available in GeoPackage, Shapefile and PBF formats.

9. Historical surface water

Source: JRC Global Surface Water

We can use this as background water evidence, particularly to distinguish persistent/seasonal water from event-related inundation.

## What I will build

I will build an interactive flood-exposure map for Minna showing areas that have experienced satellite-observed inundation during selected major rainy-season events, together with the built-up areas, population and infrastructure affected.

The final product would allow a user to select a flood event and see where flooding occurred, which settlements were affected, how many people were potentially exposed, and which roads/buildings fall within the affected areas.

