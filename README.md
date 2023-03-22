# HomeAssistant-VSR-Modbus
Simple control of Systemair VSR(300) via modbus TCP (Wifi/LAN) directly to HA.

Credits to Ztaeyn who i forked this project from and to GMTrevis who created the original code for Home Assistant, and then improved it for use via Node-Red.

With this you currently can:
- Change operation Mode
- Set duration setpoint for Away, Vacation, Boost, Crowded and Fireplace
- See alarm status and filter replacement countdown.
- Set wanted temperature on the VSR thermostat.
- Create automations your own automations using the above. 

Known Issues:
See Issues Tab.


Sources:
* SAVE VSR 300: https://shop.systemair.com/sv-SE/save--vsr--300/p609831
* Modbus Variable List: hhttps://shop.systemair.com/upload/assets/SAVE_MODBUS_VARIABLE_LIST_20210301_REV36.PDF?cbe60fbf
* Code for VTR credit to Ztaeyn: https://github.com/Ztaeyn/HomeAssistant-VTR-Modbus
* Older HA code from GMTrevis: https://community.home-assistant.io/t/systemair-savecare-ventilation-unit/229653/2 
* New Node-Red/HA code from GMTrevis: https://github.com/GMTrevis/Homeassistant-NodeRed-Systemair-VTR300

HACS addons used:
* https://github.com/thomasloven/lovelace-card-mod
* https://github.com/custom-cards/button-card
* https://github.com/htmltiger/numberbox-card
* https://github.com/piitaya/lovelace-mushroom

Image of Ztaeyns Control Panel with full settings. A feedback check is added for Setpoints, with a comparison of the input number and the VTR sensor. Green when matching, Red when matching/waiting for sync.

<img src="https://user-images.githubusercontent.com/58105460/212980334-ebb6171f-e2f8-463c-b7aa-30d927fd5b3e.png" width="400">
<img src="https://user-images.githubusercontent.com/58105460/212980462-d8833cf8-0271-4090-b510-cd9a067c1393.png" width="400">


Hardware used for my setup:
RS232/RS485 to Ethernet Converter - https://www.amazon.se/dp/B07S3HRYRR?ref=ppx_pop_dt_b_product_details&th=1
PoE-splitter 48 V till 5 V - https://www.amazon.se/gp/product/B0832SXPT7/ref=ppx_yo_dt_b_asin_title_o04_s03?ie=UTF8&psc=1


How to install this:
- Copy save_vsr_300.yaml to packages in you HA installation folder, and make sure you have included the packages directory in your configuration.yaml
- Modify save_vsr_300.yaml with your working modbus settings.
- Verify HA configuration is OK and reboot.
- Copy my HA UI card layouts if you'd like. Take note of the dependency of some HACS addons I've used.

Files explained:
User Interface/* - Copy of my HA card layout
save_vsr_300.yaml - Contains some system specific settings and everything else. NOTE: The addresses has an offset of -1 compared to the user manual linked.
configuration.yaml - Contains info how to include packages directory



