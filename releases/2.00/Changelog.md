# Core Business Changelog

## Introduction

This document describes the (major) changes to [the current version 1.0.0](https://github.com/SEMICeu/Core-Business-Vocabulary/tree/master/releases/1.00) of the Core Business Vocabulary for which a new version is being proposed ([version 2.0.0](https://semiceu.github.io/Core-Business-Vocabulary/releases/2.00/)). The list of changes results in the new version to be considered as a major release.

## Detailed changes from v1.0.0 to v2.0.0

The table below gives an overview of the classes (and their definitions) within both data models. Classes that are related are juxta-positioned.

**C** stands for changes in classes

**R** stands for changes in relationships

**P** stands for changes in properties

**D** stands for changes in data types

| Nr | Core Business Vocabulary v1.0.0 | Core Business Vocabulary v2.0.0 | Rationale | GitHub / Change |
| --- | --- | --- | --- | --- |
| C1 | **Resource** | **Resource class** added in the diagram | To align with the other distributions, the class resource is now represented visually  | Change |
| C1 | **Change** | **Change class removed** Issue created: https://github.com/SEMICeu/Core-Person-Vocabulary/issues/10 | There should be a discussion on Github about the interest of keeping the Change class. | GitHub |
| C3 | **Licence** | **Licence class removed** Issue created: https://github.com/SEMICeu/Core-Business-Vocabulary/issues/7 | There should be a discussion on Github about the interest of keeping the Licence class. And if kept, what properties should it include? | GitHub |
| R1 | **LegalEntity.companyType** | **LegalEntity.companyType** |Is there a need for recommending or listing some controlled vocabularies? If yes, what kind of controlled vocabularies? Existing vocabularies are: (1)[AnaCredit](https://www.ecb.europa.eu/stats/money_credit_banking/anacredit/html/index.en.html) from the European central Bank and one of its [annexes on legal entities per country](https://www.ecb.europa.eu/stats/money/aggregates/anacredit/shared/pdf/List_of_legal_forms.xlsx).  (2)[ISO 20275](https://www.gleif.org/en/about-lei/code-lists/iso-20275-entity-legal-forms-code-list): Entity Legal Forms Code List available in different formats such as [XLS](https://www.gleif.org/content/2-about-lei/7-code-lists/2-iso-20275-entity-legal-forms-code-list/2020-11-19_elf-code-list-v1.3.xlsx). The list also provides names of legal entities per country.| Github |

## Changes since April 2021 

### Terms

| Nr | Core Business Vocabulary v2.0.0 2021 | Core Business Vocabulary v2.0.0 2022                                | Rationale                                           | GitHub/Change                                                                                                                  |
| -- | ------------------------------------ | ------------------------------------------------------------------- | --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| C1 | Resource                             | \-                                                                  | deleted as legalEntity relation has been deprecated |                                                                                                                                |
| C2 | Concept                              | \-                                                                  | made it implicit                                    |                                                                                                                                |
| R1 | Resource.legalEntity:LegalEntity     | \-                                                                  | the relation has been deprecated                    | [https://github.com/SEMICeu/Core-Business-Vocabulary/issues/13](https://github.com/SEMICeu/Core-Business-Vocabulary/issues/13) |
| R2 | LegalEntity.companyActivity:Concept  | LegalEntity.legalEntityActivity:Code                                | renamed company in legalEntity                      | [https://github.com/SEMICeu/Core-Business-Vocabulary/issues/10](https://github.com/SEMICeu/Core-Business-Vocabulary/issues/10) |
| R3 | LegalEntity.companyStatus:Concept    | LegalEntity.legalEntityStatus:Code                                  | renamed company in legalEntity                      |                                                                                                                                |
| R4 | LegalEntity.companyType:Concept      | LegalEntity.legalFormType:Code                                      | renamed company in legalEntity                      | [https://github.com/SEMICeu/Core-Business-Vocabulary/issues/11](https://github.com/SEMICeu/Core-Business-Vocabulary/issues/11) |
| P4 | \-                                   | Identifier.schemeName                                               | Identifiers can be detailed                         |                                                                                                                                |
| P5 | Identifier.issuingAuthority          | Identifier.issuingAuthorityName                                     | Better property readability                         | [https://github.com/SEMICeu/Core-Person-Vocabulary/issues/14](https://github.com/SEMICeu/Core-Person-Vocabulary/issues/14)     |
| P6 | Identifier.identifier                | Identifier.notation                                                 | to better distinguish it from the identifier itself |                                                                                                                                |
| P7 | Identifier.issuingAuthorityURI       | Identifier.issuingAuthorityURI:Identifier.issuingAuthorityURI:Agent | made it explicit relation toward Agent              |                                                                                                                                |
| D1 | Identifier.dateOfIssue:DateTime      | Identifier.dateOfIssue:Date                                         | the property is more generic                        |                                                                                                                                |
| D2 | Address:AdminUnitL1:Code             | Address:AdminUnitL1:Text                                            | In compliance with W3C location                     |                                                                                                                                |
| D3 | Address:AdminUnitL2:Code             | Address:AdminUnitL1:Text                                            | In compliance with W3C location                     |

### Definitions

Changes in definitions are registered in [this file](Changelog_definitions.md)