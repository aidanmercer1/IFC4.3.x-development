# IfcEvaporator

An evaporator is a device in which a liquid refrigerent is vaporized and absorbs heat from the surrounding fluid.

> HISTORY  New entity in IFC4

{ .note}
>

## Attributes

### PredefinedType


## Formal Propositions

### CorrectPredefinedType
Either the _PredefinedType_ attribute is unset (e.g. because an _IfcEvaporatorType_ is associated), or the inherited attribute _ObjectType_ shall be provided, if the _PredefinedType_ is set to USERDEFINED.

### CorrectTypeAssigned
Either there is no evaporator type object associated, i.e. the _IsTypedBy_ inverse relationship is not provided, or the associated type object has to be of type _IfcEvaporatorType_.

## Concepts

### Material


### Object Typing


### Port


### Property Sets for Objects


### Quantity Sets


