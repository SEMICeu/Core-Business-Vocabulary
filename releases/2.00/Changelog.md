# Transition from Core Business v1.0.0 to v2.0.0

## Introduction

This document describes the (major) changes to [the current version 1.0.0](https://github.com/SEMICeu/Core-Business-Vocabulary/tree/master/releases/1.00) of the Core Business Vocabulary for which a new version is being proposed ([version 2.0.0](https://semiceu.github.io/Core-Business-Vocabulary/releases/2.00/)). The list of changes results in the new version to be considered as a major release.

## Detailed changes

The table below gives an overview of the classes (and their definitions) within both data models. Classes that are related are juxta-positioned.

**C** stands for changes in classes

**R** stands for changes in relationships

**P** stands for changes in properties

**D** stands for changes in data types

| Nr | Core Person Vocabulary v1.0.0 | Core Person Vocabulary v2.0.0 | Rationale | GitHub / Change |
| --- | --- | --- | --- | --- |
| C1 | **Change** | **Change class removed** Issue created: https://github.com/SEMICeu/Core-Person-Vocabulary/issues/10** | There should be a discussion on Github about the interest of keeping the Change class. | GitHub |
| P1 | **Jurisdiction id** | **Jurisdiction id** | Why is an ID property required for this class and not for others? Should we add/remove ID properties? | GitHub |
| D1 | **Person.familyName: String** | **Person.familyName: Text** | Alignment with SDG WP4 where the datatype was changed to allow for multi-script. |Change|
| D2 | **Person.givenName: String** | **Person.givenName: Text** | Alignment with SDG WP4 where the datatype was changed to allow for multi-script. | Change |
| D3 | **Person.alternativeName: String** | **Person.alternativeName: Text** | Following the same rationale as for given and family name. | Change |
| D4 | **Person.birthName: String** | **Person.birthName: Text** | Following the same rationale as for given and family name. | Change |
| D5 | **Person.fullName: String** | **Person.fullName: Text** | Following the same rationale as for given and family name. | Change |
| D6 | **Person.patronymicName: String** | **Person.patronymicName: Text** | Following the same rationale as for given and family name. | Change |
| P2 | **Person.givenName** | **Person.givenName (forename)** | Alignment with public documents schema. | Change |
| P3 | **Person.familyName** | **Person.familyName (surname)** | Alignment with public documents schema. | Change |
| R1 | **-** | **Person.registeredAddress: Address** | This relationship was needed by SDG WP4. | Change |
| P4 | **-** | **Person.identifier: added reference to eIDAS regulation and mapping.** | | Change |
| P5 | **Definition of Person.dateOfBirth/dateOfDeath:** &quot;A date that specifies the birth/death date of a Person.&quot; | &quot;The day on which the Person was born/died.&quot; | Improved definitions based on SDG WP4. | Change |
| R2 | **Definition of Person.placeOfBirth/placeOfDeath:**&quot;A Person&#39;s place of birth/death.&quot; | &quot;The Location where the Person was born / died.&quot; | Improved definitions based on SDG WP4. | Change |

| Nr | Core Location Vocabulary v1.0.0 | Core Location Vocabulary v2.0.0 | Rationale | GitHub / Change |
| --- | --- | --- | --- | --- |
| C1 | **Definition of Location: A spatial region or named place.** | An identifiable geographic place or named place. | Proposition made by SDG WP4. | Change |
| C2 | **Geometry (alternative representation)** | **Geometry (alternative representation) class removed and properties put** | Decrease ambiguity. | Change |
| C3 | **Definition of Address: Representation of an address spatial object for use in external application schemas that need to include the basic, address information in a readable way.** | A spatial object that in a human-readable way identifies a fixed location of a property. | Proposition made by SDG WP4. | Change |
| C4 | **-** | Resource | Addition of the resource class | Change |
| D1 | **Location:** Geographic name expects a string value | **Location:** Geographic name expects a text value. Also updated the usage note example accordingly. | Adapted data type for consistency. | Change |
| P1 | **-** | **Address: added an example in the usage notes for most properties** | To increase understandability. | Change |
| D2 | **Address.adminUnitL1: String** | **Address.adminUnitL1: Code** | Proposition made by SDG WP4. | Change |
| D3 | **Address.adminUnitL2: String** | **Address.adminUnitL2: Text** | Proposition made by SDG WP4 to allow for multi-language + alignment with INSPIRE. | Change |
| P2 | **-** | **Address.adminUnitL2: added recommended codelists** | To facilitate usage. | Change |
| D4 | **Address.fullAddress: String** | **Address.fullAddress: Text** | Proposition made by SDG WP4 to allow for multi-language. | Change |
| D5 | **Address.addressArea: String** | **Address.addressArea: Text** | To allow for multi-language + alignment with INSPIRE. | Change |
| D6 | **Address.locatorName: String** | **Address.locatorName: Text** | To allow for multi-language + alignment with INSPIRE. | Change |
| D7 | **Address.postName: String** | **Address.postName: Text** | To allow for multi-language + alignment with INSPIRE. | Change |
| D8 | **Address.thoroughfare: String** | **Address. thoroughfare: Text** | To allow for multi-language + alignment with INSPIRE. | Change |
| P3 | **Address.locatorDesignator:** A number or a sequence of characters that uniquely identifies the locator within the relevant scope(s). The full identification of the locator could include one or more locator designators. | A number or a sequence of characters which allows a user or an application to interpret, parse and format the locator within the relevant scope. A locator may include more locator designators. | Update from INSPIRE. | Change |
| P4 | **Address.adminUnitL1:** The uppermost administrative unit for the address, almost always a country. | The name or names of a unit of administration where a Member State has and/or exercises jurisdictional rights, for local, regional and national governance. Level 1 refers to the uppermost administrative unit for the address, almost always a country. | Update from INSPIRE. | Change |
| P5 | **Address.adminUnitL2:** The region of the address, usually a county, state or other such area that typically encompasses several localities. | The name or names of a unit of administration where a Member State has and/or exercises jurisdictional rights, for local, regional and national governance. Level 2 referst to the region of the address, usually a county, state or other such area that typically encompasses several localities. | Update from INSPIRE. | Change |

| Nr | Core Business Vocabulary v1.0.0 | Core Business Vocabulary v2.0.0 | Rationale | GitHub / Change |
| --- | --- | --- | --- | --- |
| C1 | **Resource** | **Resource class** added in the diagram | To align with the other distributions, the class resource is now represented visually  | Change |
| C1 | **Change** | **Change class removed** Issue created: https://github.com/SEMICeu/Core-Person-Vocabulary/issues/10 | There should be a discussion on Github about the interest of keeping the Change class. | GitHub |
| C3 | **Licence** | **Licence class removed** Issue created: https://github.com/SEMICeu/Core-Business-Vocabulary/issues/7 | There should be a discussion on Github about the interest of keeping the Change class. And if kept, what properties should it include? | GitHub |
| R1 | **LegalEntity.companyType** | **LegalEntity.companyType** |Is there a need for recommending or listing some controlled vocabularies? If yes, what kind of controlled vocabularies? Existing vocabularies are: (1)[AnaCredit](https://www.ecb.europa.eu/stats/money_credit_banking/anacredit/html/index.en.html) from the European central Bank and one of its [annexes on legal entities per country](https://www.ecb.europa.eu/stats/money/aggregates/anacredit/shared/pdf/List_of_legal_forms.xlsx).  (2)[ISO 20275](https://www.gleif.org/en/about-lei/code-lists/iso-20275-entity-legal-forms-code-list): Entity Legal Forms Code List available in different formats such as [XLS](https://www.gleif.org/content/2-about-lei/7-code-lists/2-iso-20275-entity-legal-forms-code-list/2020-11-19_elf-code-list-v1.3.xlsx). The list also provides names of legal entities per country.| Github |


| Nr | Core Public Organisation Vocabulary v1.0.0 | Core Public Organisation Vocabulary v2.0.0 | Rationale | GitHub / Change |
| --- | --- | --- | --- | --- |
| D1 | **Contact point:** opening hours expects a structured literal value | **Contact point:** opening hours expects a literal value | Structured literal is not an existing data type. | Change |
| D2 | **Public organization:** alternative label expects a literal value | **Public organization:** alternative label expects a text value | Alignment with other Core Vocs. | Change |
| D3 | **Public organization:** description expects a literal value | **Public organization:** description expects a text value | Alignment with other Core Vocs. | Change |
| D4 | **Public organization:** identifier expects a literal (typed) value | **Public organization:** identifier expects a literal value | Alignment with other literal data types. | Change |
| D5 | **Public organization:** preferred label expects a literal value | **Public organization:** preferred label expects a text value | Alignment with other Core Vocs. | Change |
| P1 | **-** | **ChangeEvent.description: added property** | Give some content to the class. | Change |
| P2 | **-** | **ChangeEvent.startedAtTime: added property** | Give some content to the class. | Change |
| P3 | **-** | **ChangeEvent.endedAtTime: added property** | Give some content to the class. | Change |
| D6 | **PublicOrganization.identifier: Literal** | **PublicOrganization.identifier: Identifier** | Alignment with other Core Vocabularies. | Change |
