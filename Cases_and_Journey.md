# CLM API – USER STORIES 
# Use Case 1 – Client Onboarding (New Client Opening)

## Stakeholder: EAM External Asset Manager / FIM Financial Intermediary

- As an external asset manager,  
  I want to send a structured client onboarding package  
  so that the bank can automatically initiate the client opening process without manual re-entry.

- As an external asset manager,  
  I want to send the necessary client-documentation files through my PMS to the bank  
  so that the bank has all the required documents.

- As an external asset manager,  
  I want to track the status of the onboarding request (e.g., received, in review, approved, rejected)  
  so that I can inform my client about the progress and react to any missing items.

- As an external asset manager,  
  I want to indicate the desired relationship manager, team, or onboarding channel  
  so that the bank can route the request to the appropriate internal desk.

## Stakeholder: PMS System

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
