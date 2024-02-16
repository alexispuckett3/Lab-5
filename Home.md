# Lab 5: Microcontrollers
* Alexis Puckett
* Hannah Markwell
February 15, 2024

## Project Summary:
The purpose of this lab is to obtain knowledge of how to use microcontrollers. This lab is allowing us to obtain this knowledge by using various circuits and components. This lab allowed the use of the Arduino as the microcontroller, with that being said Arduino IDE was also needed in this lab in order to help gain more knowledge on how to use microcontrollers. The Arduino system allows us to be able to program and use different types of microcontrollers. With this knowledge, this lab will and has allowed us to gain a better knowledge of how to use and code in the Arduino system as well as learn about microcontrollers. In this lab, the use of a Light Emitting Diode (LED) will allow us to see how our code in Arduino IDE is working and how it is shown throughout the circuits that are constructed. In partnership with the LED, a photoresistor is also used. This allows the circuit's resistance to change based on the amount of light that is being sensed and detected by it. Finally, Pulse Width Modulation (PWM) is used. PWM is a way to generate analog signals from the digital code that we will be creating in the lab. This can be done by the PWM switching on and off, which represents the new signal as well as informs us on what the duty cycle (percentage of time the signal is on) is. All of these factors, components, and circuits will allow us to obtain a better understanding of microcontrollers as well as the individual components themselves.

 

 
## Design and Methods:

For this lab we needed:
* An oscilloscope: Tektronix TDS 2012
* 330 &Omega; resistor
* Computer running Arduino IDE: MacBook Air
* RedBoard, photoresistor, LED, two 10 k&Omega; potentiometers, momentary button, 10 k&Omega; resistor from SparkFun Inventor's kit

**Part One:** Blinking an LED

First, connect the Arduino RedBoard to the computer and run Arduino IDE on the computer. Then, import the blink program that is a sample program on Arduino IDE. This program is displayed below:

<p align="center">
  <img src="https://github.com/hrma240/Lab-5/blob/main/Screenshot%202024-02-15%20at%2010.59.02%20AM.png">
</p>

Next, build a circuit with the 330 &Omega; resistor and LED in series.

Run the program through the circuit to make the LED blink. The LED will turn on for one second then turn off for one second and repeat the cycle continuously with the code above. We then changed the delay in the code until the LED was blinking so fast that it looked as though it was constantly illuminated. We recorded this value and discuss it in our results section. 

**Part Two:** Controlling an LED with a potentiometer

Keep the Arduino RedBoard connected to the computer and open the Analog Read Serial Program that is a sample program on Arduino IDE.

<p align="center">
  <img src="https://github.com/hrma240/Lab-5/blob/main/Screenshot%202024-02-15%20at%2011.01.42%20AM.png">
</p>

Build the following circuit with a 10 k&Omega; potentiometer in series with an LED to control the blinking rate of the LED with the changing resistance of the potentiometer. Connect the variable resistance pin of the potentiometer to A0 of the RedBoard. 

Then, turn on the serial monitor to make sure the program is running correctly. We then edited the code so that the LED blinking time rate is the value read from the potentiometer. We made the delay of the LED equal the sensorValue read in the potentiometer.

<p align="center">
  <img src="https://github.com/hrma240/Lab-5/blob/main/Screenshot%202024-02-15%20at%2011.02.46%20AM.png">
</p>

With this code, the blinking rate of the LED will change as we adjust the resistance in the potentiometer. 

**Part Three:** Controlling an LED with a photoresistor

Keep the RedBoard connected to the computer and build a circuit with a photoresistor in series with a 10 k&Omega; resistor and an LED. 

We used the same code that we used to control the blinking rate of the LED with the potentiometer to instead control the blinking rate of the LED with the sensor value read from the photoresistor. From this, we found what the minimum and maximum analog values are for this circuit. 

We then created code that would turn on the LED only when the lighting was dark. For this code, we used the value that the serial monitor read when it was very bright, and made an if/else statement that would keep the LED off if the sensor value was above this value (900), and would turn the LED on if the sensor value went below 900. We put this in a loop so that the program would run continuously and we would have a circuit that acted as a nightlight.

<p align="center">
  <img src="https://github.com/hrma240/Lab-5/blob/main/Screenshot%202024-02-15%20at%2011.04.50%20AM.png">
