---
layout: default
title: 7 segment Display
parent: Gp8 stopwatch
nav_order: 3
---
During startup the device shows a little intro:

GP8
{: class="dseg7"}

Right after powering on, the stopwatch is in the main mode (let's call it a stopwatch mode). Depending on the conditions it either can:

Display zeroes which indicates that it sees the IR beam and is ready:

00.00.00
{: class="dseg7"}

Display "no beam" message which means, that there is no IR signal seen by one of the receivers (either built-in or external):

nobeam
{: class="dseg7"}

Display "blind" message when the internal IR sensor has been disabled and no external ones are attached. 

blind
{: .dseg7}

Display "noise" message which indicates, that the IR beam is disturbed in some way. This can be caused either by intense sunlight shining directly into the sensor or some other spurious IR signals. Note, that some digital cameras and cellphones can emit IR light:

noise
{: class="dseg7"}

Display "cable" message which indicates that there's a problem with an external peripheral connection. Check for loose cables and if [terminators are set correctly](gate-setup.html). 

cable
{: class="dseg7"}

To cycle through the available menu options, you press the button briefly (a *short-press* later on throughout the docs). To change the setting, you usually press the button once, but this time a little longer (*long-press* later on). This works for boolean settings like *sound on/off* or *IR on/off*. There are settings that are changed slightly differently, so read on.


Stopwatch mode
: in this mode, the stopwatch waits for the IR beam, or for external sensors to be connected and does its usual job of tracking time in case of a trigger event. This is the mode described above.
  >*Short-press* for the next mode.

Results mode
: this mode lets you cycle through up to 64 results that are stored in the flash. In case of flash being empty, you get the <span class="dseg7">empty</span> message on the screen. Upon entering this mode, the most recent result is displayed, (or *empty*). To display the second result, you have to *long-press* the button, and then cycle through the rest using a *short-press*. Last result in the memory is indicated by the <span class="dseg7">end</span> message.
  > *Long-press* to display the second result, and enter the *cycling through all results* mode. *Short-press* to show the third and every consecutive result. Finally *long-press* to exit the *cycling through all results* mode and go to the next mode. 
  
  > *Short-press* for the next mode.

Screen orientation mode

: lets you flip the display upside down and right side up again by using a *long-press*. In this mode the display shows : <span class="dseg7">1.flip</span>
  > *Long-press* changes the screen orientation.

  > *Short-press* for the next mode.

Built-in IR sensor mode

: lets you to turn the built-in IR sensor on and off. Simply *long-press* to change between the modes. Screen indicates <span class="dseg7">2.i.r.on</span> and <span class="dseg7">2.i.r.off</span> respectively. Remember that the internal sensor can pick up unwanted IR signals when no transmitter is emmiting a beam onto it. 
  > *Long-press* changes the setting.

  > *Short-press* for the next mode.

Buzzer mode

: is used to turn the buzzer on and off. *Long-press* changes the setting which is indicated on the screen accordingly : <span class="dseg7">3.sn.on</span> or <span class="dseg7">3.sn.off</span>.
  > *Long-press* changes the setting.

  > *Short-press* for the next mode.

Resolution mode

: In this mode you can change the resolution of the time on the 7 segment LED display. Note, that internally all the results are sored using the most presice, 10µs variant. The default displayed resolution is the lowest one. Lets list them in order:\\
<span class="dseg7">4.10ms</span> stands for 10ms and corresponds to <span class="dseg7">00.00.00</span> in the main mode.\\
<span class="dseg7">4.1ms</span> stands for 1ms and corresponds to <span class="dseg7">0.00.000</span> in the main mode.\\
<span class="dseg7">4.100us</span> stands for 100µs and corresponds to <span class="dseg7">00.0000</span> in the main mode.\\
<span class="dseg7">4.10us</span> stands for 10µs and corresponds to <span class="dseg7">0.00000</span> in the main mode.\\
Note, that the 10µs is below the true resolution of the IR trigger (around 75µs).
  > *Long-press* changes the setting.

  > *Short-press* for the next mode.

Mode of operation

: This mode lets you choose between the *stop* mode (indicated on the display as <span class="dseg7">5.stop</span>) and the *loop* mode (<span class="dseg7">5.loop</span>). In the former mode, the device acts as a stopwatch i.e. it starts the time after first trigger, and stops entirely after the second displaying the result. The result is displayed until the next trigger event. In the latter mode, at the other hand, it starts on the first trigger event, and does not stop. On the every next trigger the device displays the recent result briefly, and continues to run. Note, that the last 64 results are always stored in the flash memory, and can be reviewed either via USB or on the LED display.
  > *Long-press* changes the setting.

  > *Short-press* for the next mode.

Time mode

: This mode shows the current time in HH.MM.SS format. 
  > *Long-press* changes the setting.

  > *Short-press* for the next mode.

Date mode

: This mode shows the current date in yy.mm.dd format. 
  > *Long-press* changes the setting.

  > *Short-press* for the next mode.

