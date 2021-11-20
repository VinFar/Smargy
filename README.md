# Smargy IoT Smartmeter Reader

<img src="https://github.com/VinFar/SML_Reader_V2.0/blob/master/Beispielanlage.png" width="100%"/>
This Project is a continuation of the second version available [here](https://github.com/VinFar/SML_Reader_V2.0)

# Introduction
This Repo is about a eco-system for reading out the upcoming electrical [SmartMeter](https://discovergy.com/blog/was-ist-ein-smart-meter). With this device it is possible to read out SmartMeter over the optical interface that is present on all meters.

It is part of an eco-system consisting of the following features:
- This IoT-Device for reading out the Smartmeters (Vincent Fartmann)
- Database for storing the time-based Data (InfluxDB) (Simon Wüllhorst)
- Grafana for visualization the data coming from the Readers (Simon Wüllhorst)
- Prediction of power generation if a photovoltaic plant exists (Simon Wüllhorst)
- Web-Interface with GUI (PC and Smartphone) for usability (Christian Wunder)

The IoT-Device (referred as Reader) is briefly described here:

# Pictures

<img src="Reader.jpg" width="50%"/><img src="34Schnitt.png" width="50%"/>

# Features

## Hardware Features
- Iot-Functionality with WiFi
- STM32L432KC as MCU
  - Flash (256KB) and RAM (48+16KB) is already 98% used
  - We need more RAM!!!
- OLED Display
- SD-Card Slot
- EEPROM for storing critical data
- Powersupply over Micro-USB
- RTC with Backup Battery
- Possibility to read Smartmeters and Ferrarris Meter
- Stacked PCBs
  - This allows development of different Wireless Modules (WiFi, GSM, LoRa, ZigBee, DECT etc...) which are interfaced by the MCU  

<img src="OhneHousing.png" width="33%"/><img src="MiddlePCB.png" width="33%"/><img src="TopPCB.png" width="33%"/>

## Software Features
- FreeRTOS as operating system
- IP Stack
- SD-Card Interface using FatFS
- OTA-Update of Firmware (currently in development)
- Telnet Server for command-line-interface
- TCP Debugging Stream to Server
- Creating of HttpServer for Wifi SSID and PW input
- DMA Transfers for USART and I2C
- Fast-Fourier-Transformation for detection of Ferrarris reader
- QR-Code Generation for pairing device with a specific user
- Offline mode using SD-Card
- Printf functionality

<img src="pairing_qr_code_scan.png" width="50%"/>

<img src="Telnet.png" width="50%"/><img src="TCPTerminal.png" width="50%"/>


This Readme will be filled with content in the next time 

