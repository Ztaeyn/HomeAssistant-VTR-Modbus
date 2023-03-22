# HomeAssistant-VSR-Modbus
Simple control of Systemair VTR(300) via modbus TCP (Wifi) directly to HA.

Credits to GMTrevis who created the original code for Home Assistant, and then improved it for use via Node-Red.
The Node Red version has full control of the VTR, but I had issues where it overloaded my Node-Red. 
I found his incomplete Home Assistant code, and am working on filling it out for my own experiences.

With this you currently can:
- Change operation Mode
- Set duration setpoint for Away, Vacation, Boost, Crowded and Fireplace
- See alarm status and filter replacement countdown.
- Set wanted temperature on the VSR thermostat.
- Create automations your own automations using the above. 

Known Issues:
See Issues Tab.


Sources:
* SAVE VSR 300 -  https://shop.systemair.com/sv-SE/save--vsr--300/p609831
* Modbus Variable List - https://shop.systemair.com/upload/assets/SAVE_MODBUS_VARIABLE_LIST_20210301_REV36.PDF?cbe60fbf
* Ztaeyn original work for VTR: https://github.com/Ztaeyn/HomeAssistant-VTR-Modbus
* Older HA code from GMTrevis: https://community.home-assistant.io/t/systemair-savecare-ventilation-unit/229653/2 
* New Node-Red/HA code from GMTrevis: https://github.com/GMTrevis/Homeassistant-NodeRed-Systemair-VTR300


Hardware required:
A modbus tcp converter.

Industrial RS232/RS485 to Ethernet Converter - https://www.amazon.se/gp/product/B07S3HRYRR/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1
PoE-splitter 48 V till 5 V - https://www.amazon.se/gp/product/B0832SXPT7/ref=ppx_yo_dt_b_asin_title_o04_s03?ie=UTF8&psc=1

How to install this:
- Add save_vsr_300.yaml to packages folder in HA installation folder.
- Include packages directory in configuration.yaml

Files explained:
save_vsr_300.yaml - Stored in the HA root folder. Contains the system specific settings, and everything else. NOTE: The addresses has an offset of -1 compared to the VSR user manual.
configuration.yaml - How to include packages directory in your configuration.



