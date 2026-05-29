# **Novalex EU Variations RIM Dashboard**

## **Project Overview**

This project is a fictional regulatory affairs portfolio project that simulates a **Veeva Vault RIM-style regulatory submissions dashboard** for an EU-approved medicinal product named **Novalex**.

The project focuses on post-authorisation lifecycle management, including EU variation submissions, agency queries, CTD content planning, document lifecycle tracking, publishing readiness, and archive QC monitoring.

The objective is to demonstrate how regulatory submission data can be structured, automated, connected, and visualised using **Excel, Python, Power Query, DAX, and Power BI**.

---

## **Product Context**

**Novalex** is a fictional EU-approved product used for this simulation.

| Field | Details |
| ----- | ----- |
| Product Name | Novalex |
| Region | European Union |
| Health Authority | EMA |
| Procedure Type | Centralised Procedure |
| MAA Approval Date | 15-Mar-2022 |
| Lifecycle Stage | Post-authorisation lifecycle management |
| First Post-authorisation Variation | 15-Jun-2024 |
| Current Portfolio Checkpoint | Q2 2026 |
| Current Focus | EU variations, implementation tracking, agency query readiness, publishing, and archive oversight |

---

## **Business Problem**

Regulatory teams manage multiple submissions, documents, agency queries, implementation deadlines, publishing activities, and archive records across several systems or trackers.

Without a centralised dashboard, it becomes difficult to answer questions such as:

* Which submissions are currently active?  
* Which submissions are implementation overdue?  
* Which variation types carry the highest risk?  
* Which CTD modules are generating the most agency queries?  
* Which documents are still in review?  
* Which submissions are publishing-ready?  
* Which final packages are archived and QC-complete?

This project addresses that problem by creating an integrated regulatory operations dashboard.

## **Project Scope**

The dashboard simulates the following regulatory workflow:

Drug Profile  
    ↓  
Submission Tracker  
    ↓  
Content Plan Tracker  
    ↓  
Document Lifecycle Tracker  
    ↓  
Publishing Tracker  
    ↓  
Agency Query Tracker  
    ↓  
Archive Tracker  
    ↓  
Power BI Dashboard

The workflow is inspired by Veeva Vault RIM concepts but implemented using simulated Excel datasets, Python automation, and Power BI.

## **Dashboard Pages**

The Power BI report contains the following pages:

### **1\. Drug Profile**

Provides a product-level view of Novalex, including:

* Product identity  
* MAA approval date  
* Current lifecycle status  
* Current regulatory activity  
* Regulatory approval status gauge  
* Key lifecycle milestones

### **2\. Executive Overview**

Provides a management-level portfolio summary, including:

* Total submissions  
* Archived submissions  
* Under assessment submissions  
* Pending implementation  
* Implementation overdue  
* Total agency queries  
* Submission status distribution  
* Variation category mix  
* Risk profile  
* Overdue implementation watchlist

### **3\. Submission Pipeline**

Tracks submission timelines and delays, including:

* Planned vs actual submission lifecycle  
* Submission delay days  
* Assessment duration  
* Implementation overdue days  
* Submission status pipeline

### **4\. Agency Query Intelligence**

Analyses health authority query patterns, including:

* Queries by type and round  
* CTD module query heat map  
* Average days to respond  
* Query workload by response owner  
* Query subcategory by submission

### **5\. Document Readiness & Lifecycle**

Tracks CTD content and document review lifecycle, including:

* Document status by CTD module  
* Average days in review  
* Draft-to-approval Gantt chart  
* Document ownership breakdown  
* Content readiness status

### **6\. Publishing & Archive Pipeline**

Tracks eCTD publishing and archive health, including:

* Submitted packages  
* Validation passed  
* Archived packages  
* Pending archive QC  
* Archive QC status by submission  
* Final dossier and agency correspondence availability

### **7\. EMA Variation Reference Intelligence**

Provides variation classification reference insights, including:

* Variation category by risk level  
* Preapproval requirement by variation type  
* Variation type by example category  
* Common required documents  
* Regulatory burden by variation category

### **8\. Drug Lifecycle Timeline**

Shows the full product lifecycle from development through post-authorisation maintenance, including:

* Development activities  
* MAA submission and approval  
* Launch readiness  
* First post-authorisation variation  
* Future planned variations  
* Renewal and long-term lifecycle management

## **Data Files**

The project uses both raw and processed datasets.

### **Raw Data**

| File | Purpose |
| ----- | ----- |
| `EMA Variations Master Database.xlsx` | Reference database for EU variation triggers and classifications |
| `Novalex Submission Tracker.xlsx` | Main submission-level tracker |
| `Novalex Agency Query Tracker.xlsx` | Simulated health authority query tracker |
| `Novalex timeline.xlsx` | Drug lifecycle timeline data |
| `Drug Information.xlsx` | Product profile and current status information |

### **Processed Data**

| File | Purpose |
| ----- | ----- |
| `Novalex_Content_Plan_Tracker.xlsx` | CTD content plan generated from submission data |
| `Novalex_Document_Lifecycle_Tracker.xlsx` | Document review and approval lifecycle tracker |
| `Novalex_Publishing_Tracker.xlsx` | eCTD publishing and validation tracker |
| `Novalex_Archive_Tracker.xlsx` | Archive and QC status tracker |
| `Novalex_Data_Dictionary.xlsx` | Data dictionary for all project files |
| `Novalex_Relationship_Map.xlsx` | Power BI relationship mapping guide |

---

## **Python Automation**

Python was used to generate the processed regulatory trackers.

The automation created:

1. **Content Plan Tracker**  
   Generated required CTD sections and documents for each submission.  
2. **Document Lifecycle Tracker**  
   Created document records with versioning, authors, reviewers, approvers, lifecycle status, and review dates.  
