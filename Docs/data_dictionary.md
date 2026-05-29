\# Data Dictionary

\#\# Purpose

This document describes the main data files used in the Novalexib EU Variations RIM Dashboard project.

The project includes raw input files and Python-generated processed trackers.

\#\# Data Sources

\#\# 1\. EMA Variations Master Database

This file acts as the regulatory reference database for variation classification.

\#\#\# Key Columns

| Column | Description |  
|---|---|  
| Trigger\_ID | Unique identifier for each regulatory trigger |  
| Variation\_Category | IA, IAIN, IB, II, or Extension |  
| Type\_of\_Example | Administrative, CMC/Quality, Safety, Clinical, etc. |  
| Risk\_Level | Low, Medium, or High regulatory risk |  
| Preapproval\_Required\_or\_Not | Indicates whether prior approval is required |  
| Key\_Documents\_Involved | Main documents expected for the variation |  
| Affected\_CTD\_Modules | CTD modules likely impacted |  
| Description | Description of the regulatory trigger |

\#\# 2\. Novalex Submission Tracker

This is the main submission-level tracker.

\#\#\# Key Columns

| Column | Description |  
|---|---|  
| Submission\_ID | Unique identifier for each submission |  
| Product\_Name | Product associated with the submission |  
| Submission\_Title | Short title of the submission |  
| Variation\_Category | Variation type such as IA, IAIN, IB, II |  
| Submission\_Category | Administrative, CMC, Quality, Safety, etc. |  
| Submission\_Status | Current lifecycle status |  
| Planned\_Submission\_Date | Planned date of submission |  
| Actual\_Submission\_Date | Actual date submitted |  
| Approval\_Decision\_Date | Approval or decision date |  
| Target\_Implementation\_Date | Planned implementation completion date |  
| Actual\_Implementation\_Date | Actual implementation date |  
| Risk\_Level | Submission risk level |  
| Functional\_Owner | Function responsible for the submission |

\#\# 3\. Novalex Agency Query Tracker

This tracker captures health authority questions and responses.

\#\#\# Key Columns

| Column | Description |  
|---|---|  
| Query\_ID | Unique query identifier |  
| Submission\_ID | Submission linked to the query |  
| Query\_Round | Validation, Round 1, Round 2 |  
| Query\_Type | Quality, CMC, GMP, Stability, etc. |  
| Query\_Subcategory | More detailed query topic |  
| Query\_Title | Short query title |  
| Query\_Description | Description of the query |  
| CTD\_Module\_Impacted | CTD module impacted by the query |  
| Query\_Received\_Date | Date the query was received |  
| Response\_Due\_Date | Due date for the response |  
| Response\_Submitted\_Date | Date response was submitted |  
| Query\_Status | Open, In Progress, Closed, Overdue, etc. |  
| Response\_Owner | Team or owner responsible for response |  
| Reviewer | Reviewer assigned to query response |  
| Risk\_Level | Query risk level |  
| Days\_To\_Respond | Number of days taken to respond |

\#\# 4\. Novalex Content Plan Tracker

This tracker simulates a Veeva-style content plan.

\#\#\# Key Columns

| Column | Description |  
|---|---|  
| Content\_Plan\_ID | Unique content plan item identifier |  
| Submission\_ID | Submission linked to the content plan |  
| CTD\_Module | CTD module required |  
| CTD\_Section | CTD section required |  
| Required\_Document | Document required for the submission |  
| Document\_Type | Administrative, CMC, Clinical, Labelling, etc. |  
| Document\_Owner | Owner responsible for the document |  
| Planned\_Due\_Date | Planned document completion date |  
| Actual\_Completion\_Date | Actual completion date |  
| Content\_Status | Planned, In Review, Approved, Published |  
| Readiness\_Flag | Ready, In Progress, Not Ready |  
| Risk\_Level | Risk associated with the content item |

