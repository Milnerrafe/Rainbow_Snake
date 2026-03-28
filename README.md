# Rainbow Snake
A simple python package that allows you to colour and format text in both terminal and idle environments.

**Example**
```python
from rainbowsnake import Color

Color.clear()
Color.clear()
    
Color.output(
    f"\nWelcome to {Color.bold + Color.hexbg('#EE1C25') + Color.hextext('#ffffff')}Mushroom Cafe{Color.hexOFF + Color.boldOFF} Payroll Management \n \n"
)
    
Color.output(
    f"{Color.warning}Please enter a number between 1 and 4{Color.warningOFF} \n"
)
    
Color.output("Select task:")
Color.output(f"{Color.bold}1{Color.boldOFF}. Enter hours worked")
Color.output(f"{Color.bold}2{Color.boldOFF}. Manage employees")
Color.output(f"{Color.bold}3{Color.boldOFF}. Export payroll slips")
Color.output(f"{Color.bold}4{Color.boldOFF}. View statistics \n")
```


Output of example
|  Platform Type |  Image |
|--|--|
| Terminal | ![Screenshot of code output in terminal](https://github.com/Milnerrafe/Rainbow_Snake/blob/3529079b14b0c878d98fae0b490e4123c2897f45/images/screenshot1.png)|
| Idle |![Screenshot of code output in Idle](https://github.com/Milnerrafe/Rainbow_Snake/blob/3529079b14b0c878d98fae0b490e4123c2897f45/images/screenshot2.png)|


# About
Rainbow Snake is a python package that allows you to add colour to your command line programs. 

Unlike other solutions that target terminal escape codes or idle colouring exclusively, Rainbow Snake works across all platforms, including idle and terminal based systems. 

Rainbowsnake supports progressive enhancement. That means that in terminal environments it can display full hex colours, but falls back to simple colour definitions in idle.

 In the terminal, Rainbowsnake can provide bold, any hex colour for text and any hex colour for background. It can also colour based on the built-in colours/symbolic styles of error, warning, success, information and important. 

In idle, Rainbow Snake can only provide bold and the contextual colours of error warning success information and important.

# Usage

**Install Package**
```bash
pip install rainbowsnake
```

**Import color class:**

```python
from rainbowsnake import Color
```

**Use Output [print()]**

```python
Color.output(f"Sometext")
```

**Use Input**

```python
somevalue = Color.input(f"Enter some input: ")
```

**Clear the Terminal**

```python
Color.clear()
```

**Bold text**

```python
Color.output(f"{Color.bold}Sometext{Color.boldOFF}")
```

**Symbolically Color**


Available Colors
| Name | Color | Start fString Code | end fString Code |
|--|--|--|--|
| Error | Red |`{Color.error}`|`{Color.errorOFF}`|
| Warning | Yellow |`{Color.warning}`|`{Color.warningOFF}`|
| Success | Green |`{Color.success}`|`{Color.successOFF}`|
| Information | Blue |`{Color.information}`|`{Color.informationOFF}`|
| Important | Purple |`{Color.important}`|`{Color.importantOFF}`|

```python
Color.output(f"{Color.error}Sometext{Color.errorOFF}")
```


**Hex Color Background**
```python
color.output( f"{color.hexbg('#EE1C25')}Sometext{color.hexOFF}")
```


**Hex Color Text**
```python
color.output( f"{color.hextext('#EE1C25')}Sometext{color.hexOFF}")
```


**Combining Codes**
```python
color.output( f"{color.hexbg('#EE1C25')}This text has a red background{color.hexOFF} and this is {Color.bold}bold{Color.boldOFF} and this an {Color.error}Error{Color.errorOFF}")
```

# API Reference
## Available Codes

Available Modifiers
| Name | Start fString Code | end fString Code |
|--|--|--|
| Bold | `{Color.bold}`|`{Color.boldOFF}`|

Available Colors
| Name | Color | Start fString Code | end fString Code |
|--|--|--|--|
| Error | Red |`{Color.error}`|`{Color.errorOFF}`|
| Warning | Yellow |`{Color.warning}`|`{Color.warningOFF}`|
| Success | Green |`{Color.success}`|`{Color.successOFF}`|
| Information | Blue |`{Color.information}`|`{Color.informationOFF}`|
| Important | Purple |`{Color.important}`|`{Color.importantOFF}`|

----------

## Hex Colors (Terminal Only)

| Type | Start Code |End Code|
|--|--|--|
| Text Color |`{Color.hextext("#RRGGBB")}`|`{Color.hexOFF}`|
|Background Color|`{Color.hexbg("#RRGGBB")}`|`{Color.hexOFF}`|


----------

## Functions

### `Color.output(string)`

Prints styled text using embedded color codes.

----------

### `Color.input(string)`

Displays a styled prompt and returns user input.

----------

### `Color.clear()`

Clears the screen.

----------

# Tips

Do not nest codes

    Color.output(f"{Color.error}This {Color.warning}will{Color.warningOFF} not work {Color.errorOFF}")

This will result in an error, instead, to change colors, end the current color and start the next color.

    Color.output(f"{Color.error}This {Color.errorOFF}{Color.warning}will{Color.warningOFF}{Color.error} not work {Color.errorOFF}")






