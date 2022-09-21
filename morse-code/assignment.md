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
