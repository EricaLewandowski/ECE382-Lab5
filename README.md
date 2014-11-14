ECE382-Lab5
===========

#Day 1

The purpose behind the first day's work was to collect data from the IR sensor. The IR Sensor was connected to the MSP430 to receive inputs from a remote control. Using the oscilloscope combined with the computer program tes5.c information on pulse lengths was collected, as seen in Table 1. Table 2 contains data on what hex codes were transmitted when various buttons were pressed, which is more relevant to day 2's work. 

Table1

|Pulse | Duration | Timer A Counts |
|------|----------|----------------|
|Start Logic 0  |  9.1 ms |  9045 |
|Start Logic 1  |  4.6 ms |   4491 |
|Data 1 Logic 0 |   580 us |   591 |
|Data 1 Logic 1 |   1.66 ms |  1662 |
|Data 0 Logic 0 |   600 us  |  592 |
|Data 0 Logic 1 |   540 us  |  534 |
|Stop Logic 0   | 590 us  |  586 |
|Stop Logic 1   | 39.9 ms |  39318 |

Table2

| Button | Code |
|--------|------|
|0  | 0x2FD00FF |
|1  | 0X2FD807F |
|2  | 0X2FD40BF |
|3  | 0X2FDC03F |
|POWER  | 0X2FD48B7 |
|VOL+   | 0X2FD58A7 |
|VOL-   | 0X2FD7887 |
|CH+  | 0X2FDD827 |
|CH-  | 0X2FDF807 |

#Day2

On day two, the data collected above was input into the code shells given: start5.c and start5.h. Our task was to modify the code to toggle both LED lights on the MSP430 using different buttons on the remote control. 

#Code Walk Through

the code is broken up into three main parts. The first, and most important is the main function. Main contains the if statements instructing the LEDs when certain buttons are pressed. For my code, the Ch+/Ch- turned on the red LED and Vol+/Vol- toggled the green LED. The second is the Port2Vector function which controls the Timer A Register. The timer is set to turn on and off and take readings, in this case, IF readings on both the positive and negative edges and classiofy them. Lastly the Timer0_A1Vector function. This function controls when the timer flag is set and when it is cleared. 

#Debugging

I had a lot of trouble with this lab, partly because I was under the weather during the process. I referenced a lot of the other programs we've been given and taught so as to not mess up the syntax. In addition, while testing, I had to reprogram the button input codes because my remote couldn't be found. 

#Observations/Conclusions

Once the program finally worked, the Ch+ button turned on the red LED, and the CH- turned off the LED. The Vol+/Vol- were programmed similarly except for the green LED. 

#Documentation

Dr Coulston helped me in EI two different times, in addition to help in the lab. 

#Commit History
... Uhh yeah. 
