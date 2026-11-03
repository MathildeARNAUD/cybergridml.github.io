---
title: CyberGridML Resources Architecture
parent: Reference
nav_order: 5
---
The `CyberGridMLProfile` contains the main architectural definitions.

It is divided into two packages:

* `CRA` —  Resource Architecture
* `CFA` —  Functional Architecture

## CRA — Control Resource Architecture

The `CRA` package represents the **infrastructure** of the system.

### ComputingResource

`ComputingResource` represents a computational platform capable of hosting software resources.

### SoftwareResource

`SoftwareResource` represents a software component running on a computing resource.

It is equipped with properties to describe when a software component is activated :

* `Activation_period`
* `Execution_delay`



### RedundancyCluster

`RedundancyCluster` represents a set of redundant software resources.

It defines:

* An associated redundancy mechanism through `runtime`
* One or more active software resources
* One or more passive software resources
* An optional hypervisor

```text
RedundancyCluster
├── runtime
├── active
├── passive
└── hypervisor
```



### CommunicationMedia

`CommunicationMedia` represents a communication between resources.

It provides two main properties:

* `capacity`
* `latency`

Both properties use the reusable datatypes defined in `CyberGridMLDatatypes`.

### CRA Relationships

Three allocation/connection relationships are defined:

`Allocate` connects a `ComputingResource` with a `SoftwareResource`.

`Connect` connects a `ComputingResource` with a `CommunicationMedia`.

`Link` connects two `CommunicationMedia` elements.

Together, these relationships can be used to describe how software is deployed and how resources communicate.





