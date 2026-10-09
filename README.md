# esmf-examples

This repository contains example models written in [Semantic Aspect Meta Model
(SAMM)](https://eclipse-esmf.github.io/samm-specification/snapshot/index.html).

The examples are built around the notion of a digital twin for a machine in a
production line. The models are organized into separate namespaces, each
representing one aspect of the information for this digital twin. At the same
time, each model demonstrates the use of various SAMM features. The following
sections describe the models and which modeling features they demonstrate.

## org.eclipse.examples.asset_master_data

Contents:
```
org.eclipse.esmf.examples.asset_master_data/
├── 1.0.0
│   └── AssetMasterData.ttl
├── 1.0.1
│   └── AssetMasterData.ttl
└── 1.0.2
    └── AssetMasterData.ttl
```

* [AssetMasterData
  1.0.0](aspect-models/org.eclipse.esmf.examples.asset_master_data/1.0.0/AssetMasterData.ttl)
  demonstrates the basic structure of an Aspect Model. It defines a single
  Aspect and two Properties. It shows how to use built-in Characteristic
  instances such as `samm-c:Text` and how to instantiate Characteristic classes
  such as `samm-c:Code`. It also shows how to attach `samm:preferredName` and
  `samm:description` attributes to model elements.

* [AssetMasterData 1.0.1](aspect-models/org.eclipse.esmf.examples.asset_master_data/1.0.1/AssetMasterData.ttl) builds on version 1.0.0 and shows how Property names can
  be renamed without breaking the runtime data structure that is defined by the
  Aspect Model, by using `samm:payloadName`.

* [AssetMasterData 1.0.2](aspect-models/org.eclipse.esmf.examples.asset_master_data/1.0.2/AssetMasterData.ttl) builds on version 1.0.1 and additionally demonstrates
  how to provide descriptions in multiple languages, both for the model elements
  and for the runtime data.

## org.eclipse.examples.machine_online_status

Contents:
```
org.eclipse.esmf.examples.machine_online_status/
├── 1.0.0
│   └── MachineOnlineStatus.ttl
├── 1.0.1
│   └── MachineOnlineStatus.ttl
├── 1.0.2
│   └── MachineOnlineStatus.ttl
├── 1.0.3
│   └── MachineOnlineStatus.ttl
└── 1.1.0
    └── MachineOnlineStatus.ttl
```

This namespace contains the MachineOnlineStatus Aspect in multiple versions,
that demonstrates how the evolution of a model across multiple versions can take
place. The idea of the model and the evolution process is explained in more
detail in the section [Model
Evolution](https://eclipse-esmf.github.io/samm-specification/snapshot/appendix/model-evolution.html)
of the SAMM specification appendix.

Between [MachineOnlineStatus
1.0.0](aspect-models/org.eclipse.esmf.examples.machine_online_status/1.0.0/MachineOnlineStatus.ttl)
to
[1.0.3](aspect-models/org.eclipse.esmf.examples.machine_online_status/1.0.3/MachineOnlineStatus.ttl)
certain changes are introduced and explained in the comments of the respective
files. [MachineOnlineStatus 1.1.0](aspect-models/org.eclipse.esmf.examples.machine_online_status/1.1.0/MachineOnlineStatus.ttl) demonstrates the use of a `samm:Operation`.

## org.eclipse.examples.machine_technical_specifications

Contents:
```
org.eclipse.esmf.examples.machine_technical_specifications/
├── 1.0.0
│   └── MachineTechnicalSpecifications.ttl
└── 1.0.1
    └── MachineTechnicalSpecifications.ttl
```

* [MachineTechnicalSpecifications 1.0.0](aspect-models/org.eclipse.esmf.examples.machine_technical_specifications/1.0.0/MachineTechnicalSpecifications.ttl) demonstrates how to combine multiple
  Properties into Entities and use these Entities as types. It also shows how to
  share Characteristics for multiple Properties. It makes use of the
  `samm-c:Quantifiable` Characteristic and shows how to relate physical units
  with numeric Properties. Furthermore, it demonstrates how to use `samm:see` to
  relate a model element with a concept defined external to the model.

* [MachineTechnicalSpecifications 1.0.1](aspect-models/org.eclipse.esmf.examples.machine_technical_specifications/1.0.1/MachineTechnicalSpecifications.ttl) builds on version 1.0.0 and demonstrates
  how `samm-c:Trait` and Constraints are used to express restrictions on values.

## org.eclipse.examples.machine_temperature

Contents:
```
org.eclipse.esmf.examples.machine_temperature/
└── 1.0.0
    ├── _dependencies.ttl
    ├── MachineTemperatureHistory.ttl
    └── MachineTemperature.ttl
```

This namespace demonstrates how to share model elements between multiple Aspect
Models. [MachineTemperature
1.0.0](aspect-models/org.eclipse.esmf.examples.machine_temperature/1.0.0/MachineTemperature.ttl)
is a simple Aspect that provides the current temperature of the machine as a
measurement value. The corresponding historic data Aspect,
[MachineTemperatureHistory
1.0.0](aspect-models/org.eclipse.esmf.examples.machine_temperature/1.0.0/MachineTemperature.ttl),
represents the history of machine temperatures as a time series. This is Aspect
is a so-called [Collection
Aspect](https://eclipse-esmf.github.io/samm-specification/snapshot/appendix/best-practices.html#if-certain-characteristics-are-present).
Both Aspects use the shared Temperature Characteristic from
[_dependencies.ttl](aspect-models/org.eclipse.esmf.examples.machine_temperature/1.0.0/_dependencies.ttl).

## org.eclipse.examples.movement

Contents:
```
org.eclipse.esmf.examples.movement
└── 1.0.0
    └── Movement.ttl
```

The simple self-contained example model that is also bundled with the [Aspect Model Editor](https://eclipse-esmf.github.io/ame-guide/introduction.html).
