# Lab 5: Microcontrollers
* Alexis Puckett
* Hannah Markwell
February 15, 2024

## Project Summary:

## Design and Methods:

For this lab we needed:
* An oscilloscope: Tektronix TDS 2012
* 330 &Omega; resistor
* Computer running Arduino IDE: MacBook Air
* RedBoard, photoresistor, LED, two 10 k&Omega; potentiometers, momentary button, 10 k&Omega; resistor from SparkFun Inventor's kit

**Part One:** Blinking an LED

First, connect the Arduino RedBoard to the computer and run Arduino IDE on the computer. Then, import the blink program that is a sample program on Arduino IDE. This program is displayed below:

Next, build a circuit with the 330 &Omega; resistor and LED in series.

Run the program through the circuit to make the LED blink. The LED will turn on for one second then turn off for one second and repeat the cycle continuously with the code above. We then changed the delay in the code until the LED was blinking so fast that it looked as though it was constantly illuminated. We recorded this value and discuss it in our results section. 

**Part Two:** Controlling an LED with a potentiometer

Keep the Arduino RedBoard connected to the computer and open the Analog Read Serial Program that is a sample program on Arduino IDE.

Build the following circuit with a 10 k&Omega; potentiometer in series with an LED to control the blinking rate of the LED with the changing resistance of the potentiometer. Connect the variable resistance pin of the potentiometer to A0 of the RedBoard. 

Then, turn on the serial monitor to make sure the program is running correctly. We then edited the code so that the LED blinking time rate is the value read from the potentiometer. We made the delay of the LED equal the sensorValue read in the potentiometer.

With this code, the blinking rate of the LED will change as we adjust the resistance in the potentiometer. 

**Part Three:** Controlling an LED with a photoresistor

Keep the RedBoard connected to the computer and build a circuit with a photoresistor in series with a 10 k&Omega; resistor and an LED. 

We used the same code that we used to control the blinking rate of the LED with the potentiometer to instead control the blinking rate of the LED with the sensor value read from the photoresistor. From this, we found what the minimum and maximum analog values are for this circuit. 

We then created code that would turn on the LED only when the lighting was dark. For this code, we used the value that the serial monitor read when it was very bright, and made an if/else statement that would keep the LED off if the sensor value was above this value (900), and would turn the LED on if the sensor value went below 900. We put this in a loop so that the program would run continuously and we would have a circuit that acted as a nightlight.

**Part Four:** LED dimmer using PWM 

Keep the RedBoard connected to the computer with Arduino IDE running. We then built the same circuit that we used in part two of this lab with the 10 k&Omega; potentiometer in series with the LED. However, we changed the LED pin to one that is PWM capable to be able to look at the signal through the LED on an oscilloscope. 

We then edited the blink sample program again so that 


## Results:

**Part One:** 
What does this first program do?

What are the major sections of the computer program and what does each section do?

What is the value of your delay when the light appears to stay consistently illuminated? What field may this "persistence of vision" play a greater role in?

**Part Two:** 
What is the difference between an analog and digital signal?

List a few examples of real-world examples that can be described by an analog signal?

What are the two states which can be conveyed by a digital signal?

What happens to the Serial Monitor Refresh rate as you move the potentiometer to control the LED blinking time?

**Part Three:** 
Does the LED turn on immediately after blocking the light? What about when you remove the object blocking the light, does the LED turn off immediately?

What happens when you place your finger over the photoresistor?

How does this help you visualize Ohm's Law?

What were the minimum and maximum analog values for this circuit?

**Part Four:** 
Connect the oscilloscope to the LED pin and observe and record what happens to the signal and the LED brightness when you turn the knob of the potentiometer.


## Conclusions:
