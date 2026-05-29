## **1\. Regulatory Trigger**

### **Veeva-like concept**

A regulatory trigger represents the reason for creating a regulatory submission.

### **Project file**

`EMA Variations Master Database.xlsx`

### **Example triggers**

* MAH name or address change  
* Manufacturing site change  
* Stability update  
* Specification update  
* Labelling change  
* GMP certificate update  
* New strength or extension-type change

## **2\. Submission Record**

### **Veeva-like concept**

A submission record represents the regulatory activity submitted to a health authority.

### **Project file**

`Novalex Submission Tracker.xlsx`

### **Example fields**

* Submission\_ID  
* Product\_Name  
* Variation\_Category  
* Submission\_Status  
* Planned\_Submission\_Date  
* Actual\_Submission\_Date  
* Approval\_Decision\_Date  
* Risk\_Level  
* Functional\_Owner

## **3\. Content Plan**

### **Veeva-like concept**

A content plan defines the CTD sections and documents required for a submission.

### **Project file**

`Novalex_Content_Plan_Tracker.xlsx`

### **Example fields**

* Content\_Plan\_ID  
* Submission\_ID  
* CTD\_Module  
* CTD\_Section  
* Required\_Document  
* Document\_Owner  
* Content\_Status  
* Readiness\_Flag

## **4\. Document Lifecycle**

### **Veeva-like concept**

Documents move through controlled lifecycle states such as Draft, In Review, Approved, and Published.

### **Project file**

`Novalex_Document_Lifecycle_Tracker.xlsx`

### **Example fields**

* Document\_ID  
* Content\_Plan\_ID  
* Submission\_ID  
* Document\_Name  
* Version  
* Author  
* Reviewer  
* Approver  
* Document\_Status  
* Draft\_Start\_Date  
* Review\_Start\_Date  
* Approval\_Date

## **5\. Publishing**

### **Veeva-like concept**

Approved content is published into a submission package such as an eCTD sequence.

### **Project file**

`Novalex_Publishing_Tracker.xlsx`

### **Example fields**

* Publishing\_ID  
* Submission\_ID  
* Sequence\_Number  
* Submission\_Format  
* Lifecycle\_Operation  
* Publishing\_Status  
* Validation\_Status  
* Gateway\_Submission\_Status  
* Acknowledgement\_Received

## **6\. Agency Query Management**

### **Veeva-like concept**

Health authority questions are tracked, assigned, reviewed, responded to, and closed.

### **Project file**

`Novalex Agency Query Tracker.xlsx`

### **Example fields**

* Query\_ID  
* Submission\_ID  
* Query\_Round  
* Query\_Type  
* Query\_Subcategory  
* CTD\_Module\_Impacted  
* Response\_Owner  
* Reviewer  
* Response\_Due\_Date  
* Response\_Submitted\_Date  
* Query\_Status

## **7\. Implementation Tracking**

### **Veeva-like concept**

After approval, the company must implement the approved change.

### **Project file**

`Novalex Submission Tracker.xlsx`

### **Example fields**

* Approval\_Decision\_Date  
* Target\_Implementation\_Date  
* Actual\_Implementation\_Date  
* Submission\_Status  
* Days\_Since\_Target

## **8\. Archive**

### **Veeva-like concept**

Final submitted sequences, correspondence, validation reports, and approval records are archived.

### **Project file**

`Novalex_Archive_Tracker.xlsx`

### **Example fields**

* Archive\_ID  
* Submission\_ID  
* Publishing\_ID  
* Archive\_Status  
* Final\_Dossier\_Available  
* Validation\_Report\_Available  
* Gateway\_Acknowledgement\_Available  
* Agency\_Correspondence\_Available  
* Approval\_Letter\_Available  
* Archive\_QC\_Status

## **Project Workflow Mapping Table**

| Veeva/RIM Concept | Project File |
| ----- | ----- |
| Regulatory trigger | EMA Variations Master Database |
| Submission record | Novalex Submission Tracker |
| Content plan | Novalex Content Plan Tracker |
| Document lifecycle | Novalex Document Lifecycle Tracker |
| Publishing sequence | Novalex Publishing Tracker |
| Agency query tracking | Novalex Agency Query Tracker |
| Implementation tracking | Novalex Submission Tracker |
| Final archive | Novalex Archive Tracker |
| Product lifecycle view | Novalex Timeline |
| Product master/status | Drug Information / Drug Current Status |

## **Important Note**

This is a simplified educational model. Actual Veeva Vault RIM systems include more detailed object relationships, workflows, lifecycle states, permissions, audit trails, and controlled document management features.

