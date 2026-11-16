# Edit Check Specification

## Purpose

This document defines automated and manual edit checks for the synthetic clinical trial dataset.

## Edit Checks

| Check ID | Check | Logic | Expected Action |
|---|---|---|---|
| EC001 | Participant ID format | participant_id must match PT001–PT100 | Raise query |
| EC002 | Site validity | site_id must be SITE01–SITE04 | Raise query |
| EC003 | Treatment validity | treatment_group must be Intervention or Control | Raise query |
| EC004 | Age range | Age must be 30–65 years | Raise query |
| EC005 | Weight range | Weight must be 35–200 kg | Raise query |
| EC006 | Height range | Height must be 120–220 cm | Raise query |
| EC007 | BMI range | BMI must be 15–60 kg/m² | Raise query |
| EC008 | SBP range | Systolic BP must be 70–250 mmHg | Raise query |
| EC009 | DBP range | Diastolic BP must be 40–150 mmHg | Raise query |
| EC010 | HbA1c range | HbA1c must be 4.0–15.0% | Raise query |
| EC011 | Glucose range | Fasting glucose must be 50–500 mg/dL | Raise query |
| EC012 | Adherence range | Adherence must be 0–100% | Raise query |
| EC013 | AE consistency | If ae_present = No, AE description/severity/action should be blank | Raise query |
| EC014 | AE consistency | If ae_present = Yes, AE description and severity should be populated | Raise query |
| EC015 | Medication consistency | medication_changed = Yes requires medication information | Raise query |
| EC016 | Date sequence | Randomization date must not precede screening date | Raise query |
| EC017 | BMI calculation | BMI should be consistent with weight and height | Raise query |
| EC018 | Age consistency | Age should be consistent with DOB and study date | Raise query |

## Query Handling

Any failed edit check should be:

1. Logged in the Query Log.
2. Reviewed for validity.
3. Assigned a query status.
4. Corrected or clarified where appropriate.
5. Rechecked after resolution.
6. Closed only after verification.

## Final Data Quality Principle

The final analysis dataset should contain only verified and appropriately resolved records.
