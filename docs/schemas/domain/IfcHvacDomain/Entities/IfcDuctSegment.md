# IfcDuctSegment

A duct segment is used to typically join two sections of duct network.

> HISTORY  New entity in IFC4

{ .note}
>

## Attributes

### PredefinedType


## Formal Propositions

### CorrectPredefinedType
Either the _PredefinedType_ attribute is unset (e.g. because an _IfcDuctSegmentType_ is associated), or the inherited attribute _ObjectType_ shall be provided, if the _PredefinedType_ is set to USERDEFINED.

### CorrectTypeAssigned
Either there is no duct segment type object associated, i.e. the _IsTypedBy_ inverse relationship is not provided, or the associated type object has to be of type _IfcDuctSegmentType_.

## Concepts

### Material


### Object Typing


### Port


### Property Sets for Objects


### Quantity Sets


