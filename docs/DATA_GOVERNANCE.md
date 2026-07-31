# Data Governance

## Public Repository Rule

Only sanitized or synthetic data should be committed to this public repository.

If a file cannot be shared with a future employer, client, professor, or recruiter without legal or professional concern, it should not be committed here.

## Data Classes

| Class | Description | Public Repository |
| --- | --- | --- |
| Raw confidential data | Original drilling logs, client data, coordinates, contracts, internal files | Do not commit |
| Sanitized data | Anonymized and reviewed data with sensitive details removed | Allowed after review |
| Synthetic data | Fictional data created for demonstration | Allowed |
| Derived figures | Screenshots, maps, sections, and charts based on sanitized data | Allowed after review |
| Final reports | Portfolio-ready explanations and case study summaries | Allowed after review |

## Sanitization Checklist

- Remove real client, mine, company, and person names.
- Remove or shift coordinates.
- Remove internal document identifiers.
- Replace original hole names if they identify a project.
- Review screenshots for map labels, coordinates, file paths, and project names.
- Replace confidential assay values with synthetic or normalized examples.
- Keep a private note of what was changed, but do not publish that note if it reveals sensitive information.

## Recommended Naming

Use portfolio-safe names such as:

- `Alpha Gold`
- `AG-DDH-001`
- `AG-DDH-002`
- `Synthetic Lithology`
- `Interpreted Domain A`

