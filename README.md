# Aurix Tricore TC397B SW
Aurix Tricore
* Arm core
* Used in Automotive ECUs
* 5x cores
* sleep / low power support
* ASIL D capable.
* Can bus, Tft, Ethernet, .... 
  
## Notes

### Hellow world
* Get developer kit: https://www.mouser.com/ProductDetail/726-KITA2GTC3975VTFT
* Install aurix-devel-studio
* To flash install DAS server - DAS64 for some reason v7.3.7 works 8.04 and 7.1 both didn't work out of box for me. 
* Import examples blinkey etc. build & flash.

### Application Kit SW
* Get: Application_Kit_TC397B_V2.0.0.zip https://community.infineon.com/t5/Code-Examples/Code-example-for-TC397-Application-Kit/td-p/365906 not sure where actual source repo is.
* **Could only work using iLLD from blinkey project not original in BaseSW illd**
* Import new Blinkey project
* Delete main_xx.c and blinkey.c/h
* Paste directory 0_src/AppSW into blinkey project
* Enable "auto include paths" in project settings

#### Compiler errors:
* Redeclaration error http_client.c: remove typedef (want to define content of struct not redeclare typedef)
* (Look for equivalent examples in Blinkey code)
* Comment out "initTime()"
* Remove i51 directory.  unextern scrProgram* _ToDo fix properly_
* IFX_Align CPUsync (see blinkey)

  
Success!
 

### References
* https://en.wikipedia.org/wiki/Infineon_AURIX
* Aurix developer studio  free - windows 10: https://www.infineon.com/cms/en/product/promopages/aurix-development-studio/
* https://github.com/Infineon/AURIX_code_examples/tree/master/code_examples
* Developer kit: https://www.mouser.com/ProductDetail/726-KITA2GTC3975VTFT
* https://www.mouser.com/datasheet/2/196/Infineon_ApplicationKitManual_TC3X7_UM_v02_00_EN-1842031.pdf
  
