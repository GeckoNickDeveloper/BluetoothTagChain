# BTC (Bluetooth Tag Chain)

BTC is born with the idea of transmit small quantity of data between two devices via [Bluetooth]('https://www.bluetooth.com/'). It's also inspired by [JSON]('https://en.wikipedia.org/wiki/JSON') but tries to be more lightweight.
The main drowback of BTC is that strings value are very limited in order to communicate the minimum sensitive informations.

> It's very important  to specify that BTC supports **mixed lists**:<br>
> different data types can be included to the list, including more lists<br>
## Specific
This data rappresentation is based on those 3 data types:
 - numbers
 - strings
 - booleans
## Syntax
There are few sintax rules, but they are very strict:
> Each tag must start with `@`<br>
> Tag name are strings that can be composed by `-`<br>
> Tag name is case sensitive<br>
> A tag ends with `>` character<br>
___
**Strings**<br>
Strings are rappresented with: `"my string"`<br>
There are some limitations:
> Every special character that requires a backslash to be rappresented is not allowed<br>
> for example: `\n`, `\t`, `\"`, ecc...

**Numbers**<br>
Numbers are rappresented with a series of numbers (for example: `37.49`)<br>
**Booleans**<br>
Booleans are rappresented with `true` or `false`<br>
___
> Objects can't be empty
> List can't be empty

#### Element
An Element is a basic pair between a **_TAG_** and **_DATA_**<br>
```
@identifier-name > *
```
Where \* can assume the following data types:
- _Basic Datas_:
    - _Numbers_
    - _Strings_
    - _Booleans_
- _Complex Datas_:
    - _Objects_
    - _Lists_
___
#### Object
An object is a structure composed of several Elements.<br>
**Object syntax**<br>
> An Object starts with `(` and ends with `)`<br>
> Each item inside an Object **IS** an Element<br>
```
(
    @comp-a > 13
    @comp-b > "Ajeje Brazorf"
    @comp-c > true
)
```
___
#### List
Lists are compositions of Data.<br>
**List syntax**<br>
> A List starts with `[` and ends with `]`<br>
> Each item in the List is separated by `,` character<br>
> Each item in the List **ISN'T** an Element: IS a **DATA**<br>
```
[
    420.69,
    "Mixed Type List",
    (
        @comp-a > "Wait. That's illegal."
        @comp-b > "Ah, I see you're a developer of culture as well!"
        @comp-c > true
    ),
    [
        "Wait. That's",
        "Outstanding move",
        "Behind science",
        "*MEME's POWER INTESIFIES*"
    ]
]
```