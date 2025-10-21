
```mermaid
erDiagram

%% Main Business Objects -------------------------------

    Customer {
    }

    Mandate {
    }

    Person {
    }

    Account {
    }

    Correspondence {
    }

    Document {
    }

%% Slave Business Objects -------------------------------

    Address {
    }

    Contact {
    }

    Education {
    }

    Employment {
    }

    WealthProfile {
    }

    FundFlows {
    }

    CorporateInsider {
    }

    MajorShareholder {
    }

    RiskCompliance {
    }

    FATCA {
    }

    tin {
    }

    InitialAmount {         
    }

    ExpectedFundFlow {           
    }

%% Relation-Definition-Objects -------------------------------

    customer2personRelation {
    }

    person2personRelation {
    }

    mandate2personRelation {
    }

%% Beziehungen

    Customer ||--|{ customer2personRelation : hasMultiple
    Customer ||--o{ Document : hasMultiple
    Customer ||--o{ Mandate : hasMultiple

    Mandate ||--o{ mandate2personRelation : hasMultiple
    Mandate ||--o{ Account : hasMultiple
    Mandate ||--o{ Document : hasMultiple  
    Mandate ||--o{ Correspondence : hasMultiple  

    Person ||--o{ Address : hasMultiple
    Person ||--o{ Contact : hasMultiple
    Person ||--o{ tin : hasMultiple
    Person ||--o{ Employment : hasOne
    Person ||--o{ Education : hasOne
    Person ||--o| WealthProfile : hasOne
    Person ||--o| RiskCompliance : hasOne
    Person ||--o{ FundFlows : hasMultiple
    Person ||--o| FATCA : hasOne
    Person ||--o{ Document : hasMultiple
  
    RiskCompliance ||--o{ CorporateInsider : hasMultiple
    RiskCompliance ||--o{ MajorShareholder : hasMultiple

    FundFlows  ||--o{ InitialAmount : hasMultiple
    FundFlows  ||--o{ ExpectedFundFlow : hasMultiple

    Correspondence ||--o| Address : hasOne
    Correspondence ||--o| Contact : hasOne
    
    customer2personRelation }o--|| Person : hasMultiple
    mandate2personRelation ||--o{ Person : hasMultiple 
    person2personRelation }o--|| Person : hasMultiple
    person2personRelation ||--|| Person : isRelatedPerson

%% Colors

    style Customer, Mandate, Person, Document, Correspondence fill:#e0f0ff,stroke:#3366cc,stroke-width:1px
    style customer2personRelation, mandate2personRelation, person2personRelation fill:#ffe0e0,stroke:#cc0000,stroke-width:1px
