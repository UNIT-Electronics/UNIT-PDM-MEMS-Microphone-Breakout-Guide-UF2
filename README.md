# [UNIT PDM MEMS Microphone](https://github.com/UNIT-Electronics/UNIT-PDM-MEMS-Microphone-MP34DT05) Breakout Guide with UF2 File

<a href="https://github.com/UNIT-Electronics/UNIT-PDM-MEMS-Microphone-MP34DT05/blob/main/Hardware/UNIT_PDM_MIC-schematic.pdf"><img src="https://github.com/UNIT-Electronics/UNIT-PDM-MEMS-Microphone-MP34DT05/blob/main/Hardware/Schematics_icon.jpg?raw=false" width="500px"><br/> Schematics</a>

In this guide we are to connect an UNIT PDM microphone MP34DT05 module to the RP2040 microcontroller, following these steps:

First, make sure that you have all the necessary: an [UNIT PDM microphone module](https://github.com/Rabadan-uelectronics/UNIT-PDM-MEMS-Microphone), a [JST SH 4-pin cable 1 mm pitch](https://uelectronics.com/producto/conectores-sh1-0mm-con-cable-28-awg-15cm/) and the RP2040 microcontroller development board, we use a [DualMCU](https://uelectronics.com/producto/unit-dualmcu-esp32-rp2040-tarjeta-de-desarrollo/) board to make the example.

Locate the 4-pin JST connector for RP2040 microcontroller (GPIO12 and GPIO13 pins) on the DualMCU board ([Pinout](https://raw.githubusercontent.com/UNIT-Electronics/DualMCU/main/Hardware/Resources/EU0002-DUALMCU%20V3.1.2.jpg)). Connect the PDM microphone module to the DualMCU board using the four pin JST cable, following these connections:

* DualMCU (3.3V) to PDM-MIC (3.3V)
* DualMCU (GND) to PDM-MIC (GND)
* DualMCU (GPIO12) to PDM-MIC (SCL signal)
* DualMCU (GPIO13) to PDM-MIC (DAT signal)

![image](https://github.com/Rabadan-uelectronics/UNIT-PDM-MEMS-Microphone/blob/main/Hardware/MicConectionsJST1.jpg)

With these steps, you should be able to successfully connect your UNIT PDM microphone MP34DT05 module to the RP2040 microcontroller on the DualMCU board.

<img src="https://github.com/Rabadan-uelectronics/UNIT-PDM-MEMS-Microphone/blob/main/Hardware/Mic%26DualMCU.jpg?raw=false" width="1000px"><br/>

Power on the DualMCU board and the PDM microphone module.

Follow the next instructions and steps required to enable BOOT mode on the RP2040, and drag and drop [usb_microphone.uf2](https://github.com/UNIT-Electronics/DualMCU/blob/main/Software/UF2_Files/usb_microphone.uf2) file on the DualMCU board.

* **usb_microphone.uf2** is an example file that can be used to transform a development board like [UNIT DualMCU](https://github.com/Rabadan-uelectronics/DualMCU-RP2040-Arduino-Package/blob/main/releases/download/1.0.0/DualMCU-rp2040-1.0.0.zip), [the Raspberry Pi Pico](https://www.raspberrypi.com/documentation/microcontrollers/raspberry-pi-pico.html) into a high-performance USB microphone using the RP2040 microcontroller. This PDM Mic module, allows the RP2040 to function as an excellent microphone for use in video conferences or simply for entertainment, with very good sound quality. This file is particularly useful for those looking to add microphone functionality to their project or to explore the capabilities of the RP2040 microcontroller.


# Uploading UF2 example
To upload the usb_microphone.uf2 file onto your DualMCU, you will need to plug the USB-C cable into the DualMCU, move the mechanical USB selector to the “A” position, see section: 3.11 Mechanical selector for the USB Communication of the [Product Reference Manual](https://github.com/UNIT-Electronics/DualMCU/blob/main/DualMCU(Product%20Reference%20Manual).pdf) and press and hold the RP2040 reset button (PB1), you can find it onboard with the label “RST”

![image](https://github.com/UNIT-Electronics/DualMCU/blob/main/Docs/RP2040-Reset_BUTTON.jpg)

Without release the RESET, with the other hand, press and hold the RP2040 boot button (PB2) labeled “BOOT”

![image](https://github.com/UNIT-Electronics/DualMCU/blob/main/Docs/RP2040-Enter_Bootloader_mode.jpg)

Then hit the RST and BOOT buttons, you will see a new windows appears and then drag and drop the usb_microphone.uf2, the file should be transferred and start to run.

![image](https://github.com/UNIT-Electronics/DualMCU/blob/main/Docs/RP2040-Boot_button.jpg)

Once the file finished to uploading, go to device manager a you can see your DualMCU recognized as UNITMic as show in the following image:

![image](https://github.com/Rabadan-uelectronics/UNIT-PDM-MEMS-Microphone/blob/main/Hardware/DeviceManager.jpg)
 
Now you are ready to start and enjoy using your UNIT PDM microphone as a USB microphone, we recommend that you use the following online audio recorder to do some testing:

[https://online-voice-recorder.com/es/](https://online-voice-recorder.com/es/)

![image](https://github.com/Rabadan-uelectronics/UNIT-PDM-MEMS-Microphone/blob/main/Hardware/RecordedAudio.jpg)

# THANKS!

