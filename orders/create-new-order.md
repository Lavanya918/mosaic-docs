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

## Sample Details

### Description

The Sample / Specimen Information step records clinical and laboratory details required for accurate processing and analysis. Certain fields and messages are displayed conditionally based on user selections (e.g., IHC staining or digital whole slide image availability).

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


## Supported Cancer Types

MOSAIC currently supports analysis for the following cancer types:

- Invasive ductal carcinoma
- Invasive lobular carcinoma
- Invasive mucinous carcinoma
- Inflammatory breast cancer
- Others - specify

## Specimen Types

The following **specimen collection methods** are supported:

- Core Needle Biopsy
- Incisional Biopsy 
- Excisional Biopsy
- Cell block
- Others - specify

## Sample Types

MOSAIC currently supports the following **sample formats**:

- **FFPE Tissue Blocks**
- **FFPE Tissue Slides**

> Samples must meet platform-defined quality and preparation requirements for successful analysis.


## IHC Staining Requirement

**Do you require IHC staining to be performed?**

- **Yes**
- **No**

This selection determines whether additional IHC-specific details are required.

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

## Digital Whole Slide Image (WSI)

**Do you have a digital whole slide image for analysis?**

- **Yes**
- **No**

## Additional Information (When WSI = Yes)

If **Yes** is selected for digital whole slide image availability, the following informational message is displayed:

> ℹ️ **Accepted formats:** SVS, NDPI, MRXS, TIFF  
> You will receive a secure upload link after submitting the order.

Digital slide files are uploaded securely after order submission.

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

The Review & Submit step presents a consolidated, read-only summary of all information entered during the order creation process. Users should carefully review all details before submitting the order.

> ⚠️ **Privacy Notice:**  
> All examples shown below use placeholder data. No real patient or user information is displayed.

## Order Details

This section summarizes information about the ordering professional and the purpose of the test.

| Field | Value |
|------|------|
| Role | <User Role> |
| Title | <Professional Title> |
| First Name | <First Name> |
| Last Name | <Last Name> |
| Institution | <Institution Name> |
| Institution Address | <Institution Address> |
| Medical Registration Number | <Registration Number> |
| Work Email | <Work Email Address> |
| Work Phone | <Work Phone Number> |
| Work Landline | <Work Landline Number> |
| Purpose of Test | <Purpose Description> |
| Shipping ID | <System Generated ID> |

## Patient Information

This section displays patient demographic and contact information.

| Field | Value |
|------|------|
| First Name | <Patient First Name> |
| Last Name | <Patient Last Name> |
| MRN | <Medical Record Number> |
| Date of Birth | <DD-MM-YYYY> |
| Age | <Patient Age> |
| Gender | <Gender> |
| Email | <Patient Email Address> |
| Phone | <Patient Phone Number> |
| Address | <Patient Address> |
| Postal Code | <Postal Code> |
| State | <State> |
| Country | <Country> |

## Ordering Physician

This section summarizes referral details for the ordering physician.

| Field | Value |
|------|------|
| Physician Recommended Test | <Yes / No> |
| Physician Name | <Physician Full Name> |
| Clinic / Hospital Name | <Clinic or Hospital Name> |
| Clinic / Hospital Address | <Clinic Address> |
| Email | <Physician Email Address> |
| Phone | <Physician Phone Number> |


## Sample / Specimen

This section summarizes all pathology and specimen-related information.

| Field | Value |
|------|------|
| Require IHC | <Yes / No> |
| Has Digital WSI | <Yes / No> |
| Date of Sample Collection | <DD-MM-YYYY> |
| Histopathology Slide Reference | <Reference Number> |
| Total Slides / Blocks | <Numeric Value> |
| Total H&E Slides | <Numeric Value> |
| Total IHC Slides | <Numeric Value> |
| Cancer Type | <Selected Cancer Type> |
| Cancer Type (Other) | <If Applicable> |
| Specimen Type | <Specimen Type> |
| Specimen Type (Other) | <If Applicable> |
| Sample Type | <FFPE Block / FFPE Slide> |
| IHC Markers | <Selected IHC Markers> |

## Shipping

This section summarizes pickup and return logistics.

| Field | Value |
|------|------|
| Sent From Lab | <Yes / No> |
| Same Return Address | <Yes / No> |
| Sender / Lab Name | <Sender Name> |
| Pickup Address | <Pickup Address> |
| Contact Person | <Contact Name & Details> |
| Return Address | <Return Address> |
| Postal Code | <Postal Code> |
| State | <State> |
| Country | <Country> |

## Actions

- **Save as Draft**  
  Saves the order without final submission.

- **Back**  
  Returns to the **Shipping Address** step for edits.

- **Submit**  
  Submits the order for processing.

> ⚠️ Once submitted, the order cannot be edited.


## Validation

- All required steps must be completed before submission.
- Users must verify the accuracy of all information before submitting the order.
- Submission confirms that the provided information is complete and correct.

## Terms, Privacy & Declaration (Post-Submit Confirmation)

When the user clicks **Submit** on the **Review & Submit** page, a modal dialog is displayed requiring explicit agreement to the Terms & Conditions, Privacy Policy, and Declaration before the order can be submitted.

## Modal Overview

**Title:**  
Terms, Privacy & Declaration

**Description:**  
Users are prompted to carefully review the Terms & Conditions, Privacy Policy, and Declaration applicable to the MOSAIC clinical test service before completing the order submission.

## Terms and Conditions

The modal displays legal and regulatory information governing the use of the MOSAIC (Mammary Oncology Spatial Analysis and Intelligent Classification) service, including:

### Key Sections

1. **Nature of the MOSAIC Service**
   - AI-driven clinical decision support for breast cancer histopathology analysis
   - Analysis of digitized histopathology slides
   - Generation of AI-derived insights to assist pathologists

2. **Augmentative Tool Disclaimer**
   - MOSAIC is intended to **support**, not replace, clinical judgment
   - Results must be interpreted alongside comprehensive clinical evaluation

3. **No Medical Advice Disclaimer**
   - MOSAIC does not provide medical advice
   - Final diagnostic and treatment decisions remain with qualified healthcare professionals

> The complete Terms & Conditions and Privacy Policy content is scrollable within the modal.

## User Consent Requirement

To proceed with submission, the user must explicitly confirm the following:

- ☑️ *I have scrolled through and read the Terms & Conditions, Privacy Policy, and Declaration.*

This checkbox is **mandatory**.

## Actions

| Action | Description |
|------|-------------|
| Cancel | Closes the modal and returns the user to the Review & Submit page without submitting the order |
| Submit | Finalizes and submits the order after consent is provided |

## Validation Rules

- The **Submit** button within the modal is enabled **only after** the consent checkbox is selected.
- If the checkbox is not selected, the user cannot complete order submission.
- Submission indicates acceptance of all listed terms and declarations.

## Submission Outcome

Once the Terms, Privacy & Declaration are accepted:

- The order is successfully submitted
- An order reference ID is generated
- The order status is updated accordingly
- Any next steps (such as secure upload links, if applicable) are triggered
  
## Related Documentation

* Home Dashboard
* View All Orders
* Order Details & Results
