# CLM API – USER STORIES 
## Use Case 1 – Client Onboarding (New Client Opening)

### Stakeholder: EAM External Asset Manager / FIM Financial Intermediary

- As an external asset manager,  
  I want to send a structured client onboarding package  
  so that the bank can automatically initiate the client opening process without manual re-entry.

- As an external asset manager,  
  I want to send the necessary client-documentation files through my PMS to the bank  
  so that the bank has all the required documents and I only have to upload the client-documentation once.

- As an external asset manager,  
  I want to track the status of the onboarding request (e.g., received, in review, approved, rejected)  
  so that I can inform my client about the progress and react to any missing items.

- As an external asset manager,  
  I want to indicate the desired relationship manager, team, or onboarding channel  
  so that the bank can route the request to the appropriate internal desk.

### Stakeholder: PMS System

- As a PMS system,  
  I want to transmit the full client identification data set (name, address, date of birth, nationality, etc.)  
  so that the bank has a consistent and compliant basis to create the client master record.

- As a PMS system,  
  I want to submit the legal form and structure of the client (individual, company, trust, etc.)  
  so that the bank can determine applicable onboarding workflows and documentation requirements.

- As a PMS system,  
  I want to send all known beneficial owners and controlling persons related to the client  
  so that the bank can perform necessary AML checks and UBO validations.

- As a PMS system,  
  I want to include contact persons and power of attorney holders with their identification data  
  so that the bank can correctly configure access rights and authorized signatures.

- As a PMS system,  
  I want to attach risk classification, investment strategy, and suitability profile information  
  so that the bank can ensure the portfolio setup complies with MiFID/FinSA rules.

- As a PMS system,  
  I want to send tax information (CRS/FATCA status, TINs, tax residence)  
  so that the bank can fulfill its tax reporting obligations from the start.

- As a PMS system,  
  I want to receive validation feedback from the bank (e.g., missing fields, incorrect formats)  
  so that data quality can be corrected proactively before manual intervention is required.

- As a PMS system,  
  I want to send structured attachments (e.g., IDs, proof of residence, signed agreements)  
  so that the bank can store them directly in the document management system.

- As a PMS system,  
  I want to provide a preferred booking center and domicile of the relationship  
  so that the bank can assign the correct legal entity and jurisdictional rules.

### Stakeholder: Bank

- As a bank,  
  I want to receive client onboarding data in a structured and validated format  
  so that I can automate the creation of client records in core systems with minimal manual intervention.

- As a bank,  
  I want to verify completeness and plausibility of all submitted client data  
  so that I can ensure regulatory and internal onboarding requirements are fulfilled.

- As a bank,  
  I want to extract and store UBO and controlling person information  
  so that I can perform AML risk assessments and fulfill regulatory disclosure obligations.

- As a bank,  
  I want to receive uploaded client documents (e.g., ID copies, proof of residence, tax forms)  
  so that I can archive them in my document management system and validate authenticity.

- As a bank,  
  I want to validate tax residency and CRS/FATCA classification  
  so that I can determine any tax reporting obligations.

- As a bank,  
  I want to notify the external asset manager of the onboarding request status (e.g., in process, accepted, rejected)  
  so that client expectations are managed and delays are avoided.

- As a bank,  
  I want to receive relationship-level metadata (e.g., assigned RM, internal segmentation, origin of relationship)  
  so that I can route and categorize the new relationship appropriately.

- As a bank,  
  I want to detect and block duplicate or conflicting onboarding requests  
  so that I maintain data integrity and avoid compliance risks.

- As a bank,  
  I want to log the source of onboarding data (e.g., PMS system ID, timestamp, submitting advisor)  
  so that I can ensure auditability and accountability of the onboarding process.

## Use Case 2 – Address Change / Relocation

### Stakeholder: External Asset Manager / Financial Intermediary (EAM/FIM)

- As an external asset manager,  
  I want to initiate an address change request via my PMS system  
  so that the change can be processed digitally without requiring paper forms.

- As an external asset manager,  
  I want to be notified if the bank accepts, rejects, or requests additional documentation for an address change  
  so that I can clarify next steps with the client and ensure compliance.

- As an external asset manager,  
  I want to submit supporting documents (e.g., utility bill or residence certificate)  
  so that the bank has evidence for address validation when required by internal or regulatory rules.

- As an external asset manager,  
  I want to track the effective date of the address change  
  so that I can synchronize my records and set appropriate reminders for related client follow-ups.

### Stakeholder: PMS System

- As a PMS system,  
  I want to support the entry and validation of new address data in structured fields (e.g., street, ZIP, city, country)  
  so that downstream systems like the bank can process the update automatically.

- As a PMS system,  
  I want to distinguish between domicile address and mailing address  
  so that different address types can be updated independently.

- As a PMS system,  
  I want to transmit the address change event with timestamp and user reference  
  so that the receiving party can perform traceable updates and meet audit requirements.

- As a PMS system,  
  I want to allow the upload of documents linked to the address change request  
  so that the bank can validate the change in line with internal policies.

### Stakeholder: Bank

- As a bank,  
  I want to receive structured address change notifications from external PMS systems  
  so that I can update the client’s records efficiently and reduce manual input errors.

- As a bank,  
  I want to validate whether the new address triggers any cross-border, tax, or compliance implications  
  so that I can initiate further review processes if needed (e.g., CRS reassessment).

- As a bank,  
  I want to distinguish whether the address change affects domicile or correspondence  
  so that I can update internal systems appropriately and avoid communication issues.

- As a bank,  
  I want to log the address change event along with user metadata and timestamp  
  so that I maintain a full audit trail of client lifecycle events.

- As a bank,  
  I want to notify the PMS system of the processing status (accepted, rejected, pending clarification)  
  so that the intermediary has visibility and the client is kept informed.

- As a bank,  
  I want to check whether the address change impacts risk classification or reporting obligations  
  so that I can trigger internal reassessments where necessary.


