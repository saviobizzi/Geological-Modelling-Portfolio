# Geological Data QA/QC Checklist

Use this checklist before importing data into Leapfrog, QGIS, notebooks, or final reports.

## Collar

- Hole IDs are unique.
- Easting, northing, and elevation fields are present.
- Coordinates use a documented coordinate system or are intentionally anonymized.
- Total depth is numeric and greater than zero.
- Collar table contains no duplicate records.

## Survey

- Every surveyed hole exists in the collar table.
- Depth values are numeric and ordered.
- Survey depth does not exceed collar total depth.
- Azimuth values are within 0 to 360 degrees.
- Dip values are within -90 to +90 degrees.
- Missing survey intervals are documented.

## Lithology

- Every logged hole exists in the collar table.
- From and To intervals are numeric.
- `From` is always smaller than `To`.
- Intervals do not overlap unless the overlap is intentional and documented.
- Logged depth does not exceed collar total depth.
- Lithology codes are consistent and explained in a legend.

## Assays

- Every assay interval belongs to a valid hole.
- From and To intervals are numeric.
- Sample intervals do not overlap unexpectedly.
- Missing or below-detection values are coded consistently.
- Units are documented.
- Outliers are reviewed before modelling or reporting.

## Interpretation

- Modelling assumptions are written down.
- Geological domains have short definitions.
- Areas of uncertainty are described.
- Any manual corrections are traceable.
- Screenshots are reviewed for sensitive labels before publication.

