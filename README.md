# Sailfish OS port to Redmi K20/Xiaomi 9T devices, LineageOS 16.0 based, aarch64

## About

Please read this document fully before planning or starting to use this port.

This is a community port, meaning that there is no official support and extensions included in the paid version:

* There is no Android app support
* There is no MS exchange support
* There is no Jolla Store predictive text support. Use Presage-based keyboards instead

## How to install

1. download sailfishos zip from [here](https://github.com/sailfish-on-davinci/main/releases/tag/0.5.0.0.43).    
2. download Lineageos 16.0 from [here](https://github.com/sailfish-on-davinci/main/releases/tag/0.5.0.0.43).
3. download twrp from [here](https://dl.twrp.me/davinci/), i perfet twrp-3.3.1-0-davinci.img.
4. revert to android9 base miui, and install twrp.(Mine is davinci_images_V11.0.3.0.PFJCNXM_20190926.0000.00_9.0_cn)
5. install Lineageos 16.0 and boot up to check if everything is ok.
6. reboot to TWRP, go to "Wipe -> Advanced Wipe -> Format `Data`.
8. Send sailfishos zip to your phone, flash it, and reboot.

### How to install waydroid

1. add chum repo `ssu ar sailfishos-chum https://repo.sailfishos.org/obs/sailfishos:/chum/5.0_aarch64/`.
3. `zypper ref` and `zypper in waydroid-runner waydroid-gbinder-config-hybris`, you can also install them via `Chum GUI`
4. run `waydroid init`, this takes some minutes to download lineageos images. Already have system.img and vendor.img? use [this way to init ](https://docs.waydro.id/faq/using-custom-waydroid-images)
5. run `systemctl disable --now dnsmasq`
6. ~~replace all `aidl2` to `aidl3` in `/etc/gbinder.d/anbox-hybris.conf`~~ (not needed now)
~~7. comment or delete `lxc.apparmor.profile = unconfined` in `/var/lib/waydroid/lxc/waydroid/config`~~
8. `systemctl restart waydroid-container`
9. open Waydroid from launcher, it should be working now.

#### How to use docker

https://github.com/sailfish-on-davinci/main/issues/19#issuecomment-3663276558

## Current state

### Working

* Audio
* Display
* Touch, multitouch
* Calls
* Cellular network
* LED
* Bluetooth
* GPS
* WLAN (connect and hotspot)
* GSM (SMS, voice, data)
* Keys (Vol +/-, camera, power)
* Power management
* USB Charging, Network, MTP
* Sensors
* Vibrator
* SD card (not tested)
* Waydroid
* Camera (Popup camera works too)
  
### Not Working

* FM radio
* Fingerprint




## Issues

https://github.com/sailfish-on-ginkgo/main/issues


## Buy me a coffee

Buy me a coffee to keep this project, thanks! https://paypal.me/birdzhang
