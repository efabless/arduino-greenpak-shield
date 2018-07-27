# Programming

## Generating the device configuration

First, you need to generate the configuration that gets loaded onto your SLG4682X device, it has a dizzying array of registers to use to connect things luckily Dialog provides the excellent [GreenPAK Designer Suite](https://www.dialog-semiconductor.com/greenpak-designer-software) available for free. It provides an easy drag and drop interface for creating device configurations. It also includes powerful analysis and simulation tools to help debug and verify your device.

![GreenPAK](img/GreenPAK.png)

## Exporting your configuration to an Arduino sketch

To export your configuration to an Arduino for programming you need to export it from GreenPAK Designer, you can do this by selecting File -> Export -> Export NVRAM. You then need to run `python "NVRAM to arduino.py" <exported file>` it will generate a `SLG4682X_Conf.h` file that you can use in your sketch to write to the configuration EEPROM on the device over I2C.