# Designing Interactive Devices Lab1: Make it blink!

Lab report for the first IDD lab by Fabio Daiber


## Part A: Setting up the board 

![alt text](https://github.com/fpdaiber/IDD_Lab1/blob/master/Overview.jpg)


## Part B: Manually Blink an LED

### a. What color stripes are on a 270 Ohm resistor?
•	Red for 2 as 1st value
•	Violet for 7 and 2nd value
•	Black for 0 as 3rd value
•	Black for 1 as multiplier
•	Brown for -2% tolerance

### b. What do you have to do to light your LED?
I have to press the button to complete the circuit. 


## Part C. Blinking an LED using Arduino 

### Blink the on-board LED

#### a. What line(s) of code do you need to change to make the LED blink (like, at all)?

I needed to change the parameter digitalWrite(LED_BUILTIN, HIGH) to HIGH.

#### b. What line(s) of code do you need to change to change the rate of blinking?

I change the rate of blinking by chaning the value of delay

#### c. What circuit element would you want to add to protect the board and external LED?

We want to add a resistor to protect it from frying. 

#### d. Change the delay parameter to modify blink rate of your LED to make it blink faster. At what delay can you no longer perceive the LED blinking? (And how can you prove to yourself that it is, in fact, still blinking?

With a delay of 15ms I could barely still detect it flashing, with 10ms I can no longer detect it flashing. By taking a video, you can check if it is still flashing as the picture fps are not high enough.

[Video proof](https://drive.google.com/file/d/1rShkwkkIYeimTYln_pymeBtIXzmQfCBs/view?usp=sharing)

#### e. Modify the code to make your LED blink your way.

[BlinkMyWay Code](https://github.com/fpdaiber/IDD_Lab1/blob/master/Blink.ino)


### 2. Blink your LED

# Video missing!!!


## Part D. Manually fade a LED

[Manual fading video](https://drive.google.com/open?id=1eic9VNwoTOcWFWR3KyC3RD8JYtNe1lD9)


### a.	Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?
No, the LED turns off if the potentiometer is on the highest resistance because the resistance consumes all the current and the LED does not light up anymore.


## Part E. 

### a. What do you have to modify to make the code control the circuit you've built on your breadboard?

I had to change the led variable to 11.

```C++
int led = 11;           // the PWM pin the LED is attached to
```

### b. What is analogWrite()? How is that different than digitalWrite()?
The analogWrite allows us to control the brightness of the LED by toggling the LED on and off in a range from 255 to 0 so fast that it looks like the LED is fading. It lets us use the Arduino like a potentiometer whereas the digitalWrite only allows to turn it on or off (5v and 0V).


## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside.
#### a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"

#### b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?

#### c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?

#### d. Is information stored in your device? Where? How?

## 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.


### 3. Build your light!


# Make a video showing off your Frankenlight.

# Include any schematics or photos in your lab write-up.
