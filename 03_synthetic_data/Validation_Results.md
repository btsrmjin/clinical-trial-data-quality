# Data Validation Results

## Dataset

- Dataset: Clinical Trial Synthetic Dataset
- Participants: 100
- Study type: Simulated randomized parallel-group trial
- Data source: Synthetic / educational data
- PHI: None

## Validation Checks Performed

| Check ID | Check Type | Description | Expected Result |
|---|---|---|---|
| DQ001 | Completeness | Check required participant IDs | Pass |
| DQ002 | Completeness | Check treatment group completeness | Pass |
| DQ003 | Range | Age within 30–65 years | Pass |
| DQ004 | Range | Weight within 35–200 kg | Pass |
| DQ005 | Range | Height within 120–220 cm | Pass |
| DQ006 | Range | BMI within 15–60 kg/m² | Pass |
| DQ007 | Range | HbA1c within 4.0–15.0% | Pass |
| DQ008 | Range | Fasting glucose within 50–500 mg/dL | Pass |
| DQ009 | Range | Adherence within 0–100% | Pass |
| DQ010 | Format | Participant IDs follow PT001–PT100 format | Pass |
| DQ011 | Format | Dates follow YYYY-MM-DD | Pass |
| DQ012 | Logical | AE fields consistent with AE presence | Review |
| DQ013 | Logical | Medication change fields internally consistent | Review |
| DQ014 | Cross-field | BMI consistency with height and weight | Review |
| DQ015 | Cross-field | Age consistency with date of birth | Review |

## Validation Status

The dataset contains intentionally varied records for demonstration of clinical data validation and query-management workflows.

Checks marked **Review** require detailed record-level assessment before the dataset can be considered fully clean.

## Next Step

Potential data issues identified during validation will be documented in the query log and tracked through resolution.
