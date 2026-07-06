# Data Folder

This folder contains the compact data artifacts used by the Australian winter-crop early-warning project.

## Structure

```text
data/
  processed/
```

Raw source tables are not included in this double-blind review snapshot. The processed panels below contain the feature matrices and metadata needed for the reviewer reproduction checks.

## Processed Data

- `processed/weather_stage_features.csv`: May-Jun to May-Oct weather-stage features by `region`, `year_start`, and `forecast_window`.
- `processed/soil_selected_features.csv`: selected regional soil background features.
- `processed/model_ready_panel.csv`: initial modeling panel.
- `processed/model_ready_panel_improved.csv`: main improved modeling panel used by the ACML manuscript.

The main analysis unit is:

```text
region + crop + year_start + forecast_window
```

The improved panel has 4,830 forecast-window rows from 966 unique region-crop-year yield observations. `production_kt` and `area_000ha` are retained only as metadata and are excluded from the training feature matrices and manuscript evidence.
