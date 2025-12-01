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

## Purpose

UsbBluetooth was created to:

- Provide direct control over USB Bluetooth devices using LibUSB.
- Enable OS independent device interaction for reproducible behaviour no mater the chosen platform.
- Enable custom HCI command crafting, including vendor specific commands.
- Facilitate fuzzing, reverse engineering, and protocol analysis.
- Support development in multiple languages with bindings for C, Python, and C#.

## Featured In

- **RootedCon 2025, Madrid**: Initial release presentation. Part of a broader initiative to improve tooling for Bluetooth security research. [Slides](https://github.com/TarlogicSecurity/Talks/blob/main/2025_RootedCon_BluetoothTools.pdf), [Blog](https://www.tarlogic.com/blog/hacking-bluetooth-the-easy-way-with-esp32-hci-commands-and-hidden-features/)
- **Hardwear.io 2025, Netherlands**: Used by Xeno Kovah as a tool to interact with and aid the reverse engineering process of some Realtek chips. [Publication](https://darkmentor.com/publication/2025-11-hardweario/), [Slides](https://darkmentor.com/2025-11-21_HardwearioNL2025_RTL8761B_RE_Slides_With_Builds.pdf)
