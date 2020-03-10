# Bluetooth Tag Chain (BTC)

_BTC_ is born with the idea of transmit small quantity of data between two devices via [_Bluetooth_]('https://www.bluetooth.com/'). It's also inspired by [_JSON_]('https://en.wikipedia.org/wiki/JSON') but tries to be more lightweight.

> It's very important  to specify that BTC supports **mixed lists**: 
> different data types can be included to the list, including more lists
## Specific
This data rappresentation is based on those 4 data types:
 - int
 - double
 - string
 - boolean
## Syntax
#### Element
TODO MIN DESC OF ELEMENT
```
@identifier-name > *
```
Where \* can assume the following data types:
- basic types:
    - int
    - double
    - string
    - boolean
- complex types:
    - object
    - list
___
#### Object
An object is a structure composed of several elements 
```
(
    @comp-a > 13
    @comp-b > "Ajeje Brazorf"
    @comp-c > true
)
```
Obviously, the object can fits more than 3 elements of the example
___
#### List
```
[
    420.69 |
    "Mixed Type List" |
    (
        @comp-a > "Wait. That's illegal."
        @comp-b > "Do you understand the reference?"
        @comp-c > true
    ) |
    false |
    [
        "This bad boy can" |
        "Fits a lot of things" |
        "Inside itself!" |
        "*MEME's POWER INTESIFIES*"
    ]
]
```
ADD DESCRIPTION
___
## TODO
Definire il carattere di fine elemento [al momento è '<']