
# Lab 1: Tomáš Kašpar

### Morse code

1. Listing of C code which repeats one "dot" and one "comma" (BTW, in Morse code it is letter `A`) on a LED. Always use syntax highlighting, meaningful comments, and follow C guidelines:

```c

#include <avr/io.h>     
#include <util/delay.h> 

#include "Arduino.h"

int main(void)
{
    // Set pin where on-board LED is connected as output
    #define LED_RED 8
    pinMode(LED_RED, OUTPUT);

    #define SHORT_DELAY 100
    #define LONG_DELAY 400

    // Infinite loop
    while (1)
    {
        // Generate a lettre `A` Morse code
        digitalWrite(LED_RED, LOW);
        _delay_ms(LONG_DELAY);
        digitalWrite(LED_RED, HIGH);
        _delay_ms(SHORT_DELAY);
        digitalWrite(LED_RED, LOW);
        _delay_ms(LONG_DELAY);
        digitalWrite(LED_RED, HIGH);
        _delay_ms(800);

    }

    // Will never reach this
    return 0;
}
```

2. Scheme of Morse code application, i.e. connection of AVR device, LED, resistor, and supply voltage. The image can be drawn on a computer or by hand. Always name all components and their values!

   ![your figure]()
