# PWM_To_PPM_Encoder_Smooth

## IDE
Arduino 1.8.16

## Board
Arduino Pro Mini or Atmega328 or 328p chip

## Programmer:
ArduinoISP

![EngineLibrary](Screenshots/EngineLibrary.PNG)

## Wiring
Connect upto 8 RC PWM input signals so that the wires go to:
     red = 5v
     black = GND or 0V pin on arduino
     white = PWM signal pins, these connect to D0,D1,D2,D3,D4,D5,D6,D7

Connect the PPM output so that the wires go to:
     red = 5v
     black = GND or 0V
     PPM out = D10 
     
## Notes 
* any channel that you don't connect a PWM input on, will emit a default value ( which is 1500 for all channels excpt throttle, which is 1100.
* disconnecting any channel after booting will cause the system to use the last-known-position of the input, until a good signal returns.
* D0 and D1 are also used by the Serial Programmer/bootloader.   You can not reprogram this unit with PWM inputs still connected to D0 and D1, unplug unit from PWM sources before re-programming.
* THis is not a "failsafe" unit, if has no failsafe functionality.

## License
This repository and any materials provided by NI therein are provided AS IS. NI DISCLAIMS ANY AND ALL LIABILITIES FOR AND MAKES NO WARRANTIES, EITHER EXPRESS OR IMPLIED, INCLUDING WITHOUT LIMITATION ANY WARRANTIES OF MERCHANTABILITY, FITNESS FOR PARTICULAR PURPOSE, OR NON-INFRINGEMENT OF INTELLECTUAL PROPERTY. NI shall have no liability for any direct, indirect, incidental, punitive, special, or consequential damages for your use of the repository or any materials contained therein.
