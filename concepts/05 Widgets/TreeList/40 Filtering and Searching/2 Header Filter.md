A header filter allows a user to filter values in an individual column by including or excluding them from the applied filter. Clicking a header filter icon invokes a popup menu with all the column's unique values. A user includes or excludes values from the filter by selecting or clearing their selection in this menu.

![DevExtreme HTML5 JavaScript jQuery Knockout Angular TreeList Filtering HeaderFilter](/images/treelist/visual_elements/header_filter.png)

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/Tree_List/UsingHeaderFilter/jQuery/Light/"
}

Assign **true** to the [headerFilter](/api-reference/10%20UI%20Widgets/dxTreeList/1%20Configuration/headerFilter '/Documentation/ApiReference/UI_Widgets/dxTreeList/Configuration/headerFilter/').**visible** option to make header filter icons visible for all columns. Set a column's [allowHeaderFiltering](/api-reference/10%20UI%20Widgets/GridBase/1%20Configuration/columns/allowHeaderFiltering.md '/Documentation/ApiReference/UI_Widgets/dxTreeList/Configuration/columns/#allowHeaderFiltering') option to **false** if its header filter should not be available. Note that this option inherits the [allowFiltering](/api-reference/10%20UI%20Widgets/GridBase/1%20Configuration/columns/allowFiltering.md '/Documentation/ApiReference/UI_Widgets/dxTreeList/Configuration/columns/#allowFiltering') option's value by default.

---
##### jQuery

    <!--JavaScript-->$(function() {
        $("#treeListContainer").dxTreeList({
            headerFilter: { visible: true },
            columns: [{
                // ...
                allowHeaderFiltering: false
            }]
        });
    });

##### Angular
    
    <!--HTML-->
    <dx-tree-list ... >
        <dxo-header-filter [visible]="true"></dxo-header-filter>
        <dxi-column [allowHeaderFiltering]="false" ... ></dxi-column>
    </dx-tree-list>

    <!--TypeScript-->
    import { DxTreeListModule } from 'devextreme-angular';
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxTreeListModule
        ],
        // ...
    })
    
---

A user can change the applied filter by including or excluding values to/from it. Use a column's [filterType](/api-reference/10%20UI%20Widgets/GridBase/1%20Configuration/columns/filterType.md '/Documentation/ApiReference/UI_Widgets/dxTreeList/Configuration/columns/#filterType') option to specify the required mode.

---
##### jQuery

    <!--JavaScript-->$(function() {
        $("#treeListContainer").dxTreeList({
            columns: [{
                // ...
                filterType: "exclude" // or "include"
            }]
        });
    });

##### Angular
    
    <!--HTML-->
    <dx-tree-list ... >
        <dxi-column ...
            [filterType]="exclude"> <!-- or "include" -->
        </dxi-column>
    </dx-tree-list>

    <!--TypeScript-->
    import { DxTreeListModule } from 'devextreme-angular';
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxTreeListModule
        ],
        // ...
    })
    
---

The header filter provides a searching capability that you can enable using the **headerFilter**.[allowSearch](/api-reference/10%20UI%20Widgets/GridBase/1%20Configuration/headerFilter/allowSearch.md '/Documentation/ApiReference/UI_Widgets/dxTreeList/Configuration/headerFilter/#allowSearch') option. The same option can be declared in a column's configuration object, in which case it controls searching in that column's header filter.

---
##### jQuery

    <!--JavaScript-->$(function() {
        $("#treeListContainer").dxTreeList({
            headerFilter: { 
                visible: true,
                allowSearch: true
            },
            columns: [{
                // ...
                headerFilter: { 
                    allowSearch: false
                }
            }]
        });
    });

##### Angular
    
    <!--HTML-->
    <dx-tree-list ... >
        <dxo-header-filter [visible]="true" [allowSearch]="true"></dxo-header-filter>
        <dxi-column ... >
            <dxo-header-filter [allowSearch]="false"></dxo-header-filter>
        </dxi-column>
    </dx-tree-list>

    <!--TypeScript-->
    import { DxTreeListModule } from 'devextreme-angular';
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxTreeListModule
        ],
        // ...
    })
    
---

A header filter's popup menu lists all column values by default. You can group them using the **headerFilter**.[groupInterval](/api-reference/10%20UI%20Widgets/GridBase/1%20Configuration/columns/headerFilter/groupInterval.md '/Documentation/ApiReference/UI_Widgets/dxTreeList/Configuration/columns/headerFilter/#groupInterval') option if they are numbers or dates. You can also provide a custom data source for a header filter using the [dataSource](/api-reference/10%20UI%20Widgets/GridBase/1%20Configuration/columns/headerFilter/dataSource.md '/Documentation/ApiReference/UI_Widgets/dxTreeList/Configuration/columns/headerFilter/#dataSource') option. Refer to the option's description for details.

#####See Also#####
- [Filtering API - Initial and Runtime Filtering](/concepts/05%20Widgets/TreeList/40%20Filtering%20and%20Searching/5%20API/1%20Initial%20and%20Runtime%20Filtering.md '/Documentation/Guide/Widgets/TreeList/Filtering_and_Searching/#API/Initial_and_Runtime_Filtering')