## Python Quick Reaction Game


**Introduction**

This project gives you the opportunity to use electronics to create a quick reaction game that you will program using Python. If you have little or no experience of creating circuits do not worry, this guide will walk you through it and by the end you will have a fun game to play with your friends.


**Requirements**

This guide assumes that you have the following:

- A Raspberry Pi
- Connected to a monitor or TV
- A keyboard and mouse
- A speaker or headphones
- An SD card with the latest version of Raspbian installed via NOOBS
- A half size breadboard
- LED
- A resistor
- Four female to male jumper wires
- Two male to male jumper wires
- Two tactile buttons


## Step 0: Set up your Raspberry Pi

You will need to set up your Raspberry Pi to take part in this activity. [See the Raspberry Pi Quick Start Guide here](http://www.raspberrypi.org/quick-start-guide) to get you up and running.


## Step 1: Connect the Components

Before using Python the program the game, you will need to connect the electronic components on a **breadboard** that has lots of holes in it allowing you to connect electrical bits together really easily.

**Activity Checklist:**

1. Begin by placing all the components on a desk and make sure that you have space to work. Lay the breadboard lenthways (landscape).

2. Take one of your tactile buttons and push it into the holes on your breadboard, with one set of legs on row 'a' and one set of legs on row 'c'.

3. Repeat the last step with the second button only placing it at the other end of the breabdoard on the same row. See the diagram below.

4. Place an LED with the longer leg in.. 


## Step 2: Controlling the Light

When programming it makes sense to tackle one problem at a time. This makes it easier to test your project at various stages. In this step you will use a python library to control the Raspberry Pi GPIO, set the mode of pin numbering that you are going to use, and then write a simple sequence to turn on and off the LED.

**Activity Checklist**

1. Open the Python programming enevironment **IDLE** by double clicking the desktop icon, or by using the main menu, selecting *Programming* and then *IDLE*. 
	
	**Note:** You could use IDLE 3 for this program but just make sure that in step 5 you use python 3 syntax for getting user input.  
	
	[!alt text](https://idle.png "Idle desktop icon")

2. Create a new test editor file by clicking on *File* and *New Window*

3. Save this file as **reaction.py** by clicking on *File* and *Save As* 

4. First you will need to import the modules and libraries needed to control the GPIO pins on the Raspberry Pi. Type:

	```python
	import RPi.GPIO as GPIO
	import time
	```
5. 	Make sure the GPIO pins are ready zion
	GPIO.setmode(GPIO.BOARD)
	```
6. 	As you are outputting to an LED you need to set up the pin that that the LED connects to on the Raspberry Pi as an output. First by using a variable to name the pin and then by setting the output:
	led = 23
	
	time.sleep(5)
	```
	









	import random
	``` 



The LED is working, now you want to add functionality to your program so that when a button is pressed it is detected. That way you can record the scores of the players to see who wins. The way do this is to have a loop that keeps going until one of the buttons is pressed.



	```python
	rightButton = 3
	leftButton = 5
2. Next set the buttons as input in the same way that you set the LED as output. Underneath `GPIO.setup(led, GPIO.OUT)` type:
	```python
	GPIO.setup(rightButton, GPIO.IN)
	GPIO.setup(leftButton, GPIO.IN)
	```
3. Then underneath `GPIO.output(led, 0)` add the button loop that waits until a button has been pressed:

	``` python

	Each time around this loop the Raspberry Pi checks if a button has been pushed and if one 	has then a statement is printed to the screen to indicate that it has been pushed.

	Notice that the line after `while` is **indented** (it has paces at the start). Python 	knows which lines are in the loop (and also for the `if` blocks) by how far they are 	indented, so make sure you put the spaces in correctly. The IDLE text editor should do 	much of this for you, but make sure you check it.

4. Save your program and test it with a friend.

## Step 5: Get Player Names


**Activity Checklist:**

1. To find out the names of the players you can use `raw_input` to ask the players to type in their names. Underneath the imported libraries and modules type:
	```python
	```
2. Next type the following code to put the inputted names into a list:	


4. Repeat the last step replacing `print "Right button pressed"` with `print names[1] + " won"`

	```python
	if GPIO.input(rightButton) == False:

