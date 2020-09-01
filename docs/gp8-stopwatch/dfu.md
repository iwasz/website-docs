---
layout: default
title: Device firmware update
parent: Gp8 stopwatch
nav_order: 3
---
# Firmware
The newest firmware can be always [found here](https://github.com/gp8-stopwatch/receiver-firmware/releases). Always pick up the newest one.

# Windows
Install [ST's DFU program](https://www.st.com/en/development-tools/stsw-stm32080.html) (login required). Run the program. A window will pop up:

![Main DFU window](01.png)

Connect the stopwatch, and then turn it on **holding the button pressed on**. The stopwatch should then be recognized and it should show up in the combo box as depicted below. The screen does not lit up in this mode :

![Stopwatch attached](02.png)

Pick a firmware file you want to use. The newest firmware can be always [found here](https://github.com/gp8-stopwatch/receiver-firmware/releases).

![Main DFU window](03.png)

Simply click the "Upgrade" button:

![Main DFU window](04.png)

Click "Yes" if the popup like shown below shows up:

![Main DFU window](05.png)

# Linux
Manjaro : install `dfu-util` and run it as so:

```sh
dfu-util -D receiver.dfu -a0
```
