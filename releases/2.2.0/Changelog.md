# Core Business Changelog

## Introduction

This document describes the (major) changes to [the current version 2.1.0](https://semiceu.github.io/Core-Business-Vocabulary/releases/2.1.0/) of the Core Business Vocabulary for which a new version is being proposed ([version 2.2.0](https://semiceu.github.io/Core-Business-Vocabulary/releases/2.2.0/)). The list of changes results in the new version to be considered as a minor release.

All of the changes were discussed and approved during the [webinar](https://joinup.ec.europa.eu/collection/semic-support-centre/event/webinar-review-core-vocabularies) of 27/10/2023.

## Changes from v2.1.0 to v2.2.0 
The table below gives an overview of the classes (and their definitions) within both data models. Classes that are related are juxta-positioned.

**C** stands for changes in classes

**R** stands for changes in relationships

**P** stands for changes in properties

**D** stands for changes in data types

### Terms
| Nr | Core Business Vocabulary v2.1.0 | Core Business Vocabulary v2.2.0 | Rationale                                | GitHub/Change                                                                                                                              |
| -- | ------------------------------- | ------------------------------- | ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| - | - | ReSpec Styling has been applied to the specification.| - | - |
| - | - |Explicit exlusions of sole traders have been removed| This change allows users to decide what type of organisations are within scope of their implementations. | [#26](https://github.com/SEMICeu/Core-Business-Vocabulary/issues/26), [#24](https://github.com/SEMICeu/Core-Business-Vocabulary/issues/24) |
| P1 | \-                              | LegalFormType                   | Add property to include more types of LegalEntity. As input the code list of GLEIF can be used which can be appended upon request with national legal entities. | [#26](https://github.com/SEMICeu/Core-Business-Vocabulary/issues/26), [#24](https://github.com/SEMICeu/Core-Business-Vocabulary/issues/24) |
