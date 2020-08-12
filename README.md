OpenBCI-AndroidStudio 4.01
==================
This is a 2020 port of https://github.com/yeah-sir/OpenBCI-AndroidApp
with updated permissions + checking and apk file of easy installation.

I would like to add OpenBCI to my universal BCI app https://robosoft.de/eegcenter 
which allready supports 
1. Muse EEG headband
2. Melon EEG headband
3. Emotiv Insight.

My "central station" is intended for neuro feedback and multiple mind commands that can not only be recorded but trained via neuro feedback !

So it would be nice if someone would test this code/apk and give me feedback.
For example it looks like this code will only read 6 channels of EEG raw data, see class SaveBytesToFile. So i am not sure what hardware this app connects to via the RFduino :-/

Robo Durden, Germany, the little physicist :-)

OpenBCI-AndroidApp
==================
This Android application demonstrates the capability of interfacing an RFduino with an Android app to store processed data as comma separated values onto the file system.

This work is based on the work done by Lann Martin found here: https://github.com/lann/RFDuinoTest 

Description
=================
MainActivity: the main activity class for the Android app

SaveBytesToFile: an AsyncTask to store processed data onto a file

RFduinoService: Android service to connect, display data, and display GATT services and characteristics supported by the RFduino via the Android BLE API

OpenBCIDataConversion: helper class to convert byte data received from RFduino into microvolt values

FormatDataForFile: helper class to convert the process data into comma separated values

BluetoothHelper: RFduino specific Bluetooth computation

HexAsciiHelper: helper class to convert bytes to hex/ASCII values

Usage
=====
-Turn on the Bluetooth using the “Enable Bluetooth" button

-Press “Scan” to begin a BLE scan for GATT servers on devices

-When an RFduino is found, some of the device information will be displayed under “Device Info”

-Press “Connect” to connect to the RFduino

-You can either type in your command using the text input provided or press “Start” to send a “b” (begin) command to the RFduino

-Click “Stop” to send a “s” (stop) command to the RFduino

-Press “View File” to open the data file for the current session and use your favorite text viewer to view the “.csv” file

Note: All files are stored under an “OpenBCI” folder in the file system. The files are name “openbci<timestamp>” where the time stamp is in the "yyyy_MM_dd_HH_mm_ss" format.

References
==========
https://developer.android.com/guide/topics/connectivity/bluetooth-le.html

https://developer.bluetooth.org/TechnologyOverview/Pages/BLE.aspx


