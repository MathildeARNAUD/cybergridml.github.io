---
title: CyberGridML Functional Architecture
parent: Reference
nav_order: 4
---

The `CyberGridMLProfile` contains the main architectural definitions.

It is divided into two packages:

* `CRA` —  Resource Architecture
* `CFA` —  Functional Architecture


# CFA — Functional Architecture

The `CFA` package represents the **electrical grid and its control system**.

## GridElement

`GridElement` is the base definition for grid-related elements.

Other elements can specialize this definition.

## MainGrid

`MainGrid` represents the overall electrical grid.

It contains elements representing the components of the physical electrical grid : substations and power lines, as well as the central controller in charge of the function of control of the main grid, and zones which have a logical role of gathering selected substations for targeted control.

* Substations
* Zones
* Lines
* CentralController

```text
MainGrid
├── Substation
├── Zone
├── Line
└── CentralController
```

## Zone

`Zone` represents a section of the main grid.

A zone contains:

* A zonal controller
* One or more substations
* Lines

`Zone` also specializes `GridElement`.

## Substation

`Substation` represents an electrical substation.

It contains one or more buses and can reference one or more zones.

## Bus

`Bus` represents an electrical bus inside a substation.

It defines:

* `nominalLevel` — nominal voltage
* `connected` — connection status
* `equipments` — equipment connected to the bus
* `substation` — associated substation

## Equipment

`Equipment` is the base definition for electrical equipment.

It provides common properties such as:

* `connected`
* `p` — active power
* `q` — reactive power
* `activable`
* `localController`

Three specialized equipment types are defined:

```text
Equipment
├── Generator
├── Battery
└── Load
```

`Generator` represents a power generation unit.

`Battery` represents an energy storage device.

`Load` represents an electrical consumption unit.

## Controllers

The library defines a hierarchy of controllers.

```text
Controller
├── CentralController
├── ZonalController
└── LocalController
```

`Controller` provides the common `controlBehavior` property.

`CentralController` is associated with the `MainGrid`.

`ZonalController` is associated with a `Zone`.

`LocalController` is used at the equipment level.

## Line

`Line` represents an electrical line in the grid.

A line references:

* Its main grid
* One or two terminals

## Terminal

`Terminal` represents an endpoint of a line.

It specializes `Equipment` and provides electrical and structural information such as:

* `finish`
* `branch`
* `side`
* `ecr` — current
* `v` — voltage

A terminal also references its associated line.

## Control

`Control` represents a relationship between a grid element and a controller.

```text
GridElement ───── Control ───── Controller
```

This relationship allows the control architecture to be connected to the physical grid model.

