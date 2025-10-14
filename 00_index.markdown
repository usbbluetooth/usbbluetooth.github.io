---
layout: home
permalink: /
---

<p align="center">
  <img src="/assets/img/logo.png" style="max-height:200px;" />
</p>

## Take full control of your USB Bluetooth controllers!

UsbBluetooth is a LibUSB based Bluetooth device driver that allows you to interact directly with USB Bluetooth dongles.

It bypasses traditional OS level Bluetooth stacks, enabling low level access to HCI commands and vendor specific extensions.

This project was first presented at RootedCon 2025 as part of a broader initiative to improve tooling for Bluetooth security research. See the [original slides](https://github.com/TarlogicSecurity/Talks/blob/main/2025_RootedCon_BluetoothTools.pdf) of the talk.


## Purpose

UsbBluetooth was created to:

- Provide direct control over USB Bluetooth devices using LibUSB.
- Enable OS independent device interaction for reproducible behaviour no mater the chosen platform.
- Enable custom HCI command crafting, including vendor specific commands.
- Facilitate fuzzing, reverse engineering, and protocol analysis.
- Support development in multiple languages with bindings for C, Python, and C#.
