# Asset-Management-Portal-ServiceNow

## Overview
The **Asset Management Portal** is a ServiceNow-based application designed to manage and track organizational assets through a centralized system. The portal allows administrators to create, assign, monitor, and maintain assets while automating key processes such as asset status updates, warranty monitoring, and reporting.

This system replaces manual asset tracking methods such as spreadsheets with an automated solution that improves asset visibility, operational efficiency, and data accuracy.

Developed as part of the **SmartInternz ServiceNow Internship Project (2025–2026).**

---

## Key Features

### 1. Centralized Asset Inventory
A custom ServiceNow table stores all asset information including:

- Asset Name  
- Asset Number (Auto-generated)  
- Asset Type  
- Assigned To  
- Status  
- Purchase Date  
- Warranty Expiry Date  

This provides a **single centralized location** to manage and track all assets.

---

### 2. Asset Status Management
The portal includes UI action buttons that allow administrators to update asset status quickly.

Available actions:

- **Mark As Lost**
- **Mark As Damaged**
- **Mark As Repaired**

Each button appears only when appropriate based on the current asset status.

Example:
- Damaged assets show **Repaired** option
- Available assets show **Lost** and **Damaged**
- Lost assets show **Repaired**

---

### 3. Automated Warranty Monitoring
A **Scheduled Job** runs daily to check for assets with warranties expiring within the next **30 days**.

If any assets match the condition:
- The system automatically sends **email alerts**
- IT support teams can take proactive maintenance actions

---

### 4. Reporting and Analytics
The portal includes built-in reporting using the **ServiceNow Reporting Engine**.

Report features:

- Pie chart visualization
- Asset status distribution
- Hover tooltips with percentages
- Drill-down to asset records

This helps administrators understand the current condition of organizational assets.

---

## System Architecture

The application follows a **four-layer architecture**:

### Data Layer
Stores asset records in the custom table:


### Logic Layer
Handles automation through:

- UI Actions
- Scheduled Jobs
- Business Rules
- Number Maintenance

### UI Layer
Provides user interaction via:

- Asset forms
- List views
- UI action buttons
- Reports and dashboards

### Configuration Layer
Uses **Update Sets** for deployment and configuration management.

---

## Technology Stack

| Component | Technology |
|-----------|------------|
| Platform | ServiceNow |
| Backend Logic | GlideRecord API |
| Automation | Scheduled Jobs |
| Email Notifications | GlideEmailOutbound |
| Reporting | ServiceNow Reporting Engine |
| Database | ServiceNow Tables |

---

## Project Structure


---

## Testing

The system was tested using multiple scenarios:

| Test Scenario | Expected Result |
|---------------|----------------|
| Create asset | Record stored successfully |
| Mark asset damaged | Status changes to Damaged |
| Mark asset repaired | Status returns to Available |
| Mark asset lost | Status changes to Lost |
| Scheduled job run | Email alerts sent |
| Report generation | Accurate asset distribution |

All test cases were **successfully passed**.

---

## Advantages

- Centralized asset management
- Reduced manual tracking effort
- Automated warranty monitoring
- Quick status updates with UI actions
- Real-time reporting and analytics
- Role-based security through ServiceNow

---

## Limitations

- Requires ServiceNow platform license
- Assets must be manually entered
- Limited reporting capabilities
- No mobile barcode or QR scanning

---

## Future Enhancements

Planned improvements include:

- Mobile app with QR/Barcode scanning
- Predictive maintenance analytics
- Employee self-service asset request portal
- Procurement system integration
- Multi-location asset tracking
- Network device auto-discovery
- Financial depreciation tracking
- AI-based asset allocation recommendations

---

## Conclusion
The **Asset Management Portal** demonstrates how the ServiceNow platform can be used to build an automated asset lifecycle management system. By integrating centralized data management, automation, and reporting, the system improves asset visibility, reduces operational costs, and enables data-driven decision-making.