3. **Publishing Tracker**  
   Created publishing status, eCTD sequence numbers, validation status, and gateway acknowledgement fields.  
4. **Archive Tracker**  
   Created archive records, final dossier availability flags, agency correspondence flags, and archive QC status.  
5. **Data Dictionary**  
   Automatically extracted table names, column names, data types, and sample values.  
6. **Relationship Map**  
   Documented how all trackers connect in Power BI.

## **Power BI Data Model**

The main Power BI relationships are:

| From Table | Column | To Table | Column |
| ----- | ----- | ----- | ----- |
| Submission Tracker | `Submission_ID` | Content Plan Tracker | `Submission_ID` |
| Content Plan Tracker | `Content_Plan_ID` | Document Lifecycle Tracker | `Content_Plan_ID` |
| Submission Tracker | `Submission_ID` | Agency Query Tracker | `Submission_ID` |
| Submission Tracker | `Submission_ID` | Publishing Tracker | `Submission_ID` |
| Publishing Tracker | `Publishing_ID` | Archive Tracker | `Publishing_ID` |

Reference tables such as the EMA Variations Master Database and Drug Lifecycle Timeline are used for contextual analysis and dashboard pages.

## **Key Measures and Calculations**

The dashboard includes DAX measures and calculated columns such as:

* Total Submissions  
* Archived Submissions  
* Under Assessment Submissions  
* Pending Implementation  
* Implementation Overdue  
* Total Agency Queries  
* Open Agency Queries  
* Responded Late Queries  
* Content Readiness %  
* Document Approval %  
* Average Days in Review  
* Average Days to Respond  
* Submitted Packages  
* Validation Passed  
* Archived Packages  
* Pending QC Count  
* Days Since Target  
* Submission Delay Days  
* Assessment Duration Days

These measures support the KPI cards, charts, matrices, and conditional formatting across the dashboard.

## **Key Insights Simulated**

The dashboard is designed to surface the following regulatory insights:

* Novalex is approved and currently in post-authorisation lifecycle management.  
* Most submissions are completed and archived.  
* Type II CMC/Quality variations carry the highest regulatory burden.  
* Implementation overdue submissions are a key operational risk.  
* Module 3 quality sections generate the highest agency query volume.  
* Review timelines are longer for complex Type II documents.  
* Agency query workload is concentrated across CMC Regulatory, QA, ASMF Holder, and Regulatory Affairs owners.  
* Publishing readiness is high, but archive QC status still requires monitoring.  
* Final dossier completeness depends on validation reports, approval letters, gateway acknowledgements, and agency correspondence availability.

---

## **Repository Structure**

novalex-eu-variations-rim-dashboard/  
│  
├── README.md  
├── LICENSE  
├── .gitignore  
│  
├── data/  
│   ├── raw/  
│   ├── processed/  
│   └── sample\_csv/  
│  
├── powerbi/  
│   ├── Novalex Variations.pbix  
│   └── dashboard\_export.pdf  
│  
├── scripts/  
│   ├── novalex\_python\_scripts.py  
│  
├── docs/  
│   ├── project\_overview.md  
│   ├── regulatory\_assumptions.md  
│   ├── data\_dictionary.md  
│   ├── dashboard\_page\_guide.md  
│   ├── veeva\_rim\_workflow\_mapping.md  
│   ├── ema\_variation\_logic.md  
│   └── limitations\_and\_disclaimer.md

## **Skills Demonstrated**

This project demonstrates skills across regulatory affairs, analytics, and dashboard development.

### **Regulatory Affairs**

* EU variation lifecycle understanding  
* Post-authorisation submission tracking  
* CTD content planning  
* Agency query management  
* Implementation monitoring  
* Publishing and archive workflow mapping  
* Veeva Vault RIM-style process simulation

### **Data and Analytics**

* Excel data modelling  
* Python automation  
* Power Query transformations  
* DAX measures  
* Power BI data modelling  
* KPI design  
* Conditional formatting  
* Dashboard storytelling

### **Portfolio and Documentation**

* GitHub project structuring  
* Data dictionary creation  
* Workflow documentation  
* Dashboard page guide  
* Regulatory assumptions documentation  
* Project disclaimer and limitations

## **How to Use This Project**

1. Open the Power BI file from the `powerbi/` folder.  
2. Review the Drug Profile page to understand the product context.  
3. Move to the Executive Overview page for the portfolio health summary.  
4. Use slicers to filter by variation category, submission status, risk level, query round, query type, or archive QC status.  
5. Review detailed operational pages for agency queries, document readiness, publishing, and archive status.  
6. Refer to the `docs/` folder for assumptions, data dictionary, dashboard guide, and workflow mapping.

## **Future Improvements**

Possible future enhancements include:

* Automated variation classification using rule-based logic or machine learning  
* AI-assisted CTD section prediction  
* Query risk scoring model  
* Automated agency response drafting support  
* Submission readiness scoring  
* Integration with SharePoint or document management systems  
* More advanced Power BI drill-through pages  
* Row-level security by function or owner  
* Simulated Veeva Vault object model  
* Enhanced Power Query data validation checks

## **Disclaimer**

This is a fictional regulatory affairs portfolio project created for learning and demonstration purposes.

Novalex is a fictional product. The data does not represent real EMA submissions, real Veeva Vault configuration, real company regulatory records, real patient data, or confidential pharmaceutical information.

This project is not intended to provide regulatory advice. Actual regulatory decisions should always be based on current regulations, official health authority guidance, product-specific context, and expert regulatory review.

## **Author**

Created as a regulatory affairs and Power BI portfolio project to demonstrate EU variation lifecycle management, regulatory submissions tracking, and Veeva Vault RIM-style dashboard development.

