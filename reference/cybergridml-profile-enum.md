---
title: CyberGridML Enumerations
parent: Reference
nav_order: 2
---

# CyberGridMLEnum

The `CyberGridMLEnum` package contains the enumeration definitions used throughout the library. An enumeration is a specialized data type that restricts the possible values of a property to a fixed, named set of constant literals. For instance, it is used to define units. These definitions are reused to define structured [datatypes](cybergridml-profile-datatypes.md).

## Electrical Units

The library defines enumerations for the core electrical units of measurement.

### Voltage 
Voltage can be expressed according to the possible values of the `VoltageUnitKind` enumeration: `V` (Volt), `KV` (KiloVolt), or `MV` (MegaVolt).

### Power
Power (P) can be expressed according to the possible values of the `PowerUnitKind` enumeration: `W` (Watt), `KW` (KiloWatt), or `MW` (MegaWatt).

### Reactive Power
Reactive power (Q) is the oscillating electrical energy that builds and collapses magnetic or electric fields in alternating current (AC) loads. Unlike (active) power, reactive power does not perform direct mechanical or thermal work. It is required to establish fields in devices like induction motors and transformers, and it helps maintain AC voltage levels across the electrical grid. In CyberGridML, reactive power can be expressed according to the possible values of the `ReactivePowerUnitKind` enumeration: `VAR` (volt-ampere reactive), `KVAR` (KiloVAR), or `MVAR` (MegaVAR).

### Energy
Energy can be expressed according to the possible values of the `EnergyUnitKind` enumeration: `J` (Joule), `KJ` (KiloJoule), `Wh` (Watt-hour), `KWh` (KiloWatt-hour), or `MWh` (MegaWatt-hour).

### Current
Current can be expressed according to the possible values of the `CurrentUnitKind`: `A` (Ampere) or `MA` (MegaAmpere).


## Communication and Time Units

The library defines enumerations for time-related units and for specifying the characteristics of communication devices.

### Time Units

Time can be expressed according to the possible values of the `TimeUnitKind` enumeration: `s` (seconds), `ms`(milliseconds), `us` (microseconds), `min` (minutes), `hrs` (hours), `day`(days), or `tick` (ticks).

### Latency
Latency can be expressed according to the possible values of `LatencyUnitKind`: `Nanoseconds` (nanoseconds), `Microseconds` (microseconds), `Milliseconds` (milliseconds); `Seconds` (seconds), or `Minutes` (minutes).

### Capacity
Capacity can be expressed according to the possible values of `CapacityUnitKind`: `Bytes`, `Kilobytes`, `Megabytes`, `Gigabytes`, `Terabytes`, or `Petabytes`.


## Other

### Voltage levels
`VoltageLevel` defines the supported grid voltage levels : `20`, `42`, `63`, `90`, `150`, `225`, and `380`.  

### Redundancy
`RedundancyKind` defines various redundancy mechanisms: `consensus`, `hypervisor` and `active_standby`.

### Control
`ControlType` defines various control modes available in the library, such as `DefaultControl`, `Limiter`, `ApproximateLinearMPC` and `ReleaseAll`.

