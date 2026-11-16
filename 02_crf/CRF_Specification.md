# Case Report Form (CRF) Specification

## Study

A Randomized, Parallel-Group Study Evaluating a Lifestyle Intervention on Glycemic Control in Adults With Type 2 Diabetes

## Purpose

This CRF specification defines the participant-level data fields to be collected at each study visit.

## CRF Modules

### 1. Participant Identification

| Field | Data Type | Required |
|---|---|---|
| Participant ID | Text | Yes |
| Study Site | Categorical | Yes |
| Screening Date | Date | Yes |
| Randomization Date | Date | Yes |
| Treatment Group | Categorical | Yes |

### 2. Demographics

| Field | Data Type | Required |
|---|---|---|
| Date of Birth | Date | Yes |
| Age | Integer | Yes |
| Sex | Categorical | Yes |

### 3. Clinical Measurements

| Field | Data Type | Required |
|---|---|---|
| Weight (kg) | Decimal | Yes |
| Height (cm) | Decimal | Yes |
| BMI (kg/m²) | Decimal | Yes |
| Systolic BP (mmHg) | Integer | Yes |
| Diastolic BP (mmHg) | Integer | Yes |

### 4. Laboratory Measurements

| Field | Data Type | Required |
|---|---|---|
| HbA1c (%) | Decimal | Yes |
| Fasting Blood Glucose (mg/dL) | Integer | Yes |

### 5. Medication

| Field | Data Type | Required |
|---|---|---|
| Medication Name | Text | No |
| Medication Dose | Text | No |
| Medication Changed Since Previous Visit | Yes/No | Yes |

### 6. Adherence

| Field | Data Type | Required |
|---|---|---|
| Intervention Adherence (%) | Integer | Yes |
| Adherence Assessment | Categorical | Yes |

### 7. Adverse Events

| Field | Data Type | Required |
|---|---|---|
| Adverse Event Present | Yes/No | Yes |
| Adverse Event Description | Text | Conditional |
| Severity | Categorical | Conditional |
| Action Taken | Categorical | Conditional |

## Study Visit Schedule

| CRF Module | Week 0 | Week 4 | Week 8 | Week 12 |
|---|---:|---:|---:|---:|
| Participant Identification | ✓ | — | — | — |
| Demographics | ✓ | — | — | — |
| Clinical Measurements | ✓ | ✓ | ✓ | ✓ |
| Laboratory Measurements | ✓ | ✓ | ✓ | ✓ |
| Medication | ✓ | ✓ | ✓ | ✓ |
| Adherence | — | ✓ | ✓ | ✓ |
| Adverse Events | ✓ | ✓ | ✓ | ✓ |

## Data Capture Principles

- Required fields should not be left blank unless a documented reason exists.
- Categorical fields should use predefined values.
- Numeric fields should have predefined acceptable ranges.
- Date fields should follow a consistent format.
- Conditional fields should become applicable only when the triggering response is selected.
- Participant identifiers in this simulated project contain no real patient information.
