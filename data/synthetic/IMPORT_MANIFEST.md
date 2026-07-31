# Synthetic Import Manifest - Alpha Gold

This folder contains a small synthetic drillhole dataset prepared for the first Alpha Gold portfolio model.

The dataset is not real project data. It is designed to demonstrate geological modelling workflow, data governance, QA/QC thinking, and Leapfrog import structure without exposing confidential information.

## Files

| File | Records | Description |
| --- | ---: | --- |
| `collar.csv` | 4 holes | Synthetic collar coordinates and total depths |
| `survey.csv` | 12 stations | Downhole azimuth and dip stations |
| `lithology.csv` | 14 intervals | Simplified lithological logging |
| `assays.csv` | 11 intervals | Synthetic Au ppm values |

## Domain codes

| Code | Domain | Modelling use |
| --- | --- | --- |
| `SOIL` | Residual soil | Weathering cover |
| `SCH` | Weathered schist | Altered/weathered host package |
| `QV` | Quartz vein domain | Initial mineralized target domain |
| `GN` | Fresh gneiss | Fresh host/basement domain |

## Quick QA/QC checklist

Before modelling:

- Confirm all `hole_id` values in interval tables exist in `collar.csv`.
- Confirm `from_m` is always smaller than `to_m`.
- Confirm no lithology intervals overlap within the same hole.
- Confirm lithology intervals do not exceed `total_depth`.
- Confirm survey depths do not exceed `total_depth`.
- Confirm Au values are numeric.

## Modelling intent

The first model should show:

- a shallow residual cover;
- a weathered schist package;
- a fresh gneissic host;
- a quartz vein/mineralized domain supported by Au intervals.

This is a workflow model, not a resource estimate.
