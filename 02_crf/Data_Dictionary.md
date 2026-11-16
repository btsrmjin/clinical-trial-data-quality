# Clinical Trial Data Dictionary

## Purpose

This data dictionary defines the database variables corresponding to the CRF fields for the simulated clinical trial.

| Variable Name | Label | Data Type | Required | Allowed Values / Range | Visit |
|---|---|---|---|---|---|
| participant_id | Participant ID | Text | Yes | PT001–PT100 | Baseline |
| site_id | Study Site | Categorical | Yes | SITE01–SITE04 | Baseline |
| screening_date | Screening Date | Date | Yes | YYYY-MM-DD | Baseline |
| randomization_date | Randomization Date | Date | Yes | YYYY-MM-DD | Baseline |
| treatment_group | Treatment Group | Categorical | Yes | Intervention, Control | Baseline |
| dob | Date of Birth | Date | Yes | YYYY-MM-DD | Baseline |
| age | Age | Integer | Yes | 30–65 years | Baseline |
| sex | Sex | Categorical | Yes | Male, Female | Baseline |
| weight_kg | Weight | Decimal | Yes | 35.0–200.0 kg | All visits |
| height_cm | Height | Decimal | Yes | 120.0–220.0 cm | Baseline |
| bmi | Body Mass Index | Decimal | Yes | 15.0–60.0 kg/m² | All visits |
| systolic_bp | Systolic Blood Pressure | Integer | Yes | 70–250 mmHg | All visits |
| diastolic_bp | Diastolic Blood Pressure | Integer | Yes | 40–150 mmHg | All visits |
| hba1c | HbA1c | Decimal | Yes | 4.0–15.0 % | All visits |
| fasting_glucose | Fasting Blood Glucose | Integer | Yes | 50–500 mg/dL | All visits |
| medication_name | Medication Name | Text | No | Free text | All visits |
| medication_dose | Medication Dose | Text | No | Free text | All visits |
| medication_changed | Medication Changed | Categorical | Yes | Yes, No | All visits |
| adherence_pct | Intervention Adherence | Integer | Yes | 0–100 % | Weeks 4, 8, 12 |
| adherence_assessment | Adherence Assessment | Categorical | Yes | Good, Moderate, Poor | Weeks 4, 8, 12 |
| ae_present | Adverse Event Present | Categorical | Yes | Yes, No | All visits |
| ae_description | Adverse Event Description | Text | Conditional | Required if ae_present = Yes | All visits |
| ae_severity | Adverse Event Severity | Categorical | Conditional | Mild, Moderate, Severe | All visits |
| ae_action | Action Taken | Categorical | Conditional | None, Monitoring, Treatment, Discontinued | All visits |

## Data Types

- **Text:** Free-text or identifier field.
- **Integer:** Whole number.
- **Decimal:** Numeric value that may contain decimal places.
- **Date:** Date stored in YYYY-MM-DD format.
- **Categorical:** Value selected from a predefined list.
- **Conditional:** Field becomes required only when the triggering condition is met.

## Key Validation Concepts

### Required Field Check

Required fields should not be blank.

### Range Check

Numeric values must remain within predefined clinically plausible ranges.

### Format Check

Dates and numeric fields must follow the specified data format.

### Logical Check

Values must be logically consistent with other fields.

### Cross-Field Check

Related fields should agree with one another.

### Conditional Check

Conditional fields become required only when the relevant trigger is present.
