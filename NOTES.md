# Notes

## Packages

### RAK

#### RAK7289V2 + RAK7267

* `kmod-usb-serial-ch341` = Required for Modbus (watchdog + solar battery status)

#### RAK7266 + RAK7267

* `kmod-usb-net-cdc-ether` = Required for cellular data on the Quectel EG915U (LTE Cat 1) modem, which runs in CDC-ECM mode rather than QMI

### Browan

#### MerryIoT Hotspot Miner V1

* `kmod-brcmfmac`, `brcmfmac-nvram-43430-sdio`, `cypress-firmware-43430-sdio` = Required for Wi-Fi on the AP6212A SDIO module (Broadcom BCM43430)
* `kmod-input-adc-keys`, `kmod-button-hotplug` = Required for the reset button, which is an ADC key on the SoC's SARADC channel 0 rather than a GPIO, so OpenWrt's GPIO button driver doesn't see it (the SARADC driver itself is built into the kernel)

### All targets

* `kmod-tun` = Required for OpenVPN
