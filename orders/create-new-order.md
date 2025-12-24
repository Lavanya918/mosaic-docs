# Create New Order

The **Create New Order** page allows users to initiate a new order request for MOSAIC analysis. The workflow is designed as a guided, multi-step process to ensure that all required professional, patient, sample, and shipping details are captured accurately before submission.

## Navigation

Users can access the **Create New Order** page through either of the following paths:

* **Home Dashboard → Create New Order**
* **Sidebar → Orders → Create New Order**

## Order Creation Workflow

The order creation process is divided into a series of steps displayed in a stepper on the left side of the screen.

### Steps Overview

1. **Order Details**
2. **Patient Information**
3. **Ordering Physician**
4. **Sample Information**
5. **Shipping Address**
6. **Review & Submit**

### General Behavior

* The current step is highlighted in the stepper.
* Users must complete each step to proceed to the next.
* Required fields are marked with an asterisk (`*`).
* Navigation between steps is linear.

## Step 1: Order Details & Purpose of Test

This step captures the professional and institutional information of the user placing the order.

### Description

The details entered in this section help identify the ordering professional and their affiliated institution. Some fields may be auto-filled based on the user profile.

### Fields

| Field Name                     | Description                                                         | Required |
| ------------------------------ | ------------------------------------------------------------------- | -------- |
| Role / Profession              | Select the professional role of the user (e.g., Pathologist)        | Yes      |
| Title                          | Professional title                                                  | No       |
| First Name                     | First name of the user placing the order                            | Yes      |
| Last Name                      | Last name of the user placing the order                             | Yes      |
| Institution / Hospital Name    | Name of the affiliated institution or hospital                      | Yes      |
| Institution / Hospital Address | Full address of the institution or hospital                         | Yes      |
| Medical Registration Number    | Official medical registration or license number                     | No       |
| Work Email                     | Official work email address                                         | Yes      |
| Work Phone Number              | Primary contact phone number for the ordering professional          | Yes      |
| Work Landline Number           | Landline contact number, if available                               | No       |
| Purpose of Test                | Brief description of the purpose for the order                      | Yes      |

### Actions

* **Next**: Saves the entered information and proceeds to **Patient Information**.
* **Back**: Returns to the previous step (disabled on the first step).

### Validation Rules

* All required fields must be completed to continue.
* Email addresses must follow a valid email format.
* Users cannot proceed if mandatory information is missing.

## Step 2: Patient Information

This step captures patient-specific demographic and contact information required for analysis and accurate record association.

### Description

The Patient Information step ensures that the order is correctly linked to the intended patient. All required fields must be completed before proceeding to the next step.

### Fields

| Field Name | Description | Required |
|----------|-------------|----------|
| First Name | Patient’s first name | Yes |
| Last Name | Patient’s last name | Yes |
| MRN Number | Medical Record Number for internal hospital reference | No |
| Date of Birth | Patient’s date of birth (dd-mm-yyyy format) | Yes |
| Age | Patient’s age at the time of order | Yes |
| Sex | Patient’s biological sex | Yes |
| Email Address | Patient’s email address | No |
| Phone Number | Primary contact phone number for the patient | Yes |
| Address | Patient’s residential address | No |
| Postal Code | Postal or ZIP code | No |
| State | State or province | No |
| Country | Country of residence | No |

### Actions

- **Save as Draft**  
  Saves the entered patient information without progressing to the next step.

- **Next**  
  Proceeds to the **Ordering Physician** step once all required fields are completed.

- **Back**  
  Returns to the previous step (**Order Details**).

### Validation Rules

- All required fields must be completed to proceed.
- Date of Birth must follow the `dd-mm-yyyy` format.
- Phone number must contain valid numeric characters.

## Step 3: Ordering Physician / Referral Details

This step captures referral information related to the physician who recommended to order for the MOSAIC clinical test.

### Description

The Ordering Physician step records whether the test was recommended by a qualified physician and captures relevant physician contact and clinic details. This information helps ensure appropriate clinical oversight.

### Physician Recommendation

**Has your physician recommended this test?***  

- **Yes**
- **No**

This selection controls the display of additional guidance and messaging on the screen.

### Warning Message (When “No” Is Selected)

If **No** is selected, the following warning message is displayed:

> ⚠️ **We strongly advise consulting a qualified physician before ordering this test.**

The user can still proceed with the order after acknowledging this advisory message.

### Fields

| Field Name | Description | Required |
|-----------|-------------|----------|
| Physician’s Full Name | Full name of the referring or associated physician | No |
| Physician’s Clinic / Hospital Name | Name of the physician’s clinic or hospital | No |
| Physician’s Clinic / Hospital Address | Address of the clinic or hospital | No |
| Physician’s Email | Professional email address of the physician | No |
| Physician’s Phone Number | Contact phone number of the physician (7–15 digits) | No |

### Actions

- **Save as Draft**  
  Saves the entered physician details without progressing to the next step.

- **Next**  
  Proceeds to the **Sample Information** step.

- **Back**  
  Returns to the **Patient Information** step.

### Validation Rules

- The physician recommendation question is mandatory.
- Email address must be in a valid format if provided.
- Phone number must contain only digits and be between 7 and 15 characters.


## Step 4: Sample / Specimen Information

This step captures detailed information about the biological sample or specimen submitted for spatial analysis, including pathology details, specimen characteristics, slide counts, and optional IHC and digital slide availability.

---

## Sample Details

### Description

The Sample / Specimen Information step records clinical and laboratory details required for accurate processing and analysis. Certain fields and messages are displayed conditionally based on user selections (e.g., IHC staining or digital whole slide image availability).

---

### Fields

