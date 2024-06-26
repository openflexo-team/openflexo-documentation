# TypedDiagram
[//]: # (Do not edit this file, which is automatically generated)

<img src="/openflexo-diagram/images/TypedDiagramModelSlot_BIG.png" alt="TypedDiagramModelSlot"/> This ModelSlot represents access to a Diagram conform to a DiagramSpecification

Such diagram refers to a diagram metamodel which is composed of a example diagram and a collection of palettes both encoding template shapes and connectors

---

## Usage

```java
[visibility] [cardinality] Diagram <identifier>
with TypedDiagram(diagramSpecification=<diagramSpecification_path>[,options]);
```

or

```java
[visibility] [cardinality] Diagram <identifier>
with DIAGRAM::TypedDiagram(diagramSpecification=<diagramSpecification_path>[,options]);
```

where

- `visibility` is default (unspecified), 'public', 'protected' or 'private'
- `cardinality` is \[0,1\] (unspecified), \[0,\*\] or \[1,\*\]
- \<identifier\> is the name of declared model slot variable
- \<diagramSpecification_path\> addresses a `DiagramSpecification`

---

## Configuration

| Property        | Type                    | &nbsp;Required&nbsp;  |
| --------------- |-------------------------| :------:|
| `diagramSpecification` &nbsp; | `DiagramSpecification` &nbsp; | yes |
| `container` &nbsp; | `Object` &nbsp; | no |
| `isReadOnly` &nbsp; | `boolean` &nbsp; | no |
| `isRequired` &nbsp; | `boolean` &nbsp; | no |
| `paletteElementBindings` &nbsp; | `List<FMLDiagramPaletteElementBinding>` &nbsp; | no |

---

- `diagramSpecification` : DiagramSpecification this diagram must conform to
- `container` : 
- `isReadOnly` : 
- `isRequired` : 
- `paletteElementBindings` : 

---

## Examples

```java
Diagram myDiagram with DIAGRAM::TypedDiagram(
        diagramSpecification = myDiagramSpecification,
        paletteElementBindings = {
            FMLDiagramPaletteElementBinding:(elementId="MyPaletteElement",
        dropAction="MyConcept.drop()",overridingGR=RED_SHAPE2),
            FMLDiagramPaletteElementBinding:(elementId="MyPaletteElement2",dropAction="MyConcept.drop()")
});
```

Declares a model slot called 'myDiagram' with resulting type 'Diagram', realized through the 'TypedDiagram' model slot, conform to 'myDiagramSpecification' and specified palette element bindings

[//]: # --------------------- ROLES
---

## Roles

- <img src="/openflexo-diagram/images/ShapeRole.png" alt="ShapeRole"/> [ShapeRole](ShapeRole.md) : No documentation yet
- <img src="/openflexo-diagram/images/ConnectorRole.png" alt="ConnectorRole"/> [ConnectorRole](ConnectorRole.md) : No documentation yet
- <img src="/openflexo-diagram/images/DiagramRole.png" alt="DiagramRole"/> [DiagramRole](DiagramRole.md) : No documentation yet

[//]: # --------------------- BEHAVIOURS
---

## Behaviours

- <img src="/openflexo-diagram/images/DropScheme.png" alt="DropScheme"/> [DropScheme](DropScheme.md) : No documentation yet
- <img src="/openflexo-diagram/images/DrawRectangleScheme.png" alt="DrawRectangleScheme"/> [DrawRectangleScheme](DrawRectangleScheme.md) : No documentation yet
- <img src="/openflexo-diagram/images/LinkScheme.png" alt="LinkScheme"/> [LinkScheme](LinkScheme.md) : No documentation yet
- <img src="/openflexo-diagram/images/DiagramNavigationScheme.png" alt="DiagramNavigationScheme"/> [DiagramNavigationScheme](DiagramNavigationScheme.md) : No documentation yet

[//]: # --------------------- EDITION ACTIONS
---

## Edition actions

- <img src="/openflexo-diagram/images/CreateDiagram.png" alt="CreateDiagram"/> [CreateDiagram](CreateDiagram.md) : This edition primitive addresses the creation of a new diagram.
- <img src="/openflexo-diagram/images/AddShape.png" alt="AddShape"/> [AddShape](AddShape.md) : This edition primitive addresses the creation of a new shape in a diagram.
- <img src="/openflexo-diagram/images/AddConnector.png" alt="AddConnector"/> [AddConnector](AddConnector.md) : This edition primitive addresses the creation of a new connector linking two shapes in a diagram
- <img src="/openflexo-diagram/images/GraphicalAction.png" alt="GraphicalAction"/> [GraphicalAction](GraphicalAction.md) : No documentation yet

[//]: # --------------------- FETCH REQUEST

---

## Javadoc

[org.openflexo.technologyadapter.diagram.TypedDiagramModelSlot](./apidocs/org/openflexo/technologyadapter/diagram/TypedDiagramModelSlot.md)

[//]: # --------------------- SEE ALSO
---

## See also

- <img src="/openflexo-diagram/images/FreeDiagramModelSlot.png" alt="FreeDiagramModelSlot"/> [FreeDiagram](FreeDiagramModelSlot.md) : This ModelSlot represents access to a Diagram without any DiagramSpecification conformance
- <img src="/openflexo-diagram/images/CreateDiagram.png" alt="CreateDiagram"/> [CreateDiagram](CreateDiagram.md) : This edition primitive addresses the creation of a new diagram.
