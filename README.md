# HomeAssistant-VTR-Modbus
Simple control of Systemair VTR(300) via modbus directly to HA.

Credits to GMTrevis who created the original code for Home Assistant, and then improved it for use via Node-Red.
The Node Red version has full control of the VTR, but I had issues where it overloaded my Node-Red. 
I found his incomplete Home Assistant code, and am working on filling it out for my own experiences.

Known Issues:
- Original code says Kitchen Fan is running when the Pressure system is active. Not looking into it, presumably just a change of name.



Sources:
* Modbus codes: https://shop.systemair.com/upload/assets/SAVE_MODBUS_VARIABLE_LIST_20190116__REV__29_.PDF
* Older HA code from GMTrevis: https://community.home-assistant.io/t/systemair-savecare-ventilation-unit/229653/2 
* New Node-Red/HA code from GMTrevis: https://github.com/GMTrevis/Homeassistant-NodeRed-Systemair-VTR300

HACS addons used:
* https://github.com/thomasloven/lovelace-card-mod
* https://github.com/custom-cards/button-card
* https://github.com/htmltiger/numberbox-card

Image of my Control Panel with full settings. A feedback check is added for Setpoints, with a comparison of the input number and the VTR sensor. Green when matching, Red when matching/waiting for sync.

<img src="https://user-images.githubusercontent.com/58105460/212387263-632d10fc-d7a7-40c7-b051-6ed2759dffb1.png" width="400">
<img src="https://user-images.githubusercontent.com/58105460/212497362-f8131aa3-9545-4121-bf9a-9b69df848d60.png" width="400">
<img src="https://user-images.githubusercontent.com/58105460/212497381-db61b45a-ba9b-4776-9699-40991e2d892b.png" width="400">




For the daily driver I have an overview with room cards displaying the operational state.

<img src="https://user-images.githubusercontent.com/58105460/211211807-b32b8dc6-8816-4dd9-9e3c-e7384acd6bf9.png" width="400">

With the room having a stripped down setup, linking via Config to the control panel.

<img src="https://user-images.githubusercontent.com/58105460/211211838-831058e2-42f3-409c-b5d5-5fb6a4974f4a.png" width="400">
