| loio |
| -----|
| 98861cf90b874e3394b666cfb347ff0b |

<div id="loio">

view on: [help.sap.com](https://help.sap.com/viewer/DRAFT/3237636b137e43519a20ad5513c49ccb/latest/en-US/98861cf90b874e3394b666cfb347ff0b.html) | [demo kit nightly build](https://openui5nightly.hana.ondemand.com/#/topic/98861cf90b874e3394b666cfb347ff0b) | [demo kit latest release](https://openui5.hana.ondemand.com/#/topic/98861cf90b874e3394b666cfb347ff0b)</div>
<!-- loio98861cf90b874e3394b666cfb347ff0b -->

## View Replacement

Views of a delivered standard application can be replaced to adapt the application to the customer needs.

If the extension points provided for view extension are not sufficient to meet the requirements of the custom application, you can replace the standard view with a custom view.

The following view is delivered in the standard application:

```lang-js

<mvc:View xmlns="sap.m" xmlns:mvc="sap.ui.core.mvc">
    <TextView text="SAP View 'Sub1' - this one should have been replaced by the customer View"></TextView>  
</mvc:View>

```

This is the custom view to replace the standard view:

```lang-js

<mvc:View xmlns="sap.m" xmlns:mvc="sap.ui.core.mvc">
    <TextView text="Custom View 'Sub1' - this one replaces the original SAP View 'Sub1'"></TextView>    
</mvc:View>
```

The following extension replaces the custom view with the view in the standard application

```lang-js

extensions: {
    .....some more content
    "sap.ui.viewReplacements": {
        "samples.components.ext.sap.Sub1": {
            viewName: "samples.components.ext.customer.CustomSub1",
            type: "XML"
        }
    },
    .....some more content

```
