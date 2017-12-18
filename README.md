# kentico-cms
Sharing front-end development knowledge to design within Kentico's portal engine webapp

***

# Transformations references

This is a resumé of the official Kentico documentation available here: [Kentico#10](https://docs.kentico.com/k10/developing-websites/loading-and-displaying-data-on-websites/writing-transformations/reference-transformation-methods), [K#11](https://docs.kentico.com/k11/developing-websites/loading-and-displaying-data-on-websites/writing-transformations/reference-transformation-methods)

## Boolean conditional operations

| method | coded example |
| :---: | --- |
| If | <%#&nbsp;`If(Eval("IsSecuredNode"),"If true do this","If false do that")`&nbsp;%> |
| IfCompare | <%#&nbsp;`IfCompare(1, 2, "The values are different", "The values are equal")`&nbsp;%> |
| IfEmpty | <%#&nbsp;`IfEmpty(Eval("PictureExample"), "No image", GetImage("PictureExample"))`&nbsp;%> |
| IfTrue | <%#&nbsp;`IfTrue(Eval("Example"), "If true do this")`&nbsp;%> |
| IsFirst | <%#&nbsp;`IsFirst("This is the first item of the list, so add a <ul> tag before")`&nbsp;%> |
| IsLast | <%#&nbsp;`IsLast("This is the last item of the list, so add a closing </ul> tag after")`&nbsp;%> |
| IsCurrentDocument | <%#&nbsp;`IsCurrentDocument()`&nbsp;%> |
| IsDocumentOnSelectedPath | <%#&nbsp;`IsDocumentOnSelectedPath()`&nbsp;%> |

## Data loading

*✔* The 2nd parameter is optional (false by default) = `<%# Eval("Example", false) %>`

| coded method | default false | description |
| --- | :---: | --- |
| <%#&nbsp;`Eval("Example")`&nbsp;%> | ✔ | Returns the value as an object data type. Use only for ASCX transformations.  |
| <%#&nbsp;`Eval<string>("Example")`&nbsp;%> | ✔ | Use only for ASCX transformations. `<string>` = _columnName_ |
| <%#&nbsp;`EvalCDATA("Example")`&nbsp;%> | ✔ | |
| <%#&nbsp;`EvalJSString("Example")`&nbsp;%> | ✔ | Encodes the returned text to be used in JavaScript code, encapsulated within `'` |
| <%#&nbsp;`GetEditableValue("Example")`&nbsp;%> | ✔ | Specify the region using the control ID (web part control ID) |
| <%#&nbsp;`GetNotEmpty("Example1;Example2")`&nbsp;%> | ✔ | Returns the value of the first data column that is not empty or null. The parameter must provide a list of column names separated by semicolons. |
| <%#&nbsp;`GetColumnName("Example")`&nbsp;%> | ✔ | Returns the value of the first column that is present in the data of the transformed object. The parameter must provide a list of column names separated by semicolons. By default, the method only returns columns that are not null or empty. Set the optional second parameter to true to allow empty values. 
| <%#&nbsp;`DataItem`&nbsp;%> | | Gets the currently transformed data item. |
| <%#&nbsp;`DataItemIndex`&nbsp;%> | | |
| <%#&nbsp;`DataItemCount`&nbsp;%> | | |
| <%#&nbsp;`DataRowView`&nbsp;%> | | |
| <%#&nbsp;`DisplayIndex`&nbsp;%> | | |
| <%#&nbsp;`DocumentCustomData["Example"]`&nbsp;%> | | Gets the value of custom page data fields (culture specific). Use the ["nodename"] notation to retrieve data stored in the specified node of the XML. |
| <%#&nbsp;`EditableItems["Example"]`&nbsp;%> | | Gets the content of the specified editable region on the page. |
| <%#&nbsp;`NodeCustomData["Example"]`&nbsp;%> | | Gets the value of custom page data fields (shared for all culture versions). Use the ["nodename"] notation to retrieve data stored in the specified node of the XML. |
