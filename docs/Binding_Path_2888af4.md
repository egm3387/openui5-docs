| loio |
| -----|
| 2888af49635949eca14fa326d04833b9 |

<div id="loio">

view on: [help.sap.com](https://help.sap.com/viewer/DRAFT/3237636b137e43519a20ad5513c49ccb/latest/en-US/2888af49635949eca14fa326d04833b9.html) | [demo kit nightly build](https://openui5nightly.hana.ondemand.com/#/topic/2888af49635949eca14fa326d04833b9) | [demo kit latest release](https://openui5.hana.ondemand.com/#/topic/2888af49635949eca14fa326d04833b9)</div>
<!-- loio2888af49635949eca14fa326d04833b9 -->

## Binding Path

Binding paths address the different properties and lists in a model and define how a node in the hierarchical data tree can be found.

A binding path consists of a number of name tokens, which are separated by a separator char. In all models provided by the framework, the separator char is the slash "/".

A binding path can either be absolute or relative: Absolute binding paths start with a slash, relative binding paths start with a name token and are resolved relative to the context of the control that is bound. A context exists either for each entry of the aggregation in case of aggregation binding or can be set explicitly for a control by using the `setBindingContext` method.

When you use multiple models, specify the model name within the binding path to address the correct model. The same applies for setting a binding context for such a model. The binding path must start with the model name followed by a '\>' as shown in the following example for setting a binding context.

```lang-js
oControl.setBindingContext(oContext );
oControl.setBindingContext(oContext,"myModelName");
```

Binding path examples:

```
'/Products/0/ProductName'
'/Products(0)/ProductName'
'ProductName'

//with model name
'myModelName>/Products/0/ProductName'
'myModelName>/Products(0)/ProductName'
'myModelName>ProductName'
```

**Related information**  


[OData V2 Model](OData_V2_Model_.md#loio6c47b2b39db9404582994070ec3d57a2)

[OData V4 Model: Bindings](Bindings_54e0ddf.md)

[Binding Path Syntax for JSON Models](JSON_Model_.md#loiod52e364907f94a3caeb4f5e5ad0cf302)

[Binding Path Syntax for XML Models](XML_Model_.md#loiob8a2c24356c443228f7819d45697a2b8)

[Binding Path Syntax for Resource Models](Resource_Model_.md#loiof05c6f2cf18241cbbb2b126989108765)
