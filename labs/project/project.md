# Communication with multiple modules

### Team members

* Tomáš Kašpar (responsible for coding)
* Dušan Kratochvíl (responsible for documentation and voice narration)


Link to this file in your GitHub repository:

[https://github.com/xkaspa46/digital-electronics-2022/blob/main/labs/project/project.md](https://github.com/...)

### Table of contents

* [Project objectives](#objectives)
* [Hardware description](#hardware)
* [Libraries description](#libs)
* [Main application](#main)
* [Video](#video)
* [References](#references)

<a name="objectives"></a>

## Project objectives

Applicaton of modules was set in this order:
- **Communication with**
  * LCD display
  * Analog joystick
  * Rotary encoder
Then the coding itself:
- **Joystick**
  * Mapping current position depending on rotation of joystick
  * Pushbutton function
- **Encoder**
  * Spin (counter)clockwise - UP/DOWN counter
  * Alphabetical increment and counter
- **LCD module**
  * Display of functions


<a name="hardware"></a>

## Hardware description
* Analog Joystick
* Rotary encoder
* Digilent PmodCLP LCD module
* Arduino UNO
 
<a name="libs"></a>

## Libraries and description of their usage


   | **Library name** | **Brief description** | **Usage in our code** |
   | :-: | :-: | :-: |
   | GPIO  | TBD | Setting Input/Output of a pin and reading its values                       |
   | LCD   | TBD | Initialization of module itself, writing values/strings on exact positions |
   | Timer | Hardware block within an MCU and can be used to measure time events | Determination of refresh time of display and code cycle, interrupt `sei()` |
   | AVR   | TBD |  |


<a name="main"></a>

## Main application

Write your text here.

<a name="video"></a>

## Video

Write your text here

<a name="references"></a>

## References

1. Write your text here.
