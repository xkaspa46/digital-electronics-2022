# Wiper drive

### Team members

* Tomáš Kašpar (responsible for documentation and voice narration)
* Dušan Kratochvíl (responsible for coding)

### Table of contents

* [Project objectives](#objectives)
* [Hardware](#hardware)
  * [Servo motor](#servo)
* [Software and libraries](#libs)
  * [Source files](#sourcefiles)
  * [Flowcharts](#flowcharts)
* [Functions](#functions)
  * [Joystick](#joystick)
    * [Position map](#positionmap)
    * [Button detection](#buttondetect)
  * [Encoder](#encoder)
    * [Value counter up/down](#counter)
    * [Alphabet](#alphabet)
* [Video](#video)
* [References](#references)

<a name="objectives"></a>

## Project objectives

Applicaton of modules was set in this order:
- **PWM initialization**
- **Wiping servo motor**


<a name="hardware"></a>

## Brief hardware of description Servo motor and schematic

This section is reserved for a short description of each element our project is composed of. It also includes separated wiring schemes corresponding to each one of used hardware for better orientation.

<a name="servo"></a>

### Servo motor

It is a development board consisting of ATmega328 microcontroller, 14 digital GPIO pins (6 PWM), 6 analog input pins, 16 MHz crystal oscilator, built-in pre-defined UART etc. Programmed via USB 2.0, it has 32 kB flash memory (0.5 kB for bootloader). 

*We can see a look of the board below:*

![Arduino](pictures/ArduinoBoard2.jpg)

<a name="joystickHW"></a>


<a name="libs"></a>

## Software and libraries

   | **Library name** | **Brief description** | **Usage in our code** |
   | :-: | :-: | :-: |
   | GPIO  | Allowing high performance digital pin access | Setting Input/Output of a pin and reading its values |
   | Timer | Hardware block within an MCU and can be used to measure time events | Determination of refresh time of display and code cycle, interrupt `sei()` |
   | AVR   | Predefined library of AVR microcontrollers | Basic functions for working with registers |

<a name="sourcefiles"></a>

### Source files & libraries

 1. **Timer:** [timer.h](https://github.com/xkrato62/Digital-electronics_2/blob/main/Labs/Project1/Project1/include/timer.h)
 2. **Gpio:** [gpio.c](https://github.com/xkrato62/Digital-electronics_2/blob/main/Labs/Project1/Project1/lib/gpio/gpio.c), [gpio.h](https://github.com/xkrato62/Digital-electronics_2/blob/main/Labs/Project1/Project1/lib/gpio/gpio.h)
 3. **Source:** [main.c](https://github.com/xkrato62/Digital-electronics_2/blob/main/Labs/Project1/Project1/src/main.c)
 4. **Hex** [firmware.hex](https://github.com/xkrato62/Digital-electronics_2/blob/main/Labs/Project1/Project1/.pio/build/uno/firmware.hex)

  *Project structure:*
   ```c
   ├── include
   │   └── timer.h
   ├── lib
   │   └── gpio
   │       ├── gpio.c
   │       └── gpio.h
   └── src
       └── main.c
   ```

<a name="flowcharts"></a>

### Software flowcharts

![Flowchar1](pictures/flow1.png)

![Flowchar2](pictures/flow2.png)

![Flowchar3](pictures/flow4.png)

![Flowchar5](pictures/flow5.png)

![Flowchar4](pictures/flow3.png)

<a name="functions"></a>

## Functions

<a name="joystick"></a>



<a name="video"></a>

## Video

[YT video with narration](https://youtu.be/0WYqbr4WcUk)🎞🎥📀

<a name="references"></a>

## References

* [1. GPIO](https://github.com/mikaelpatel/Arduino-GPIO)
* [2. doc. Ing. Fryza Ph.D. DE2 - 2022 Labs](https://github.com/tomas-fryza/digital-electronics-2/tree/master/labs)
* [3. Joystick](https://navody.dratek.cz/navody-k-produktum/arduino-joystick-ps2.html)
* [4. Encoder](https://howtomechatronics.com/tutorials/arduino/rotary-encoder-works-use-arduino/?fbclid=IwAR1UxOQv36Y3HIfpMDaVhkYf1JpnIz0Ywbn_U0N9zagLQHEsaXvEKFfGdwQ)
* [5. Digilent official website](https://projects.digilentinc.com/products/pmod-clp)
