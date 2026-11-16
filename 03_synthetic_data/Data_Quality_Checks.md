# Data Quality Checks

## Purpose

This document defines the data quality checks applied to the synthetic clinical trial dataset.

## 1. Completeness Checks

Identify missing values in required variables.

Examples:
- Participant ID missing
- Treatment group missing
- Visit-related dates missing
- HbA1c missing
- Fasting glucose missing

## 2. Range Checks

Identify values outside predefined clinical or data-entry ranges.

Examples:
- Age: 30–65 years
- Weight: 35–200 kg
- Height: 120–220 cm
- BMI: 15–60 kg/m²
- Systolic BP: 70–250 mmHg
- Diastolic BP: 40–150 mmHg
- HbA1c: 4.0–15.0%
- Fasting glucose: 50–500 mg/dL
- Adherence: 0–100%

## 3. Format Checks

Verify that variables follow the expected format.

Examples:
- Participant ID follows PT001–PT100 format
- Site ID follows SITE01–SITE04 format
- Dates follow YYYY-MM-DD
- Treatment group is Intervention or Control
- Sex is Male or Female

## 4. Logical Consistency Checks

Identify combinations of values that are logically inconsistent.

Examples:
- Adverse event marked "No" but adverse-event details are populated
- Medication changed = "Yes" but medication information is missing
- Adherence assessment does not match adherence percentage
- Randomization date occurs before screening date

## 5. Cross-Field Checks

Compare related variables.

Examples:
- BMI should be consistent with weight and height
- Age should be consistent with date of birth and study dates
- Adverse-event fields should be populated only when AE is present

## 6. Query Management

Each identified data issue should be documented using:

- Query ID
- Participant ID
- Variable
- Issue identified
- Query description
- Resolution
- Status

Query status values:

- Open
- Resolved
- Closed

## 7. Data Cleaning

After queries are resolved:

1. Re-run all validation checks.
2. Confirm that previously identified errors are corrected.
3. Verify that no new inconsistencies were introduced.
4. Document the final clean dataset.
