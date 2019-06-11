# HotPi
## Hardware set-up
### Relays
```
sudo su -
echo pcf8574 0x20 > /sys/bus/i2c/devices/i2c-1/new_device
i2cdetect -y 1
for i in $(seq 504 511) ; do echo $i /sys/class/gpio/export ; done
for i in $(seq 504 511) ; do echo in /sys/class/gpio/gpio$i/direction ; done
```

