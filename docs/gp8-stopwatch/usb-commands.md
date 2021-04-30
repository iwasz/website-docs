---
layout: default
title: USB serial options
parent: Gp8 stopwatch
nav_order: 2
---
To see how to install drivers and then issue commands under Windows or Linux see [USB drivers installation](usb-drivers.html). All commands are case insensitive, but here are presented using "camelCase". 

# Results
## `result`
The `result` command shows all the results stored in the flash memory. The maximum number of entries is 64, and all are stored along with date and time. If all 64 slots are full, the oldest result is discarded to free memory for the most recent one. The results are given in seconds and fractions of a second. This is the most precise format the stopwatch can output. Example output is presented below:

```
result
Best 00:05.04999

1 2021-02-03 11:02:06 00:05.05003
2 2021-02-03 11:03:16 00:05.05000
3 2021-02-03 11:04:24 00:05.04999
```

## `resultMs`
The `resultMs` works almost the same as the `result` with the only difference in time units displayed. In this case, all the results are given in milliseconds. Note that this format is less precise than the other.

```
resultMs
Best 5050

1 2021-02-03 11:02:06 5050
2 2021-02-03 11:03:16 5050
3 2021-02-03 11:04:24 5050
```

## `clear`
This command removes all the results from the flash.

## `last`
The `last` command shows the most recent result stored in the flash. The result is displayed in seconds (with the fractional part). Example output might look like that:

```
last
00:08.01655
```

## `lastMs`
The `lastMs` command shows the most recent result stored in the flash. The result is displayed in milliseconds. Example output might look like that:

```
lastms
8017
```

## `isCounting`
The `isCounting` command returns `1` if the stopwatch is running. If it's not, the command will output `0`. 

## `date`
`date` outputs actual date and time in the `YYYY-MM-DD HH:mm:ss` format. For now, this command accepts no arguments, and so the date and time can be set only from the [on-screen menu](screen-menu.html).

# Device state
# `reset`
Resets the stopwatch. Whether the device is currently running or displaying the last result, this command will reset it, and `000000` will appear on the display.

# `battery`

# Settings (persistent)
# `factory`
Clears all the persistent settings from the flash. All settings are thus restored to their default state, which is equivalent to issuing the following set of commands:

```
res 10ms
bright auto
mode stop // This is currently not implemented
auto none
flip 0
ir 1
sn 1
blind 5000
trigger 10
fps 30
```

All the commands for storing persistent settings are described below.

# `flip`
The command `flip 1` flips the font displayed on the LED display upside down (except for the coma sign). The command `flip 0` restores the display right side up again. The `flip` without any arguments shows the current value of the setting.

# `ir`
Every stopwatch receiver has an IR sensitive element on the left side (there's an orifice on the left wall which prevents unwanted DC ambient light getting inside). This built-in sensor may be turned off, issuing the command `ir 0`, or turned on by using `ir 1`. `ir` without any arguments shows the current value of the setting.

It is very important to remember to turn the built-in sensor off (the default) if it is not needed, for example, when using an external sensor. This is to prevent unwanted IR signals from interfering with the device. 

Another possibility is to set up a system consisting of the receiver (a stopwatch with a display with it's internal sensor turned on) + transmitter as a gate 1 and additionally external receiver + another transmitter as a gate 2. [See ... for more info about possible setups]().

# `sn`
This command follolwed by an argument `1` or `0` turns the built-in buzzer on or off. The `ir` without any arguments shows the current value of the setting.

# `res`
The command `res` sets the resolution presented on the LED screen (and only there). It can be followed by an argument:

* `10ms` (the default)
* `1ms`
* `100us`
* `10us`

Issuing the command without any parameters outputs the value of the setting. 

# `bright`
The command `bright` governs how bright is the LED display. It accepts single argument which has five possible values: 

* `1` the dimmest
* `2`
* `3`
* `4` the brightest
* `auto` the brightness is adjusted automatically according to the built-in photo-resistor located near the buzzer (the default)

Issuing the command without any parameters outputs the value of the setting. 

# `blind`
# `fps` (experimental)
# `trigger` (experimental)

# Other commands
# `help`
A help message showing possible commands.
# `auto`
# `periph`