\#\# 5\. Novalex Document Lifecycle Tracker

This tracker simulates controlled document lifecycle management.

\#\#\# Key Columns

| Column | Description |  
|---|---|  
| Document\_ID | Unique document identifier |  
| Content\_Plan\_ID | Linked content plan item |  
| Submission\_ID | Linked submission |  
| Document\_Name | Name of the document |  
| Document\_Type | Type of document |  
| Version | Document version |  
| Author | Document author |  
| Reviewer | Document reviewer |  
| Approver | Final approver |  
| Document\_Status | Draft, In Review, Approved, Published |  
| Draft\_Start\_Date | Date drafting started |  
| Review\_Start\_Date | Date review started |  
| Approval\_Date | Date document was approved |  
| Days\_In\_Review | Number of days in review |  
| Overdue\_Flag | Indicates whether document is overdue |  
| Final\_or\_Draft | Final, Draft, or Not Created |

\#\# 6\. Novalex Publishing Tracker

This tracker simulates eCTD publishing and validation status.

\#\#\# Key Columns

| Column | Description |  
|---|---|  
| Publishing\_ID | Unique publishing record |  
| Submission\_ID | Linked submission |  
| Sequence\_Number | eCTD sequence number |  
| Submission\_Format | eCTD or non-eCTD |  
| Lifecycle\_Operation | New, Replace, Delete, Append |  
| Readiness\_Percent | Percentage of documents ready |  
| Publishing\_Status | Publishing lifecycle status |  
| Validation\_Status | Passed, Pending, Failed, etc. |  
| Validation\_Errors | Number of validation issues |  
| Publish\_Start\_Date | Publishing start date |  
| Publish\_Complete\_Date | Publishing completion date |  
| Gateway\_Submission\_Status | Gateway submission status |  
| Acknowledgement\_Received | Whether acknowledgement was received |

\#\# 7\. Novalex Archive Tracker

This tracker simulates final dossier archive and QC status.

\#\#\# Key Columns

| Column | Description |  
|---|---|  
| Archive\_ID | Unique archive identifier |  
| Submission\_ID | Linked submission |  
| Publishing\_ID | Linked publishing record |  
| Sequence\_Number | eCTD sequence number |  
| Submission\_Date | Date submitted |  
| Approval\_Date | Approval decision date |  
| Archive\_Date | Archive completion or target date |  
| Archive\_Status | Archived, Ready for Archive, Not Ready |  
| Final\_Dossier\_Available | Yes/No flag |  
| Validation\_Report\_Available | Yes/No flag |  
| Gateway\_Acknowledgement\_Available | Yes/No flag |  
| Agency\_Correspondence\_Available | Yes/No flag |  
| Approval\_Letter\_Available | Yes/No flag |  
| Archive\_QC\_Status | QC Complete, Pending QC, Not Started |

\#\# 8\. Drug Information / Drug Current Status

This table provides the product master and current lifecycle status.

\#\#\# Key Columns

| Column | Description |  
|---|---|  
| Drug Name | Product name |  
| Current Lifecycle Stage | Current lifecycle phase |  
| Current Status | Current regulatory status |  
| Current Quarter | Portfolio checkpoint quarter |  
| Current Activity | Current regulatory activity |  
| Regulatory Focus | Main focus area |  
| Next Milestone | Next planned milestone |  
| Risk Level | Current product-level risk |  
| Regulatory Approval Status % | Approval completion gauge value |

\#\# 9\. Novalex Timeline

This file supports the lifecycle Gantt page.

\#\#\# Key Columns

| Column | Description |  
|---|---|  
| Task | Lifecycle task or milestone |  
| Start Quarter | Start quarter |  
| End Quarter | End quarter |  
| Start Date | Task start date |  
| End Date | Task end date |  
| Category | Lifecycle category |  
| Status | Completed, Ongoing, Planned, Current |  
| Milestone | Yes/No milestone flag |

