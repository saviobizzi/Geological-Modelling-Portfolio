# Alpha Gold Modelling Workflow

## 1. Data Intake

Collect drilling data in structured tables:

- Collar.
- Survey.
- Lithology.
- Assays, when available.
- Topography or reference surfaces, when sanitized.

Original confidential files should stay outside the public repository.

## 2. Data Validation

Run basic validation before modelling:

- Unique hole IDs.
- Valid depth intervals.
- No unintended lithology overlaps.
- Survey consistency.
- Unit consistency.
- Coordinate review.

Document all assumptions and corrections.

## 3. Modelling Preparation

Prepare cleaned datasets for modelling software:

- Standardize column names.
- Create lithology dictionaries.
- Separate raw and processed data.
- Export modelling-ready CSV files.
- Record coordinate and elevation handling.

## 4. Geological Interpretation

Interpret the deposit or target area through:

- Lithological correlation.
- Structural trends.
- Alteration or mineralized domains, when applicable.
- Cross-section review.
- Explicit uncertainty notes.

## 5. 3D Modelling

Build the model using sanitized data and documented assumptions:

- Import collar, survey, and lithology.
- Validate drillhole traces.
- Define domains.
- Create surfaces or solids.
- Review model consistency against sections.

## 6. Portfolio Deliverables

Prepare outputs for a professional audience:

- Short case study summary.
- Key screenshots.
- QA/QC notes.
- Workflow diagram or explanation.
- Final report.

