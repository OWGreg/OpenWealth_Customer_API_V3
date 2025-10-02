
```mermaid
erDiagram

    Customer {
    }

    Person {
    }

    legalPerson {
    }

    tin {
    }

    CustomerPersonRelation {
    }

    person2personRelation {
    }

    Address {
    }

    Contact {
    }

    Document {
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

    InitialAmount {          
    }

    ExpectedFundFlow {          
    }

    %% Beziehungen

    Customer ||--|{ CustomerPersonRelation : hasMultiple
    Customer ||--o{ Document : hasMultiple
    CustomerPersonRelation }o--|| Person : hasMultiple
    person2personRelation }o--|| Person : hasMultiple
    person2personRelation }o--|| Person : isRelatedPerson

    Person ||--o{ Address : hasMultiple
    Person ||--o{ Contact : hasMultiple
    Person ||--o{ tin : hasMultiple
    Person ||--o| legalPerson : hasOne
    Person ||--o| Employment : hasOne
    Person ||--o| Education : hasOne
    Person ||--o| WealthProfile : hasOne
    Person ||--o| RiskCompliance : hasOne
    Person ||--o{ FundFlows : hasMultiple
    Person ||--o| FATCA : hasOne
    
    RiskCompliance ||--o{ CorporateInsider : hasMultiple
    RiskCompliance ||--o{ MajorShareholder : hasMultiple

    FundFlows  ||--o{ InitialAmount : hasMultiple
    FundFlows  ||--o{ ExpectedFundFlow : hasMultiple
