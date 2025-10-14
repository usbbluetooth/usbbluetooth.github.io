---
layout: page
title: Platform Quirks
permalink: /quirks/
---

UsbBluetooth uses LibUsb underneath for USB communication (see [Architecture](/architecture/). Due to this, there are some platform-specific requirements and quirks to be aware of.

## Windows

On Windows, UsbBluetooth will be able to list all Bluetooth devices available in the system but will only be able to open devices that have the WinUSB driver installed.

If a device fails to open, please, verify that WinUSB is the driver currently installed for that device. Otherwise, you may install it using the [Zadig](https://zadig.akeo.ie/).

## Linux

On Linux, the user must have access to the USB devices to be able to opnen them. Several options to achieve this are available:

- **Run as root**: Use `sudo` to run the application with elevated privileges. Note that this may not be ideal for security.

- **Add user to a group**: Add your user to the `plugdev`, `usb`, or `uucp` group (depending on your distribution). Remember to reboot or log out and back in for changes to take effect. For example:

  ```
  sudo usermod -a -G plugdev $USER
  ```

- **Create a udev rule**: Create a custom udev rule for automatic permissions. Create `/etc/udev/rules.d/99-usbbluetooth.rules` with:

  ```
  SUBSYSTEM=="usb", ATTR{idVendor}=="your_vendor_id", ATTR{idProduct}=="your_product_id", MODE="0666"
  ```

  Replace with actual IDs (use `lsusb` to find them). Then reload rules:

  ```
  sudo udevadm control --reload-rules && sudo udevadm trigger
  ```
