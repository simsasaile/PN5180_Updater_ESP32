# PN5180 Firmware Updater Using ESP32 and Arduino IDE

This Project **Modify** From PN5180 Secure Firmware Update Library (SW4055). 

Prerequisites: set up ESP32 to work with Arduino IDE

**Tested ON**
+ ESP32-DevKitC v4 board (ESP32 WROOM 32D Module)
+ PN5180 (also named PN5180 R1.1-170710, cheap PN5180 board from amazon/ebay/aliexpress)

You should be able to use any other ESP32/ESP8266. 

# How To Update
1. Download NFC Cockpit And Get The PN5180 Firmware File (*.sfwu) In PN5180_SFWU Folder.
2. Convert .sfwu To C Array Of Bytes By This Website https://tomeko.net/online_tools/file_to_hex.php?lang=en
3. Save And Include As Header.
Step 1,2,3 is already done. The firmware included with the project is 4.1. 
4. Connect PN5180 Module To ESP32: GND and 3.3v (no need to supply 5v to reader for firmware upgrade) to 3.3v and ground of ESP32, SCLK to pin 18, MISO to pin 19, MOSI to pin 23, NSS to pin 5, BUSY to pin 16, Reset to pin 17, REQ to pin 4 of ESP32. 
5. Run dumpmodule.ino to read eeprom, DieID, current Firmware versions and such
6. Run FirmwareUpgrade.ino to upgrade.


Godspeed 
