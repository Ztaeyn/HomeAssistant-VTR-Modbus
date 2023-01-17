# HomeAssistant-VTR-Modbus
Simple control of Systemair VTR(300) via modbus directly to HA.

Credits to GMTrevis who created the original code for Home Assistant, and then improved it for use via Node-Red.
The Node Red version has full control of the VTR, but I had issues where it overloaded my Node-Red. 
I found his incomplete Home Assistant code, and am working on filling it out for my own experiences.

With this you currently can:
- Change operation Mode
- Set duration setpoint for Away, Vacation, Boost and Party
- See alarm status and filter replacement countdown.
  - TODO: Setup notifications to my phone.
- Set wanted temperature on the VTR thermostat.
- Create automations your own automations using the above. 
  - TODO: Set automatic Away when me and my partner are at Work. 

Known Issues:
See Issues Tab.


Sources:
* Modbus codes: https://shop.systemair.com/upload/assets/SAVE_MODBUS_VARIABLE_LIST_20190116__REV__29_.PDF
* Older HA code from GMTrevis: https://community.home-assistant.io/t/systemair-savecare-ventilation-unit/229653/2 
* New Node-Red/HA code from GMTrevis: https://github.com/GMTrevis/Homeassistant-NodeRed-Systemair-VTR300

HACS addons used:
* https://github.com/thomasloven/lovelace-card-mod
* https://github.com/custom-cards/button-card
* https://github.com/htmltiger/numberbox-card
* https://github.com/piitaya/lovelace-mushroom

Image of my Control Panel with full settings. A feedback check is added for Setpoints, with a comparison of the input number and the VTR sensor. Green when matching, Red when matching/waiting for sync.

<img src="https://user-images.githubusercontent.com/58105460/212980334-ebb6171f-e2f8-463c-b7aa-30d927fd5b3e.png" width="400">
<img src="https://user-images.githubusercontent.com/58105460/212980462-d8833cf8-0271-4090-b510-cd9a067c1393.png" width="400">



For the daily driver I have an overview with room cards displaying the operational state.

<img src="https://user-images.githubusercontent.com/58105460/211211807-b32b8dc6-8816-4dd9-9e3c-e7384acd6bf9.png" width="400">

With the room having a stripped down setup, linking via Config to the control panel.

<img src="https://user-images.githubusercontent.com/58105460/211211838-831058e2-42f3-409c-b5d5-5fb6a4974f4a.png" width="400">
