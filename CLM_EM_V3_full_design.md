
```mermaid
erDiagram

    Customer {
        *string customerId
        string externalReference
        string customerType
        string status
        *string name
        string openingDate
        string referenceCurrency
        string language
        string customerSegment
        *string[] personList
        object externalAssetManager
    }

    Person {
        string personId
        string externalReference
        enum personType
        string language
        string openingDate
        string givenName
        string middleName
        string lastName
        string title
        string gender
        array nationalities
        string civilStatus
        string dateOfBirth
        string dateOfDeath
        string dateOfMarriage
        string countryOfBirth
        object tinList
        object legalPerson "organisationName, legalForm, lei, domiciliaryCompany" 
    }

    tinList {
        string tinNumber
        string tinCountry
    }

    CustomerPersonRelation {
        string id
        *enum relationType
        string cardinality
        boolean soleBeneficialOwner
        string bankAdvisor
        string bankDeputyAdvisor
        string bankPreviousAdvisor
        string personId
        string relatedCustomerId
        string purposeOfRelationship
        string additionalInformationPurpose
        boolean soleBeneficialOwner
    }

    person2personRelation {
        string id
        enum type
        string personId
        string relatedPersonId
        string relation
        string relationOverride
        boolean personAssociation
        string personAssociationName
        string personAssociationType
    }

    Address {
        string addressId
        string personId
        string externalReference
        enum type
        string addressName
        boolean isDomicile
        string language
        boolean isMailingAddress
        string receptionRestriciton
        string salutation
        string title
        string salutationOverride
        string organisationName
        string givenName
        string lastName
        string careOf
        string toTheAttentionOf
        string department
        string streetName
        string buildingNumber
        string buildingName
        string floor
        string postBox
        string room
        string postcode
        string townName
        string townLocationName
        string districtName
        string countrySubDivision
        string country
    }

    Contact {
        string id
        enum medium
        enum prio
        string content
    }

    Document {
        string id
        string customerId
        enum group
        enum type
        enum status
        date issueDate
        string content
    }

    Education {
        string highestDiploma
        integer graduationYear
        string institute
        string studyProgramme
        object educationInformation
    }

    Employment {
        string companyName
        object companyDomicile
        object[] companyCountriesOfBusinessList
        string companyDetail
        integer companyNumberOfEmployees
        number companyAnnualTurnover
        string industry
        object roleOrPosition
        profession profession
        string domicile
        number shareholdingInPercent
        object period
        integer yearOfRetirement
        integer sharedholderSinceYear
        string mandate
        string additionalInformation
        object employmentInformation
    }

    WealthProfile {
        string sourceOfWealth_type
        object sourceOfWealth_amount
        object[] sourceOfWealth_countriesOfOrigin
        object sourceOfWealth_additionalProperties
        object totalWealth_amountTotalNetAssets
        object totalWealth_referenceYear
        object[] totalWealth_assetAllocation
        object totalIncome_amountYearlyIncome
        object totalIncome_referenceYear
        object[] totalIncome_sourceOfIncomeList
    }

    FundFlows {
        integer amountExpectedInflows
        string currencyExpectedInflow
        integer amountPlannedTotalAssets
        string currencyPlannedTotalAssets
        integer amountExpectedTurnover
        string currencyExpectedTurnover 
        object[] recurringCounterpartyList
        object[] initialAmountList
        object[] expectedFundFlowList
        integer numberOfInflows
        integer numberOfOutflows
    }

    CorporateInsider {
        string corporateInsiderAssociation
        string relation
        object position
        string companyName
        string isin
    }

    MajorShareholder {
        string majorShareholderAssociation
        string relation
        string companyName
        string isin
    }

    RiskCompliance {
        enum politicalStatus
        object countryOfDomicile
        object[] CorporateInsiderList
        object[] MajorSharholderList
            }

    TaxStatus {
        boolean fatcaStatus
        boolean fatcaDomicile
        boolean fatcaBirthplace
        boolean fatcaGreenCard
        boolean fatcaSubstantialPresenceTest
        boolean fatcaOtherReasons
        object[] taxDomicileList "taxDomicile"
    }

    InitialAmount {
        integer amount
        string currency
        string originOfAssets
        string originOfAssetsDetails
        string nameOfBank
        string domicileOfBank
        boolean physicalTransfer
        boolean electronicTransfer
        boolean samePerson
        string thirdPartyName
        string thirdPartyRelationship
        string thirdPartyReason
        string additionalInformation             
    }

    ExpectedFundFlow {
        enum type
        string counterparty
        string nameOfBank
        string domicileOfBank
        string purpose
        string frequency
        integer amount
        string currency
        string originOfAssets
        string additionalInformation             
    }

    %% Beziehungen

    Customer ||--|{ CustomerPersonRelation : hasMultiple
    Customer ||--o{ Document : hasMultiple
    CustomerPersonRelation }o--|| Person : hasMultiple
    person2personRelation }o--|| Person : hasMultiple
    person2personRelation }o--|| Person : isRelatedPerson

    Person ||--o{ Address : hasMultiple
    Person ||--o{ Contact : hasMultiple
    Person ||--o{ tinList : hasMultiple
    Person ||--o| Employment : hasOne
    Person ||--o| Education : hasOne
    Person ||--o| WealthProfile : hasOne
    Person ||--o| RiskCompliance : hasOne
    Person ||--o{ FundFlows : hasMultiple
    Person ||--o| TaxStatus : hasOne
    
    RiskCompliance ||--o{ CorporateInsider : hasMultiple
    RiskCompliance ||--o{ MajorShareholder : hasMultiple

    FundFlows  ||--o{ InitialAmount : hasMultiple
    FundFlows  ||--o{ ExpectedFundFlow : hasMultiple
