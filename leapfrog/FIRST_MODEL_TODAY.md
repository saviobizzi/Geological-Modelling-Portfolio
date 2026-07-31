# First Model Today - Alpha Gold

This guide is intentionally practical. The goal is to build the first geological model in Leapfrog Geo from the synthetic Alpha Gold dataset, validate the workflow, and export the first figures for the portfolio.

## Target outcome

By the end of this run, the project should have:

- Drillholes imported and visually checked.
- Lithology intervals displayed by category.
- A first implicit model of the main lithological domains.
- A first mineralized vein/domain interpretation using the `QV` code and Au support.
- At least two screenshots exported to `outputs/figures/`.

## Input files

Use the CSV files in:

`data/synthetic/`

| File | Purpose | Leapfrog import role |
| --- | --- | --- |
| `collar.csv` | Hole coordinates, elevation, and final depth | Collar |
| `survey.csv` | Downhole azimuth and dip stations | Survey |
| `lithology.csv` | Geological intervals | Interval table |
| `assays.csv` | Synthetic Au ppm intervals | Numeric interval table |

## Import mapping

### Collar

| CSV column | Leapfrog field |
| --- | --- |
| `hole_id` | Hole ID |
| `easting` | X |
| `northing` | Y |
| `elevation` | Z |
| `total_depth` | Max depth / hole depth |

### Survey

| CSV column | Leapfrog field |
| --- | --- |
| `hole_id` | Hole ID |
| `depth` | Depth |
| `azimuth` | Azimuth |
| `dip` | Dip |

### Lithology

| CSV column | Leapfrog field |
| --- | --- |
| `hole_id` | Hole ID |
| `from_m` | From |
| `to_m` | To |
| `lithology_code` | Category |
| `lithology_name` | Description |

### Assays

| CSV column | Leapfrog field |
| --- | --- |
| `hole_id` | Hole ID |
| `from_m` | From |
| `to_m` | To |
| `au_ppm` | Au ppm |

## Recommended coordinate system

For this synthetic dataset, keep the coordinate system as a local grid.

Do not assign a real UTM zone unless the project later uses real sanitized coordinates.

## Build sequence

1. Create a new Leapfrog Geo project named `Alpha_Gold_Portfolio_Model`.
2. Import `collar.csv` as the drillhole collar table.
3. Import `survey.csv` as the survey table.
4. Import `lithology.csv` as the lithology interval table.
5. Import `assays.csv` as the assay interval table.
6. Open the 3D scene and confirm all four holes appear.
7. Color lithology by `lithology_code`.
8. Check that the hole traces dip generally eastward/southeastward.
9. Build a first geological model using `SOIL`, `SCH`, `QV`, and `GN`.
10. Treat `QV` as the first mineralized structural/vein domain.
11. Display `au_ppm` intervals and verify that higher values coincide with `QV`.
12. Export screenshots for:
    - drillhole database validation;
    - first lithological model;
    - QV/Au interpretation.

## Interpretation rules for version 0.1

Keep the first model simple:

- `SOIL`: shallow residual cover.
- `SCH`: weathered schist / altered host package.
- `GN`: fresh gneissic basement / lower host unit.
- `QV`: quartz vein domain, used as the initial mineralized target.

Do not overfit the geometry. Four holes are enough for a portfolio workflow demonstration, not for a defensible resource model.

## First screenshots to export

Export PNGs to `outputs/figures/` using these names:

- `alpha_gold_drillholes_lithology_v0_1.png`
- `alpha_gold_qv_domain_v0_1.png`
- `alpha_gold_au_intervals_v0_1.png`

## Notes for the portfolio README

After the first model is built, add a short note describing:

- what was modeled;
- which data were used;
- what assumptions were made;
- what remains uncertain;
- what should be improved in the next version.
