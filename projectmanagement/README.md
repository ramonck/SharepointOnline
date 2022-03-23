# Manage projects from Sharepoint Online

Video: https://youtu.be/eEk2hUWRjLQ

Code for row color (Format View):
```
{
  "$schema": "https://developer.microsoft.com/json-schemas/sp/v2/row-formatting.schema.json",
  "additionalRowClass": {
    "operator": ":",
    "operands": [
      {
        "operator": ">",
        "operands": [
          {
            "operator": "Date()",
            "operands": [
              {
                "operator": "toDateString()",
                "operands": [
                  {
                    "operator": "Date()",
                    "operands": [
                      "[$EndDate]"
                    ]
                  }
                ]
              }
            ]
          },
          {
            "operator": "Date()",
            "operands": [
              {
                "operator": "toDateString()",
                "operands": [
                  {
                    "operator": "Date()",
                    "operands": [
                      "[$DueDate]"
                    ]
                  }
                ]
              }
            ]
          }
        ]
      },
      "sp-css-backgroundColor-BgDustRose sp-field-fontSizeSmall sp-css-color-DustRoseFont",
      "sp-css-backgroundColor-BgMintGreen sp-field-fontSizeSmall sp-css-color-MintGreenFont"
    ]
  }
}
```