| Field Name | Description | Required |
|-----------|-------------|----------|
| Date of Sample Collection | Date when the sample was collected (dd-mm-yyyy format) | Yes |
| Histopathology Slide Reference Number | Internal or laboratory reference number for the slide | No |
| Cancer Type | Type of cancer associated with the sample | Yes |
| Specimen Type | Method by which the tissue specimen was obtained | Yes |
| Sample Type | Physical format of the sample provided | Yes |
| Total number of slides / blocks | Total number of submitted slides or blocks | No |
| Total number of H&E slides | Number of Hematoxylin & Eosin stained slides | No |
| Total number of IHC slides | Number of Immunohistochemistry slides | No |

---

## Supported Cancer Types

MOSAIC currently supports analysis for the following cancer types:

- Breast Cancer

> This list may expand as additional cancer types are validated and supported.

---

## Specimen Types

The following **specimen collection methods** are supported:

- **Core Needle Biopsy**  
  Tissue obtained using a hollow needle, commonly used for minimally invasive diagnosis.

- **Incisional Biopsy**  
  Partial removal of tissue from a lesion or mass for diagnostic purposes.

- **Excisional Biopsy**  
  Complete removal of the lesion or mass for comprehensive pathological evaluation.

> The selected specimen type should accurately reflect the clinical procedure used to obtain the tissue.

---

## Sample Types

MOSAIC currently supports the following **sample formats**:

- **FFPE Tissue Blocks**
- **FFPE Tissue Slides**

> Samples must meet platform-defined quality and preparation requirements for successful analysis.

---

## IHC Staining Requirement

**Do you require IHC staining to be performed?**

- **Yes**
- **No**

This selection determines whether additional IHC-specific details are required.

---

## IHC Staining Details (When IHC = Yes)

If **Yes** is selected for IHC staining, the following fields and validations apply.

### Required IHC Markers

Users must select **at least one** Immunohistochemistry (IHC) marker:

- **ER** (Estrogen Receptor)
- **PR** (Progesterone Receptor)
- **HER2**
- **Ki67**

> ⚠️ **Validation:** At least one IHC marker must be selected to proceed.

### Related Fields

| Field Name | Description | Required |
|-----------|-------------|----------|
| Total number of IHC slides | Number of IHC slides required | No |
| Required IHC markers | Selected biomarkers for IHC staining | Yes |

---

## Digital Whole Slide Image (WSI)

**Do you have a digital whole slide image for analysis?**

- **Yes**
- **No**

---

## Additional Information (When WSI = Yes)

If **Yes** is selected for digital whole slide image availability, the following informational message is displayed:

> ℹ️ **Accepted formats:** SVS, NDPI, MRXS, TIFF  
> You will receive a secure upload link after submitting the order.

Digital slide files are uploaded securely after order submission.

---

## Actions

- **Save as Draft**  
  Saves the entered sample information without progressing to the next step.

- **Next**  
  Proceeds to the **Shipping Address** step once required fields are completed.

- **Back**  
  Returns to the **Ordering Physician** step.

## Validation Rules

- All required fields must be completed to proceed.
- Date fields must follow the `dd-mm-yyyy` format.
- Slide count fields must contain valid numeric values.
- When IHC staining is required, at least one IHC marker must be selected.


## Step 5: Shipping Address – Pickup & Return

This step captures pickup and return address details for shipping pathology samples, including sender information, contact details, and return logistics.

## Sample Pickup Address

### Description

The Sample Pickup Address section records where the sample will be collected from, typically a pathologist or laboratory.

### Fields

**Will the sample be sent from a Pathologist / Lab?***  

- **Yes**
- **No**

| Field Name | Description | Required |
|-----------|-------------|----------|
| Name of the Sender (Pathologist / Lab) | Name of the pathologist, laboratory, or sending entity | Yes |
| Contact Person (Name & Phone / Email) | Primary contact for sample pickup coordination | Yes |
| Complete Address of the Sender (Pathologist / Lab) | Full pickup address including street and location details | Yes |


## Sample Return Address

### Description

This section captures the address where samples should be returned after analysis.

### Pickup and Return Address Matching

**Is the pickup and return address the same?***  

- **Yes**
- **No**

- If **Yes** is selected, the pickup address is used as the return address.
- If **No** is selected, additional return address fields are displayed.


### Return Address Fields (When Pickup ≠ Return)

| Field Name | Description | Required |
|-----------|-------------|----------|
| Complete Return Address | Full address where samples should be returned | Yes |
| Postal Code | Postal or ZIP code | Yes |
| State | State or province | Yes |
| Country | Country | Yes |


## Packing Guidelines

The following advisory message is displayed to the user:

> ℹ️ **Please review our slide & block packing guidelines before shipping.**

This ensures samples are packed safely and according to platform requirements.

## Actions

- **Save as Draft**  
  Saves the entered shipping details without progressing to the next step.

- **Next**  
  Proceeds to the **Review & Submit** step once all required fields are completed.

- **Back**  
  Returns to the **Sample Information** step.

## Validation Rules

- All required fields must be completed to proceed.
- Sender and return addresses must be complete and valid.
- Return address fields are mandatory when pickup and return addresses are different.


## Step 6: Review & Submit

This final step allows users to review all previously entered information before submitting the order.

### Description

Users should verify the accuracy of order, patient, physician, sample, and shipping details.

### Actions

* **Submit Order**: Finalizes and submits the order for processing.
* **Back**: Returns to previous steps to make corrections.

Once submitted, the order appears in **View All Orders** and enters the processing workflow.

## Notes & Best Practices

* Verify all information carefully before submission.
* Some order details may not be editable after submission.
* Incomplete orders cannot be submitted.


## Related Documentation

* Home Dashboard
* View All Orders
* Order Details & Results
