---
title: CyberGridML Profile
parent: Reference
nav_order: 1
---

# CyberGridML Library Description

CyberGridML provides a modular SysML v2 framework for representing **cyber-physical power systems**.

The library separates:

* Common enumerations and datatypes
* Cyber resources and communication infrastructure
* Electrical grid components
* Control architecture
* Hazard-related metadata

This structure provides a foundation that can be extended to model more detailed electrical, cyber, communication, and control aspects of a power system.

## Overview

CyberGridML is implemented as a [SysML v2 library](https://github.com/cybergridml/cybergrid-modeller/tree/main/CybergridML/src/main/resources/sysml.cybergridML.libraries).

The library combines three main aspects:

The library provides reusable datatypes and enumerations for representing technical properties such as voltage, power, latency, capacity, and energy.

## Library Structure

```text
CyberGridML
├── CyberGridMLEnum
├── CyberGridMLDatatypes
└── CyberGridMLProfile
    ├── CFA
    └── CRA
```

The packages are organized to separate common definitions from the part of the profile that is used to describe power grid architecture and that makes use of the common definitions.

## Package Dependencies

```text
CyberGridMLEnum
       │
       ▼
CyberGridMLDatatypes
       │
       ▼
CyberGridMLProfile
       │
    ┌──┴──┐
    ▼     ▼
   CRA   CFA
```

`CyberGridMLEnum` provides the [enumeration definitions](cybergridml-profile-enum.md) used throughout the library, by the datatypes for instance.

`CyberGridMLDatatypes` provides [reusable technical definitions](cybergridml-profile-datatypes.md) for technical and non-functional properties .

`CyberGridMLProfile` uses these definitions to build the main cyber and physical definitions for the architecture.

It is divided into two packages:
* `CFA` —  [Functional Architecture](cybergridml-profile-cfa.md)
* `CRA` —  [Resource Architecture](cybergridml-profile-cra.md)

## SysML v2 Concepts

CyberGridML uses several standard SysML v2 concepts:

* **Packages** to organize the library
* **Part definitions** to represent system elements
* **Attributes** to represent properties
* **References** to connect model elements
* **Allocations** to represent resource relationships
* **Enumerations** for predefined values
* **Metadata definitions** for additional information
* **Specialization** to create hierarchical definitions




