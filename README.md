Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# AAS Production Submodel (PROD)

**Development branch `dev` created as starting point for project tasks.**

## Metadata
* **IRI**
  * `https://rub-informatik-im-bauwesen.github.io/prod`
* **Creators(s)**
  * [Philipp Hagedorn](https://orcid.org/0000-0002-6249-243X)
    [[ORCID]](https://orcid.org/0000-0002-6249-243X)
    (<philipp.hagedorn-n6v@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
  * [Simon Kosse](https://orcid.org/0000-0002-6391-784X)
    [[ORCID]](https://orcid.org/0000-0002-6391-784X)
    (<simon.kosse@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/simon_kosse.html.en)
* **Created**
  * 2024-02-01
* **Version Information**
  * 1.0
* **Imports**
  * [aas:](https://admin-shell.io/aas/3/0/)
* **License &amp; Rights**
  * [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
  * &copy; 2024 by Chair of Computing in Engineering, Ruhr University Bochum
* **Source**
  * [https://github.com/RUB-Informatik-im-Bauwesen/prod](https://github.com/RUB-Informatik-im-Bauwesen/prod)
* **Ontology RDF**
  * RDF ([.\ProductionSubmodel.ttl](turtle))
### Description
<p>The Production Submodel (PROD) for the Asset Administration Shell (AAS) is defined for providing information about the submodel for industrialized precast concrete production. The submodel is aligned with the relevant terminology of the AAS data model according to the specification version v3.0 at https://admin-shell.io/aas/3/0/</p>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Overview

![Overview](Figure_Prod_Encoded.svg)
**Figure 1:** Ontology overview
## Classes
[Buffer](#Buffer),
[ConcretingProcess](#ConcretingProcess),
[ConcretingStation](#ConcretingStation),
[CuringProcess](#CuringProcess),
[CuringStation](#CuringStation),
[FormworkProcess](#FormworkProcess),
[FormworkStation](#FormworkStation),
[Order](#Order),
[PrecastElement](#PrecastElement),
[ProductionProcess](#ProductionProcess),
[ProductionStation](#ProductionStation),
[ProductionSubmodel](#ProductionSubmodel),
[ProductionSystem](#ProductionSystem),
[ProductionUnit](#ProductionUnit),
[ReinforcementProcess](#ReinforcementProcess),
[ReinforcementStation](#ReinforcementStation),
[StrippingProcess](#StrippingProcess),
[StrippingStation](#StrippingStation),
### Buffer
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#Buffer`
Super-classes |[prod:ProductionStation](ProductionStation) (c)<br />
Restrictions |[prod:bufferSize](bufferSize) (dp) **min** 1<br />
In range of |[prod:hasBuffer](hasBuffer) (op)<br />
### ConcretingProcess
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#ConcretingProcess`
Super-classes |[prod:ProductionProcess](ProductionProcess) (c)<br />
### ConcretingStation
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#ConcretingStation`
Super-classes |[prod:ProductionStation](ProductionStation) (c)<br />
### CuringProcess
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#CuringProcess`
Super-classes |[prod:ProductionProcess](ProductionProcess) (c)<br />
### CuringStation
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#CuringStation`
Super-classes |[prod:ProductionStation](ProductionStation) (c)<br />
### FormworkProcess
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#FormworkProcess`
Super-classes |[prod:ProductionProcess](ProductionProcess) (c)<br />
### FormworkStation
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#FormworkStation`
Super-classes |[prod:ProductionStation](ProductionStation) (c)<br />
### Order
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#Order`
Super-classes |[aas:SubmodelElementCollection](https://admin-shell.io/aas/3/0/SubmodelElementCollection) (c)<br />
Restrictions |[prod:isProducedBy](isProducedBy) (op) **some** [prod:ProductionUnit](ProductionUnit) (c)<br />[prod:dueDate](dueDate) (dp) **exactly** 1<br />[prod:expectedDeliveryDate](expectedDeliveryDate) (dp) **exactly** 1<br />[prod:orderID](orderID) (dp) **exactly** 1<br />[prod:hasItem](hasItem) (op) **some** [prod:PrecastElement](PrecastElement) (c)<br />[prod:isPartOf](isPartOf) (op) **some** [prod:ProductionSystem](ProductionSystem) (c)<br />
In domain of |[prod:hasItem](hasItem) (op)<br />[prod:dueDate](dueDate) (dp)<br />[prod:isProducedBy](isProducedBy) (op)<br />[prod:expectedDeliveryDate](expectedDeliveryDate) (dp)<br />[prod:orderID](orderID) (dp)<br />
In range of |[prod:produces](produces) (op)<br />[prod:isItemOf](isItemOf) (op)<br />
### PrecastElement
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#PrecastElement`
Super-classes |[aas:SubmodelElementCollection](https://admin-shell.io/aas/3/0/SubmodelElementCollection) (c)<br />
Restrictions |[prod:quantity](quantity) (dp) **exactly** 1<br />[prod:componentType](componentType) (dp) **exactly** 1<br />[prod:precastElementAAS](precastElementAAS) (op) **exactly** 1 [aas:AssetAdministrationShell](https://admin-shell.io/aas/3/0/AssetAdministrationShell) (c)<br />[prod:isProducedBy](isProducedBy) (op) **some** [prod:ProductionProcess](ProductionProcess) (c)<br />[prod:isItemOf](isItemOf) (op) **some** [prod:Order](Order) (c)<br />[prod:isProducedBy](isProducedBy) (op) **exactly** 1 [prod:ProductionUnit](ProductionUnit) (c)<br />
In domain of |[prod:quantity](quantity) (dp)<br />[prod:isItemOf](isItemOf) (op)<br />[prod:isProducedBy](isProducedBy) (op)<br />[prod:componentType](componentType) (dp)<br />[prod:precastElementAAS](precastElementAAS) (op)<br />
In range of |[prod:hasItem](hasItem) (op)<br />[prod:produces](produces) (op)<br />
### ProductionProcess
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#ProductionProcess`
Super-classes |[aas:SubmodelElementCollection](https://admin-shell.io/aas/3/0/SubmodelElementCollection) (c)<br />
Restrictions |[prod:expectedDuration](expectedDuration) (dp) **exactly** 1<br />[prod:expectedStartTime](expectedStartTime) (dp) **exactly** 1<br />[prod:isExecutedBy](isExecutedBy) (op) **exactly** 1 [prod:ProductionStation](ProductionStation) (c)<br />[prod:startTime](startTime) (dp) **exactly** 1<br />[prod:canBeExecutedBy](canBeExecutedBy) (op) **min** 1 [prod:ProductionStation](ProductionStation) (c)<br />[prod:produces](produces) (op) **some** [prod:PrecastElement](PrecastElement) (c)<br />[prod:endTime](endTime) (dp) **exactly** 1<br />[prod:sequencePosition](sequencePosition) (dp) **exactly** 1<br />
Sub-classes |[prod:ConcretingProcess](ConcretingProcess) (c)<br />[prod:CuringProcess](CuringProcess) (c)<br />[prod:FormworkProcess](FormworkProcess) (c)<br />[prod:StrippingProcess](StrippingProcess) (c)<br />[prod:ReinforcementProcess](ReinforcementProcess) (c)<br />
In domain of |[prod:endTime](endTime) (dp)<br />[prod:expectedStartTime](expectedStartTime) (dp)<br />[prod:bufferSize](bufferSize) (dp)<br />[prod:isExecutedBy](isExecutedBy) (op)<br />[prod:expectedDuration](expectedDuration) (dp)<br />[prod:canBeExecutedBy](canBeExecutedBy) (op)<br />[prod:sequencePosition](sequencePosition) (dp)<br />[prod:produces](produces) (op)<br />[prod:startTime](startTime) (dp)<br />
In range of |[prod:isProducedBy](isProducedBy) (op)<br />
### ProductionStation
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#ProductionStation`
Super-classes |[aas:SubmodelElementCollection](https://admin-shell.io/aas/3/0/SubmodelElementCollection) (c)<br />
Restrictions |[prod:hasBuffer](hasBuffer) (op) **some** [prod:Buffer](Buffer) (c)<br />[prod:prodStationAAS](prodStationAAS) (op) **exactly** 1 [aas:AssetAdministrationShell](https://admin-shell.io/aas/3/0/AssetAdministrationShell) (c)<br />[prod:isPartOf](isPartOf) (op) **some** [prod:ProductionUnit](ProductionUnit) (c)<br />
Sub-classes |[prod:CuringStation](CuringStation) (c)<br />[prod:Buffer](Buffer) (c)<br />[prod:ConcretingStation](ConcretingStation) (c)<br />[prod:FormworkStation](FormworkStation) (c)<br />[prod:ReinforcementStation](ReinforcementStation) (c)<br />[prod:StrippingStation](StrippingStation) (c)<br />
In domain of |[prod:hasBuffer](hasBuffer) (op)<br />[prod:prodStationAAS](prodStationAAS) (op)<br />
In range of |[prod:isExecutedBy](isExecutedBy) (op)<br />[prod:canBeExecutedBy](canBeExecutedBy) (op)<br />
### ProductionSubmodel
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#ProductionSubmodel`
Super-classes |[aas:Submodel](https://admin-shell.io/aas/3/0/Submodel) (c)<br />
Restrictions |[prod:consistsOf](consistsOf) (op) **some** [prod:ProductionSystem](ProductionSystem) (c)<br />
### ProductionSystem
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#ProductionSystem`
Super-classes |[aas:SubmodelElementCollection](https://admin-shell.io/aas/3/0/SubmodelElementCollection) (c)<br />
Restrictions |[prod:consistsOf](consistsOf) (op) **some** [prod:ProductionUnit](ProductionUnit) (c)<br />[prod:produces](produces) (op) **some** [prod:Order](Order) (c)<br />
In domain of |[prod:produces](produces) (op)<br />
In range of |[prod:isProducedBy](isProducedBy) (op)<br />
### ProductionUnit
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#ProductionUnit`
Super-classes |[aas:SubmodelElementCollection](https://admin-shell.io/aas/3/0/SubmodelElementCollection) (c)<br />
Restrictions |[prod:isPartOf](isPartOf) (op) **some** [prod:ProductionSystem](ProductionSystem) (c)<br />[prod:consistsOf](consistsOf) (op) **some** [prod:ProductionStation](ProductionStation) (c)<br />
In domain of |[prod:produces](produces) (op)<br />
In range of |[prod:isProducedBy](isProducedBy) (op)<br />
### ReinforcementProcess
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#ReinforcementProcess`
Super-classes |[prod:ProductionProcess](ProductionProcess) (c)<br />
### ReinforcementStation
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#ReinforcementStation`
Super-classes |[prod:ProductionStation](ProductionStation) (c)<br />
### StrippingProcess
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#StrippingProcess`
Super-classes |[prod:ProductionProcess](ProductionProcess) (c)<br />
### StrippingStation
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#StrippingStation`
Super-classes |[prod:ProductionStation](ProductionStation) (c)<br />

## Object Properties
[canBeExecutedBy](#canBeExecutedBy),
[consistsOf](#consistsOf),
[hasBuffer](#hasBuffer),
[hasItem](#hasItem),
[isExecutedBy](#isExecutedBy),
[isItemOf](#isItemOf),
[isPartOf](#isPartOf),
[isProducedBy](#isProducedBy),
[precastElementAAS](#precastElementAAS),
[prodStationAAS](#prodStationAAS),
[produces](#produces),
[](canBeExecutedBy)
### canBeExecutedBy
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#canBeExecutedBy`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[prod:ProductionProcess](ProductionProcess) (c)<br />
Range(s) |[prod:ProductionStation](ProductionStation) (c)<br />
[](consistsOf)
### consistsOf
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#consistsOf`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](hasBuffer)
### hasBuffer
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#hasBuffer`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[prod:ProductionStation](ProductionStation) (c)<br />
Range(s) |[prod:Buffer](Buffer) (c)<br />
[](hasItem)
### hasItem
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#hasItem`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[prod:Order](Order) (c)<br />
Range(s) |[prod:PrecastElement](PrecastElement) (c)<br />
[](isExecutedBy)
### isExecutedBy
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#isExecutedBy`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[prod:ProductionProcess](ProductionProcess) (c)<br />
Range(s) |[prod:ProductionStation](ProductionStation) (c)<br />
[](isItemOf)
### isItemOf
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#isItemOf`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[prod:PrecastElement](PrecastElement) (c)<br />
Range(s) |[prod:Order](Order) (c)<br />
[](isPartOf)
### isPartOf
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#isPartOf`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](isProducedBy)
### isProducedBy
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#isProducedBy`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[prod:Order](Order) (c)<br />[prod:PrecastElement](PrecastElement) (c)<br />
Range(s) |[prod:ProductionUnit](ProductionUnit) (c)<br />[prod:ProductionProcess](ProductionProcess) (c)<br />[prod:ProductionSystem](ProductionSystem) (c)<br />
[](precastElementAAS)
### precastElementAAS
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#precastElementAAS`
Description | Reference to external AAS of a precast concrete element.
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[prod:PrecastElement](PrecastElement) (c)<br />
Range(s) |[aas:AssetAdministrationShell](https://admin-shell.io/aas/3/0/AssetAdministrationShell) (c)<br />
[](prodStationAAS)
### prodStationAAS
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#prodStationAAS`
Description | Reference to external AAS of a production station.
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[prod:ProductionStation](ProductionStation) (c)<br />
Range(s) |[aas:AssetAdministrationShell](https://admin-shell.io/aas/3/0/AssetAdministrationShell) (c)<br />
[](produces)
### produces
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#produces`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[prod:ProductionProcess](ProductionProcess) (c)<br />[prod:ProductionSystem](ProductionSystem) (c)<br />[prod:ProductionUnit](ProductionUnit) (c)<br />
Range(s) |[prod:Order](Order) (c)<br />[prod:PrecastElement](PrecastElement) (c)<br />

## Datatype Properties
[bufferSize](#bufferSize),
[componentType](#componentType),
[dueDate](#dueDate),
[endTime](#endTime),
[expectedDeliveryDate](#expectedDeliveryDate),
[expectedDuration](#expectedDuration),
[expectedStartTime](#expectedStartTime),
[orderID](#orderID),
[quantity](#quantity),
[sequencePosition](#sequencePosition),
[startTime](#startTime),
[](bufferSize)
### bufferSize
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#bufferSize`
Description | Number of components that can be temporarily stored before being processed or transferred.
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[prod:ProductionProcess](ProductionProcess) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](componentType)
### componentType
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#componentType`
Description | Specific category or type of a precast concrete component or element.
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[prod:PrecastElement](PrecastElement) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](dueDate)
### dueDate
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#dueDate`
Description | Deadline or the date by which a production job is expected to be completed.
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[prod:Order](Order) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](endTime)
### endTime
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#endTime`
Description | Time at which a particular task, event, or activity is completed or finished.
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[prod:ProductionProcess](ProductionProcess) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](expectedDeliveryDate)
### expectedDeliveryDate
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#expectedDeliveryDate`
Description | Date on which precast modules are to be delivered to the construction site for installation as part of a building or infrastructure project.
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[prod:Order](Order) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](expectedDuration)
### expectedDuration
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#expectedDuration`
Description | Estimated or anticipated length of time it will take to complete a task, project, or activity.
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[prod:ProductionProcess](ProductionProcess) (c)<br />
Range(s) |[xsd:double](http://www.w3.org/2001/XMLSchema#double) (c)<br />
[](expectedStartTime)
### expectedStartTime
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#expectedStartTime`
Description | Designated or scheduled time at which a particular task, event, or activity is expected to begin.
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[prod:ProductionProcess](ProductionProcess) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](orderID)
### orderID
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#orderID`
Description | Unique identifier assigned to a specific job or task in a production system, allowing it to be tracked and managed.
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[prod:Order](Order) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](quantity)
### quantity
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#quantity`
Description | Number or quantity of a specific component needed or required for a particular project or product.
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[prod:PrecastElement](PrecastElement) (c)<br />
Range(s) |[xsd:positiveInteger](http://www.w3.org/2001/XMLSchema#positiveInteger) (c)<br />
[](sequencePosition)
### sequencePosition
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#sequencePosition`
Description | Specific location or order of a task or activity within a larger sequence or series of tasks.
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[prod:ProductionProcess](ProductionProcess) (c)<br />
Range(s) |[xsd:positiveInteger](http://www.w3.org/2001/XMLSchema#positiveInteger) (c)<br />
[](startTime)
### startTime
Property | Value
--- | ---
IRI | `https://rub-informatik-im-bauwesen.github.io/prod#startTime`
Description | Designated or scheduled time at which a particular task, event, or activity begins.
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[prod:ProductionProcess](ProductionProcess) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />

## Named Individuals
## Namespaces
* **default (:)**
  * `https://rub-informatik-im-bauwesen.github.io/prod#`
* **aas**
  * `https://admin-shell.io/aas/3/0/`
* **dc**
  * `http://purl.org/dc/terms/`
* **owl**
  * `http://www.w3.org/2002/07/owl#`
* **prod**
  * `https://rub-informatik-im-bauwesen.github.io/prod#`
* **prov**
  * `http://www.w3.org/ns/prov#`
* **rdf**
  * `http://www.w3.org/1999/02/22-rdf-syntax-ns#`
* **rdfs**
  * `http://www.w3.org/2000/01/rdf-schema#`
* **sdo**
  * `https://schema.org/`
* **skos**
  * `http://www.w3.org/2004/02/skos/core#`
* **vann**
  * `http://purl.org/vocab/vann/`
* **xml**
  * `http://www.w3.org/XML/1998/namespace`
* **xsd**
  * `http://www.w3.org/2001/XMLSchema#`

## Legend
* Classes: c
* Object Properties: op
* Functional Properties: fp
* Data Properties: dp
* Annotation Properties: dp
* Properties: p
* Named Individuals: ni