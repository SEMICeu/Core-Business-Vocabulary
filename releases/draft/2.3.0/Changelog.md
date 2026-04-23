# Core Criterion and Core Evidences Vocabulary Changelog

## Introduction


This document describes the (major) changes to [the current version 2.2.0](https://semiceu.github.io/Core-Business-Vocabulary/releases/2.2.0) of the Core Business Vocabulary for which a new version is being proposed ([version 2.3.0](https://semiceu.github.io/uri.semic.eu-generated/Core-Business-Vocabulary/releases/draft/2.3.0/)). The list of changes results in the new version to be considered as a minor release.

## Detailed changes from v2.2.0 to v2.X.X
The table below gives an overview of the classes (and their definitions) within both data models. Classes that are related are juxta-positioned.

**C** stands for changes in classes

**R** stands for changes in relationships

**P** stands for changes in properties

**D** stands for changes in data types

| Nr | CBV v2.2.0 | CBV v2.X.X | Rationale | GitHub / Change |
| -- | ------------ | ------------ | --------- | --------------- |
| C1  | - |cv:LegalStatus | Introduction LegalStatus class to facilitate reporting conform to HVD regulations | [#45](https://github.com/SEMICeu/Core-Business-Vocabulary/issues/45) |
| P1  | - | cv:legalEntityStatus & cv:legalStatusDate | Introduction legalEntityStatus and legalStatusDate properties to provide the legal status of the entity on a given date|[#45](https://github.com/SEMICeu/Core-Business-Vocabulary/issues/45) |
| P2  | skos:prefLabel | rdfs:label | Provide ability to assign human readable labels to class instances and align approach to SEMIC Style Guide. | [#57](https://github.com/SEMICeu/CCCEV/issues/57) |
| -  | - | - | Editorial changes have been applied to the specification to fix typo's. | [#42](https://github.com/SEMICeu/Core-Location-Vocabulary/issues/42) |
| C2  | - |adms:IdentifierScheme | Alignment with Uncecfact Transparency Protocol | [#50](https://github.com/SEMICeu/Core-Business-Vocabulary/issues/50) |
