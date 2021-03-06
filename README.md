# IoT Hub Pi Hands on Lab (HoL)

## Overview
This Hands on Lab (HOL) demonstrates connecting a Raspberry Pi running Raspian to [Azure IoT Hub] (https://azure.microsoft.com/en-us/services/iot-hub/) and sending telemetry to Azure IoT Hub from either:
- a physical [Sense HAT](https://www.raspberrypi.org/products/sense-hat/) connected to the Raspberry Pi; or
- a [Sense HAT Emulator](https://www.raspberrypi.org/blog/sense-hat-emulator/) installed on the Raspberry Pi.

Completing this HOL will provide you with the basic skills needed to connect and securely send telemetry from a physical device (e.g. a field device or field gateway) to the Azure IoT Hub. This HOL does not demonstrate what can be done with the data after it arrives at the Azure IoT Hub. Having said that, you can do almost anything including complex event processing, stream processing, saving telemetry to blob storage or databases, analytics, training of Machine Learning models etc.

### Why Sense HAT?
We didn't want you to mess around with breadboards, jumper cables, resistors etc. This just wastes time and adds nothing to the goal of connecting a sensor to Azure IoT Hub. The Sense HAT has all the necessary components installed on the circuit board, including a ready to use library, and a series of sensors to play with.

### Why HTTPS and REST?
For simplicity and to avoid downloading/compiling SDKs during the HOL, we chose to send the Sense Hat telemetry to Azure IoT Hub using the [IoT Hub REST API](https://docs.microsoft.com/en-us/rest/api/iothub/) over HTTPS. Of course, you can use one of the many device SDKs available, which support sending messages over AMQP and MQTT. If you want to use the device SDKs, refer to the Using the .NET Device SDK section below.

## Lab Requirements
- [Raspberry Pi 3 Model B](https://www.raspberrypi.org/products/raspberry-pi-3-model-b/) or [Raspberry Pi Zero W](https://www.raspberrypi.org/products/raspberry-pi-zero-w/) (Pi 2 Model B with USB Wi-Fi dongle will probably work as well) with latest version of Raspian installed on the micro SD card. Using [NOOBS](https://www.raspberrypi.org/downloads/noobs/) works fine. 
- [Sense HAT Emulator](https://www.raspberrypi.org/blog/sense-hat-emulator/) (which comes with the Raspian O/S)
- [Sense HAT](https://www.raspberrypi.org/products/sense-hat/) (optional - for those that want to play with real hardware). You can order the Sense HAT from a variety of online sites such as adafruit.com, amazon.com etc. Please order yours 3-4 weeks in advance of the HOL so it will arrive in time.
- Laptop (running whatever operating system you desire) but ideally running Windows so you can install/run [Device Explorer](https://github.com/Azure/azure-iot-sdk-csharp/tree/master/tools/DeviceExplorer). 
- [PuTTY] (http://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) or another SSH client.
- If you are using the Sense HAT Emulator (vs the physical device), you'll need to install VNC viewer on your laptop so that you can remotely view your Raspbian desktop. Download and install RealVNC from (https://www.realvnc.com/download/viewer/)
- An corporate Azure subscription. You can use a corporate MSDN Azure subscription or a subscription from your company. 
- A PowerBI account (same account as the corporate Azure account).
- A basic understanding of Python and Linux.

## Pre-workshop Setup (Steps must be completed before the Hands On Lab Workshop)

Follow the instructions [here](/Prep) before you arrive on-site for the hands-on-lab workshop. 


## Hands on Workshop Steps

The following subsections of the Hands on Labs are as follows: 

### Morning

 * [1 - Hands on Lab Setup](/1)

 * [2 - Remote Monitoring Pre-configured Solution](/2)<br>

 * [3 - Connect Raspberry Pi to Azure IoT](/3)

### Afternoon

 * [4 - Stream Analytics](/StreamAnalytics)

 * [5 - Azure Functions](/AzureFunction)
 
 * [6 - Lab Clean-up](/Cleanup)
