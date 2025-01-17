# IfcReference

This entity is used to refer to a value of an attribute on an instance. It may refer to the value of a scalar attribute or a value within a collection-based attribute. Referenced attributes may be direct values, object references, collections, inverse object references, and inverse collections. References may be chained to form a path of object-attribute references.

## Attributes

### TypeIdentifier
Optional identifier of the entity or type such as 'IfcMaterialLayerSet'. For entity, type, or select-based references within a collection, this resolves the reference to such type.
If omitted, the type is assumed to be the same as the declared referencing attribute.

> EXAMPLE  _IfcRelAssociatesMaterial_._RelatingMaterial_ may be resolved to _IfcMaterialLayerSet_.

### AttributeIdentifier
Optionally identifies a direct or inverse attribute within an entity such as 'MaterialLayers'.
If _TypeIdentifier_ is specified and refers to an entity, the attribute must exist within the referenced entity.
A null value indicates a reference to the type or entity itself, such as for indicating that the type of a value must match a specified constraint.

### InstanceName
Optionally identifies an instance within a collection according to name.  If the instance has an attribute called 'Name', such attribute is used for comparison; otherwise the first STRING-based attribute of the entity is used.

> EXAMPLE  _IfcRoot_-based entities such as _IfcPropertySet_ use the _Name_ attribute; _IfcRepresentation_ entities use the _RepresentationIdentifier_ attribute.

### ListPositions
Optionally identifies an instance within a collection according to position starting at 1.  For referencing single-level collections, this attribute contains a single member; for referencing multi-level collections, then this LIST attribute contains multiple members starting from the outer-most index.

### InnerReference
Optional reference to an inner value for ENTITY, SELECT, SET, or LIST attributes.
A path may be formed by linking _IfcReference_ instances together.
> EXAMPLE  A material layer thickness may be referenced using several instances: #1=IFCREFERENCE($,'IfcSlab','HasAssociations',#2); #2=IFCREFERENCE($,'IfcMaterialLayerSet','MaterialLayers',#3); #3=IFCREFERENCE('Core','IfcMaterialLayer','LayerThickness',$);
