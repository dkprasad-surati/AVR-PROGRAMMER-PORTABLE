                        ______
                       (_____ \
                  _   _ _____) )___ ___   ____ 
                 | | | |  ____/ ___) _ \ / _  |
                 | |_| | |   | |  | |_| ( ( | |
                 | ____|_|   |_|   \___/ \_|| |
                 | |                    (_____|
                 |/


µProg - the AVR µControllers programmer

Hardware and software: Pawe³ Kisielewski "Manekinen"
manekinen@gmail.com

Used/based on third-party software:
AVR-DOS by Vögel Franz Josef
LPH7779 driver by Grzegorz Bujanowski RGB

Compiler: bascom-avr v.2.0.6.2   

PCB: Eagle light v.5.10.0    

Code quality: 2 WTFs/min

**************************************************************************    

Project website:  http://diy.elektroda.eu/uprog-maly-szybki-przenosny-programator-avr-z-sd/
English language: http://diy.elektroda.eu/uprog-maly-szybki-przenosny-programator-avr-z-sd/?lang=en

Any modifications allowed, do not remove this README.txt from archive.
Do not remove author info from pcb and code.

Any usage of this project in commercial/profit purposes, entirely or partly, is prohibited.

Project-related questions - post in comments on project site.
Other questions - contact me at manekinen@gmail.com

For software updates notifications, follow me at http://www.twitter.com/manekinen

**************************************************************************

Special thanks to:
Maciej Lassota "mlassota" mlassota76@gmail.com - beta tester

**************************************************************************
**************************************************************************

CHANGELOG:

_________________________
First release 05.06.2011:

PCB ver.1.0
-target programming tested from 3.0 to 5.5 volts

Firmware ver.1.0 BETA
-programmer fully tested with: tiny13, tiny2313, mega8, mega88, mega16, mega32, mega328, mega644
-write/read above 128kB (extended memory chips) has not been tested but it is implemented
Known issues (will be fixed within next update):
-write/read HEX files are probably limited to 64kB
-errors when writing eeporom from/to HEX files

Chip database ver.1.0
-109 chip records (47 fully supported, for rest only fuses/locks operations)


____________________
#1 Update 22.06.2011:

PCB ver.1.1
-added current limiting resistors for MOSI and SCK lines
This is necessary if your target works at 5V and have strong high state at MOSi and SCK lines
5V at ports supplied from 3V3 could damage these ports, resistors will take current overflow.

Firmware ver.1.1
-fixed issue when programmer got freeze after waking up from sleep mode
-fixed issue when LCD get too low voltage (contrast problems)
-fixed errors when writing/reading eeprom from/to HEX files
-fixed communication issues (SPI settings)
-fixed issue when non existing submenu options was visible
-fixed issue when broken verification progress bar appear if autoverify was disabled
-fixed freezing animations
-eliminated inconsistency between program and "chip.db" file in "programming method" byte
-added support for 48*102 organization LCDs (see "config.ini")
-added lcd contrast and bias settings to "config.ini" file
-added battery voltage measurement - device will not turn on if voltage exceeds 3,7V
-code improvements
