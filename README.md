# HomeAssistant-VTR-Modbus
Simple control of Systemair VTR(300) via modbus directly to HA.

Credits to GMTrevis who created the original code for Home Assistant, and then improved it for use via Node-Red.
The Node Red version has full control of the VTR, but I had issues where it overloaded my Node-Red. 
I found his incomplete Home Assistant code, and am working on filling it out for my own experiences.

Known Issues:
- Setpoint for Away not updated from Input
- Setpoint for Vacation not updated from Input
- Original code says Kitchen Fan is running when the Pressure system is active. Not looking into it, presumably just a change of name.



Sources:
Modbus codes: https://shop.systemair.com/upload/assets/SAVE_MODBUS_VARIABLE_LIST_20190116__REV__29_.PDF
Older HA code from GMTrevis: https://community.home-assistant.io/t/systemair-savecare-ventilation-unit/229653/2 
New Node-Red/HA code from GMTrevis: https://github.com/GMTrevis/Homeassistant-NodeRed-Systemair-VTR300
