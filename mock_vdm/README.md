# Mock Universal VDM vehicle dynamics model / emulator
## Idea 
* Test harness device for ECUs interfacing to vehicle ecus. 
* Use Aurix developer board to make mock vehicle Can bus interface to test command sw
* Use for rapid testing of controlling ecu. 
* Keep application code seperate from platform
  
## Features
* Configurable to different vehicle platforms.
* Not high accuracy just sufficient handshaking for smoke tests, logical errors, basic motion control etc.
* Abstract vehicle interface (hardware abstraction layer)
* [_] ToDo post code seperate from Application Kit/infineon code. 


 

### References
* https://github.com/commaai/opendbc
* Developer kit: https://www.mouser.com/ProductDetail/726-KITA2GTC3975VTFT
* https://www.mouser.com/datasheet/2/196/Infineon_ApplicationKitManual_TC3X7_UM_v02_00_EN-1842031.pdf
  
