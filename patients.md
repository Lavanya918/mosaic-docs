# Patients

The **Patients** section provides a centralized view to manage patient records, associated images, and diagnostic information within MOSAIC. Users can view, filter, export, and drill down into individual patient profiles for analysis.

## Patients List Page

### Overview

The Patients list displays all patients associated with the user’s workspace.

**Key elements:**
- Total number of patients
- Search and filter options
- Export capabilities
- Actions to view or manage individual patients

### Page Header

| Element | Description |
|------|------------|
| Patients | Page title |
| Total Patients | Displays total patient count |
| Add Patients | Button to add a new patient record |
| Export All Data | Exports the complete patient dataset |
| Export Filtered Data | Exports only filtered results |

### Patients Table

Each row represents a patient record.

| Column | Description |
|------|------------|
| Case ID | Unique system-generated patient identifier |
| Total Images | Number of images uploaded for the patient |
| Diagnosis | Diagnosis summary (if available) |
| Organ | Organ associated with diagnosis |
| Age at Index | Patient age at diagnosis/index |
| Vital Status | Patient vital status |
| Actions | View, edit, add images, or additional actions |

**Table Features:**
- Column-wise filtering
- Sorting
- Pagination
- Grid and list view toggle

## Patient Detail Page

Selecting a **Case ID** opens the detailed patient profile.

### Page Header

| Element | Description |
|------|------------|
| Case ID | Unique patient identifier |
| View Info | View patient metadata |
| Analyze | Run analysis on uploaded images |
| Edit | Edit patient details |
| Delete | Delete patient record |

## Patient Information Tabs

### 1. Basic Information

Displays core patient demographics and specimen-related metrics.

| Field | Description |
|----|------------|
| Age at Index | Age at diagnosis |
| Year of Birth | Patient year of birth |
| Sex | Patient sex |
| Ethnicity | Ethnicity (if provided) |
| Vital Status | Alive / Deceased / Unknown |
| Year of Death | If applicable |
| Height | Patient height |
| Weight | Patient weight |
| Number of Blocks | Total specimen blocks |
| Number of IHC Blocks | IHC-specific blocks |
| Number of H&E Blocks | H&E-specific blocks |
| Notes | Additional notes |


### 2. Diagnosis Information

Clinical and pathological diagnosis details.

| Field | Description |
|----|------------|
| Diagnosis ID (ICD-11) | ICD-11 diagnosis code |
| Diagnosis Name | Diagnosis description |
| Organ | Affected organ |
| Month of Diagnosis | Diagnosis month |
| Clinical Stage | Cancer stage |
| Grade | Tumor grade |
| Morphology | Tumor morphology |
| Specimen | Specimen description |
| Grossing Examination | Gross pathology notes |
| Microscopic Examination | Microscopic findings |
| AI Assisted Interpretation | AI-derived interpretation (if available) |

### 3. Additional Information

Reserved for future extensions such as:
- Molecular findings
- Genetic information
- Research annotations
- Custom metadata

## Images & Reports Section

Located below patient details.

### Images Tab

Displays all uploaded images for the patient.

**Actions available:**
- Add Image
- Run Test (enabled when images are present)
- Export image metadata

**Image Table Columns:**
- Image Name
- Magnification
- Cloud Status
- Width
- Height
- Modality
- Preparation
- Actions (view, delete, etc.)

If no images are uploaded, the system displays:
> _No records to show_

### Reports Tab

Displays generated reports related to MOSAIC analysis.

## Permissions & Privacy Notes

- Patient identifiers shown in documentation use **safe placeholders**
- Personally identifiable information (PII) should not be exposed in public documentation
- Access to edit, analyze, or delete records depends on user role

## Related Pages

- Home Dashboard
- Orders
- Order Details
- Image Upload & Analysis

