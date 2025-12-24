# Sperchios Gulf Water Pollution Dataset (Sentinel-2)

This dataset contains per-tile water quality products derived from Sentinel-2 imagery for the Sperchios Gulf. Tiles are numbered from tile_00 through tile_09 and include CSV metrics, per-date JSON collections, and PNG image layers. All tiles correspond to spatial subdivisions of the Sperchios River Gulf.

## Overview

The Sperchios Gulf Water Pollution Dataset provides spatially and temporally resolved water-quality indicators derived from Sentinel-2 imagery. The dataset is designed to support river-to-coastal water pollution monitoring, spatio-temporal analysis, and machine-learning-based forecasting of environmental parameters.

## Area of Interest

The dataset covers the Sperchios River Gulf, Greece, including the river delta and adjacent coastal waters. The area is subdivided into ten spatial tiles (tile_00 to tile_09) to enable localized analysis of water-quality dynamics.
Bounding Box:
- [22.51901286489857, 38.86448942189875, 22.562631861867928, 38.8758260508686]

## Data Products

The dataset includes the following water-quality products derived from Sentinel-2:

- Chlorophyll-a concentration
- Turbidity
- Colored Dissolved Organic Matter (CDOM)
- Cyanobacteria density, 
- Dissolved Organic Carbon (DOC)
- Water color 

Each product is provided as:
- Time-series CSV metrics
- Image visualizations (PNG)
- Raw Sentinel-2 feature collections (JSON)

## Preprocessing

Raw Sentinel-2 observations were preprocessed to:
- Remove invalid or missing acquisitions
- Aggregate per-tile statistics
- Interpolate missing dates to achieve a daily temporal resolution

The files `*_interpolated_time_based.csv.preprocessed` contain the final processed time-series recommended for machine learning applications.

## Structure

- tile_00..tile_09/
  - csv/ : CSV summaries and preprocessed time-based metrics contains processed CSV files:
    - 1D_mean_metrics_interpolated_time_based.csv.preprocessed
    - 1D_mean_metrics_interpolated_time_based.csv
    - max_metrics.csv
    - min_metrics.csv
    - mean_metrics.csv
  - images/ : PNG layers for water-quality products per tile
  - raw_s2_collections/ : per-date JSON collections (raw from Copernicus Dataspace Ecosystem)
  - tiles_info.json : per-tile metadata (tile and acquisition info)

## Global Metadata

- global_metadata.json provides dataset-wide metadata

## Recommended Usage

For machine learning and time-series modeling, we recommend using:

- `1D_mean_metrics_interpolated_time_based.csv.preprocessed`

These files provide consistent temporal sampling and reduced noise, suitable for forecasting and anomaly detection tasks.

## License

This dataset is licensed under the **Creative Commons Attribution 4.0 International (CC-BY 4.0)** license.

You are free to:
- Share — copy and redistribute the material in any medium or format  
- Adapt — remix, transform, and build upon the material  

for any purpose, even commercially, **provided that appropriate credit is given**.

Full license text: https://creativecommons.org/licenses/by/4.0/

