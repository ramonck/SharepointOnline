# Manage projects from Sharepoint Online

Code for column color:
```
{
    "$schema": "https://developer.microsoft.com/json-schemas/sp/v2/column-formatting.schema.json",
    "elmType": "div",
    "txtContent": "@currentField",
    "style": {
        "background-color": "=if(Number(@currentField) == 0, '', if(@currentField >= @now, 'lightgreen', 'red'))"
    }
}
```
