# Sperchios Gulf Water Pollution Dataset (Sentinel-2)

This dataset contains per-tile water quality products derived from Sentinel-2 imagery for the Sperchios Gulf. Tiles are numbered from tile_00 through tile_09 and include CSV metrics, per-date JSON collections, and PNG image layers.

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

## Notes
For usage in Machine Learning models we suggest using the CSV processed files.

## Paper
To be published

