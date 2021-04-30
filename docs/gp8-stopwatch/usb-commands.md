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
# `factory`
# `battery`

# Settings (persistent)
# `flip`
# `ir`
# `sn`
# `res`
# `bright`
# `blind`
# `fps` (experimental)
# `trigger` (experimental)

# Other commands
# `help`
A help message showing possible commands.
# `auto`
# `periph`
