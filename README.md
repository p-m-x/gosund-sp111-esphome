# gosund-sp111-esphome
https://www.malachisoord.com/2019/11/24/flashing-custom-firmware-on-a-gosund-sp111/

1. Backup existing fimware 
```
sudo esptool.py --port /dev/ttyUSB0 read_flash 0x00000 0x100000 <name-of-backup>.bin
```
2. Erase flash
```
sudo esptool.py --port /dev/ttyUSB0 erase_flash
```
3. Compile & upload espHome 
```
esphome sp111-esphome.yaml run
```
