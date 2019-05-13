# Ender-3-BL-Touch-Installation
Instructions and Firmware For The Ender 3 BL Touch Installation

## General Notes

## Flashing The Bootloader 

Please follow these steps to flash the bootloader of the Arduino Uno: 

### Configuring the Arduino 
1) Download and install the Arduino IDE from: https://www.arduino.cc/en/Main/Software
2) Plug your Arduino Uno into your computer.
3) Open the Arduino IDE. Under File > Preferences, tick off "Show verbose output" during both compilation and upload. 
4) Open the sketch "Arduino ISP" From File > Examples > Arduino ISP.
5) Configure for upload. From Tools > Board Select "Arduino/Genuino Uno. From Tools > Port select the COM port for your Arduino. It will probably be the only one listed. If there are multiple ports, try uploading to a different port if the selected one doesn't work. 
6) Click the "Upload" button (The second button from the left at the top of the program, the arrow pointing right). 

### Flashing the Bootloader 

Now that we have configured the Arduino Uno with the proper software, we are going to use it to put a bootloader onto the Ender-3 Motherboard. This will allow us to flash our Marlin firmware to our ender directly from the USB port in the front of the printer. 

1) In the Arduino IDE, go to File > Preferences. Under preferences you will see a field called "Additional Boards Manager URLs". Copy and paste the following link into that field, then click : https://raw.githubusercontent.com/Lauszus/Sanguino/master/package_lauszus_sanguino_index.json
2) Go to Tools > Boards > Boards Manager. Search for "Sanguino", then install the latest version. 
3) Under Tools, select Boards > Sanguino. Then select Processor > ATmega1284 or ATmega1284P (16 MHz). Finally, select Programmer > Arduino as ISP. 
4) Select Tools > Burn Bootloader. If the process is successful you will get no errors.

## Flashing Marlin

Marlin is the software that runs our 3D Printer. Luckily, we have provided a pre-compiled version for you so you don't have to mess with the code - just upload! 

1) Plug your Ender-3 into your USB port.
2) 
