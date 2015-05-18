Onboard
=======

This is an onboarding app based on https://github.com/chriscook8/esp-arduino-apboot
The changes relative to that version are as follows:

0. Restructured some of the code to (hopefully) make it a little more understandable
0. Don't store the ssid and password in EEPROM since the ESP8266 SDK already stores them if wifi_station_set_auto_connect is set to true (this is the default behavior), see http://www.esp8266.com/viewtopic.php?p=15304 for details
0. Support ssid and password containing spaces
0. Restart the node in WIFI_STA mode once the ssid and password have been configured and a successful connection to that AP has been established.
0. Once restarted advertise the address via mDNS
