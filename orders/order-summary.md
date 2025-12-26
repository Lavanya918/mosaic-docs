# Order Summary (Post-Submission)

After an order is successfully submitted, the user is redirected to the **Orders** page, which displays a consolidated list of all orders created by the user.

This page provides visibility into order identifiers, submission details, and the current processing status of each order.

## Orders Page Overview

**URL:**  
`/mosaic/orders`

**Purpose:**  
To allow users to:
- View submitted and draft orders
- Track order progress
- Access order details
- Create new orders
- Export order data

## Header Information

### Page Title
**Orders**

### Summary Indicator
- **Total Orders:** Displays the total number of orders associated with the user account.

### Primary Action
- **+ New Order**  
  Initiates the *Create New Order* workflow.

## Data Export Actions

| Action | Description |
|------|-------------|
| Export All Data | Downloads all orders visible to the user |
| Export Filtered Data | Downloads only orders matching applied filters |

## Orders Table

Each row in the table represents a single order.

### Columns

| Column | Description |
|------|-------------|
| Order ID | System-generated unique order reference |
| Patient ID | Unique identifier associated with the patient |
| Requester | User who created or submitted the order |
| Status | Current processing state of the order |
| Created | Date and time when the order was created |
| Actions | Contextual actions such as edit or view |

> All identifiers shown in documentation use placeholders and do not represent real patient or user data.

## Order Status Indicators

The **Status** column uses icons and labels to represent the order lifecycle.

Common statuses include:

- **Draft**  
  Order has been saved but not submitted.

- **Submitted**  
  Order has been successfully submitted for processing.

- **In Processing**  
  Sample logistics or analysis is in progress.

- **Completed**  
  Analysis and processing have been completed.

> Status indicators may be represented using icons, labels, or a combination of both.

## Filtering and Search

The Orders table supports filtering and sorting by:

- Order ID
- Patient ID
- Requester
- Status
- Creation date

This allows users to quickly locate specific orders.

## Pagination Controls

- Users can select the number of rows displayed per page.
- Navigation controls allow paging through large order lists.

## Privacy & Data Protection Notes

- Personal, clinical, and patient-identifiable information is masked or anonymized in documentation.
- Real names, email addresses, phone numbers, and identifiers must **never** be included in public documentation.
- Placeholder values (e.g., `<ORDER_ID>`, `<PATIENT_ID>`, `<REQUESTER_NAME>`) are recommended.

## Navigation Flow

**Create New Order → Review & Submit → Accept Terms → Order Submitted → Orders Page**

This page serves as the **final confirmation point** that the order has been successfully created and is being tracked by the system.

