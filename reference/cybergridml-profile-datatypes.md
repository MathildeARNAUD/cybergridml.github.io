---
title: CyberGridML Datatypes
parent: Reference
nav_order: 3
---

# CyberGridMLDatatypes

The `CyberGridMLDatatypes` package provides reusable definitions for technical and non-functional properties.

## Non-Functional Properties

The library defines several non-functional properties through `NFP` types:

| Type                | Description                       |
| ------------------- | --------------------------------- |
| `NFP_Latency`       | Communication latency             |
| `NFP_Capacity`      | Communication or storage capacity |
| `NFP_Voltage`       | Electrical voltage                |
| `NFP_Power`         | Active power                      |
| `NFP_Energy`        | Energy                            |
| `NFP_Current`       | Electrical current                |
| `NFP_ReactivePower` | Reactive power                    |

Each such property generally contains a **unit** and a **value/precision** attribute.

For example:

```text
NFP_Voltage
├── unit
└── precision
```

These types are reused by the physical and cyber architectures.

## Period

`Period` represents a time interval using a start and finish value.

```text
Period
├── start
└── finish
```

It can be used, for example, to describe software activation periods and execution delays.

## Hazard

`Hazard` is a metadata definition used to attach hazard-related information to model elements.

It contains:

* `description`
* `justification`
* `period`
* `percent`

This provides a way to associate additional safety or risk-related information with the model.

