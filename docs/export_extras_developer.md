Export extras for developers
-----------------------

### Preface

Blender addons may define custom properties which can be set in the addon-specific ui.
This guide is meant to give Blender-addons developers an overview on how  
these properties can be exported with the *glTF-Blender-Exporter* using the *Export extras* option.  

### Property Types

#### Which properties are exported?

```python
def register():
    bpy.types.Object.myObjectProperty = bpy.props.PointerProperty(type=EAWObjectPropertyGroup)
    bpy.types.World.myGlobalProperty = bpy.props.PointerProperty(type=WorldPropertyGroup)
```

#### Simple Properties

* BoolProperty, FloatProperty, IntProperty
* StringProperty
* EnumProperty
* BoolVectorProperty, FloatVectorProperty, IntVectorProperty

#### Structured Properties

* CollectionProperty
* PointerProperty

#### Export Hook

Lorem Ipsum ...

#### Ignored custom Properties
Some *api-defined* properties are ignored during the export.
The current black-list includes:
* cycles
* cycles_visibility
* cycles_curves
* _RNA_UI


#### Blender Development Resources
[Documentatino of Blender Properties](https://docs.blender.org/api/2.79/bpy.props.html)    
[blender.stackexchange](https://blender.stackexchange.com/questions/tagged/python+scripting)