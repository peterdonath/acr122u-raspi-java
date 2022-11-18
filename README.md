# acr122u-raspi-java
How to make ACR122U work with java on raspberry

1. Step
https://www.acs.com.hk/en/driver/3/acr122u-usb-nfc-reader/

Install driver from here

in the absence of bullseye I install buster

apt install pcscd pcsc-tools

sudo rm -r /lib/modules/5.15.0-53-generic/kernel/drivers/nfc/pn533/

sudo sh -c "echo '1-4.2:1.0' > /sys/bus/usb/drivers/pn533_usb/unbind"