</p>

We then replaced the 10 k&Omega; resistor in this circuit with another LED and observed what happened as the light levels changed. 

**Part Four:** LED dimmer using PWM 

Keep the RedBoard connected to the computer with Arduino IDE running. We then built the same circuit that we used in part two of this lab with the 10 k&Omega; potentiometer in series with the LED. However, we changed the LED pin to one that is PWM capable to be able to look at the signal through the LED on an oscilloscope. 

We then edited the blink sample program again so that 

<p align="center">
  <img src="https://github.com/hrma240/Lab-5/blob/main/Screenshot%202024-02-15%20at%2011.05.53%20AM.png">
</p>


## Results:

**Part One:** 

What does this first program do? 


The blink program turns on the LED and leaves it on for a set time period and then turns it off for a set time period. This cycle is repeated in the loop.

What are the major sections of the computer program and what does each section do? 


The first section is the void setup with the initialization of the digital pin of the LED and the second section is the void loop which puts whatever code is in that section in a loop. In this program, the code in that section is turning the pin on and off. 

What is the value of your delay when the light appears to stay consistently illuminated? 


The value of delay when the light appears to stay consistently illuminated was a delay of 10 which is equal to 0.01 seconds.

What field may this "persistence of vision" play a greater role in?

**Part Two:** 

What is the difference between an analog and digital signal? 


Analog signals are continuous and can take on infinite values while digital signals can only take on a certain number of values, such as on and off. Digital signals are discrete. 

List a few examples of real-world examples that can be described by an analog signal?

What are the two states which can be conveyed by a digital signal? 

What happens to the Serial Monitor Refresh rate as you move the potentiometer to control the LED blinking time?

**Part Three:** 

Does the LED turn on immediately after blocking the light? What about when you remove the object blocking the light, does the LED turn off immediately? 


We noticed that the LED turns on immediately after blocking the light from the photoresistor, it begins blinking rapidly right away. When the object is removed from the photoresistor, the LED blinking begins to slow down, but it takes a longer blink before returning to its steady blinking rate again. 


What happens when you place your finger over the photoresist? 


When we blocked the photoresistor with our finger, the LED blinked rapidly, but not as quickly as when we covered it with a more opaque object. The light from the room was able to still pass through our finger and hit the photoresist. 


When we changed the resistor with another LED and covered the photoresistor to block the light, the LEDs blinked one at a time. They blinked faster when the photoresistor was covered and they blinked slower when the photoresistor was uncovered. 

How does this help you visualize Ohm's Law? 


This helps us visualize Ohms Law, because as resistance in the photoresistor changes, current across the LED changes inversely while the voltage in the circuit stays the same since the supply voltage from the computer remains constant. 

What were the minimum and maximum analog values for this circuit? 


The maximum analog value we found for this circuit was 946. 

**Part Four:** 
Connect the oscilloscope to the LED pin and observe and record what happens to the signal and the LED brightness when you turn the knob of the potentiometer.

<p align="center">
  <img src="https://github.com/hrma240/Lab-5/blob/main/IMG_7807%20(1).jpg">
</p>
<p align="center">
  <img src="https://github.com/hrma240/Lab-5/blob/main/IMG_7809.jpg">
</p>
<p align="center">
  <img src="https://github.com/hrma240/Lab-5/blob/main/IMG_7813.jpg">
</p>


## Conclusions:
By the end of this lab, a better understanding of microcontrollers was obtained and learned. On top of this, the deeper observation and learning about LEDs and PWM's were obtained throughout the lab by constructing a series of differing circuits. By using the Arduino system we allowed ourselves to learn how to code and program different types of microcontrollers as well as learn how to write and create different codes. This allowed us to see how precise the Arduino IDE system is and how we must be descriptive and exact when it comes to coding the microcontrollers and other components as a whole. For example, the blink program turns on the LED and leaves it on for a set time period and then turns it off. Another learning example would be when using the photoresistor we noticed that the LED turns on immediately after blocking the light from the photoresistor, it begins blinking rapidly right away then, when the object was removed from the photoresistor, the LED blinking begins to slow down, allowing us to obtain the deeper knowledge on how to use these components. 
