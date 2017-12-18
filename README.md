# kentico-cms
Sharing front-end development knowledge to design within Kentico's portal engine webapp

*✔* The 2nd parameter is optional (false by default) = `<%# Eval("Example", false) %>`

## Data loading

| coded method | default false | description |
| --- | :---: | --- |
| <%#&nbsp;`Eval("Example")`&nbsp;%> | ✔ | Returns the value as an object data type. Use only for ASCX transformations.  |
| <%#&nbsp;`Eval<string>("Example")`&nbsp;%> | ✔ | Use only for ASCX transformations. `<string>` = _columnName_ |
| <%#&nbsp;`EvalCDATA("Example")`&nbsp;%> | ✔ | |

This is a resumé of the official Kentico documentation available here: [Kentico#10](https://docs.kentico.com/k10/developing-websites/loading-and-displaying-data-on-websites/writing-transformations/reference-transformation-methods), [K#11](https://docs.kentico.com/k11/developing-websites/loading-and-displaying-data-on-websites/writing-transformations/reference-transformation-methods)
