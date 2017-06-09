## Improvements in V2:

- Full 3V/5V compatibility
  - Power can be either, I2C signals can be either. All combinations are valid, i.e.:
    - 5V Power, 5V I2C
    - 5V Power, 3.3V I2C
    - 3.3V Power, 5V I2C
    - 3.3V Power, 3.3V I2C
  - No solder jumpers to set voltage, works automatically.
- Continuous voltage input range
  - Previously 3.3V-3.6V in 3.3V mode, 4.5-5.5V in 5V mode
  - Now 3.3V – 5.5V, no ‘modes’
- Modules are now ‘Chainable’
  - Each module has 3 JST-SH sockets on board, modules can be daisy-chained to reduce wiring clutter
  - May remove need for splitter boards in some printer layouts
- Overvoltage protection
  - Protected against supply voltages > 5.5V and < 15V, i.e. 12V will not damage the module but it will not operate in this condition.
- Reverse polarity protection
  - Protected against accidentally reversing VDD and GND pins in connector. Reversal will not damage the module but it will not operate in this condition.
- Overcurrent protection
- DIP switches instead of solder jumpers
  - Easy to set module address via switch positions
  - No longer necessary to cut/solder jumpers
  - Easily changeable/reversible
  - Configuration via I2C is still possible if preferred
- Faster on-board microcontroller
  - STM32F030F4P6 instead of ATmega328-AU
  - Possibility for averaging/filtering readings on-board