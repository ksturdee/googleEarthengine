# Google Earth Engine: Marine and Environmental Mapping

I use this repository to document my work with Google Earth Engine (GEE) and its JavaScript API. The scripts are a mix of MB5370 learning exercises and exploratory mapping projects. They cover terrain, protected areas, climate, population, night-time lights, coral habitat and deep-ocean ecosystems.

## Background and aims

The early scripts introduce JavaScript and GEE, then use spatial filters and image operations to explore environmental datasets. Later scripts examine population and nighttime-light change near coastlines, estimate nearby coral habitat around research stations, and map deep-ocean depth zones alongside seabed exploration areas.

## Repository contents

| File | Focus |
|------------------------------------|------------------------------------|
| `01_javascript_information` | JavaScript basics and introductory Earth Engine commands |
| `02_visualising_park_boundaries` | SRTM topography, protected areas and spatial filtering around New Zealand |
| `03_computations_on_images` | Terrain calculations and elevation and slope summaries for Egmont National Park (Taranaki) |
| `04_WORLDCLIMdata` | WorldClim temperature layers and a 2017 Landsat 8 median image |
| `05_nightlights` | Population and night-time-light comparisons, including coastal grid summaries |
| `06_AllenCoralAtlas` | Coral and algae area within 800 m of selected research stations |
| `mapping_deep_ecosystems` | ETOPO1-based depth zones, a slope-based canyon layer and seabed exploration areas |
| `ErthEngineMB5370.Rproj` | RStudio project settings |

The scripts are JavaScript for the Earth Engine Code Editor. Outputs are generated in Earth Engine when a script is run; they are not saved as files in this repository.

## Data sources

The scripts mainly use datasets from the [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets):

| Analysis | Dataset or asset used |
|------------------------------------|------------------------------------|
| Elevation and terrain | CGIAR SRTM 90 m (`CGIAR/SRTM90_V4`) |
| Protected areas and country boundaries | World Database on Protected Areas (`WCMC/WDPA/current/polygons`); LSIB Simple 2017 (`USDOS/LSIB_SIMPLE/2017`) |
| Climate and satellite imagery | WorldClim V1 monthly climate (`WORLDCLIM/V1/MONTHLY`); Landsat 8 Collection 2 Tier 1 TOA (`LANDSAT/LC08/C02/T1_TOA`) |
| Population and night-time lights | GPWv4.11 population count (`CIESIN/GPWv411/GPW_Population_Count`); NOAA DMSP-OLS night-time lights (`NOAA/DMSP-OLS/NIGHTTIME_LIGHTS`) |
| Coral habitat | Allen Coral Atlas reef habitat (`ACA/reef_habitat/v2_0`), with research-station locations defined in the script |
| Deep-ocean ecosystems | NOAA ETOPO1 (`NOAA/NGDC/ETOPO1`); International Seabed Authority exploration-area data, referenced in the script |

The night-time-lights script also uses Earth Engine assets for grids and a coastline, including assets under `users/murrnick/mb5370/` and `projects/UQ_intertidal/`. The deep-ocean script references `projects/coastlines-512607/assets/ISA_PolymetallicNodule_ExplorationAreas`.

The ISA source noted in the script is the [International Seabed Authority DeepData database](https://www.isa.org.jm/deepdata-database/maps/); the script uses an Earth Engine asset rather than importing the source directly.
