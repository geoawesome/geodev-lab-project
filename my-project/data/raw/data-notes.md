# Data notes

## Highway.gpkg
- Source: OpenStreetMap, extracted via QuickOSM (highway=* query)
- Downloaded: 13-Sep-2026
- 5,878 features, lines (LineString)
- Columns: full_id (text), osm_id (text), osm_type (text), highway (text), informal (text), maxspeed (text), maxheight (text), horse (text), cycleway (text), service (text), bridge (text), motor_vehicle (text), foot (text), bicycle (text), line (text), lane_markings (text), layer (text), surface (text), ref (text), oneway (text), name (text), lanes (text), junction (text)
- No nulls in full_id, osm_id, osm_type, highway; all other columns are sparsely populated
- surface tag missing for most features (5,680 nulls); paved and unpaved cannot be separated everywhere
- name populated for only 99 of 5,878 features
- Covers my area of interest completely

## LandUse.gpkg
- Source: OpenStreetMap, extracted via QuickOSM (landuse=* query)
- Downloaded: 13-Sep-2026
- 620 features, polygons (MultiPolygon)
- Columns: full_id (text), osm_id (text), osm_type (text), landuse (text), description (text), building (text), religion (text), name (text)
- No nulls in full_id, osm_id, osm_type, landuse; all other columns are sparsely populated
- description, building, religion, and name tags nearly absent across all features
- Covers my area of interest completely