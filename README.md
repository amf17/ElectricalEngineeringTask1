# Turning on the eye as a single light.

As you can see, the electrical circuit in the image below contains several components 

Arduino Uno R3

220 Ω Resistor

10 kΩ Resistor

Red LED

Pushbutton

![picture](Circuit.jpeg)

## Code
```
void setup()
{
  pinMode(2, INPUT);
  pinMode(13, OUTPUT);
}

void loop()
{
  if (digitalRead(2) == HIGH) {
    digitalWrite(13, HIGH);
  } else {
    digitalWrite(13, LOW);
  }
  delay(10); // Delay a little bit to improve simulation performance
}
```
The code you provided is an example of an Arduino sketch written in the Arduino programming language. It sets up the Arduino board to configure pin 2 as an input and pin 13 as an output in the `setup()` function.

In the `loop()` function, the code checks the state of pin 2 using the `digitalRead()` function. If pin 2 is in a HIGH state, it means that a voltage signal is detected, and the code sets pin 13 to a HIGH state using the `digitalWrite()` function. This turns on an LED or any other device connected to pin 13.

If pin 2 is in a LOW state, indicating no voltage signal, the code sets pin 13 to a LOW state, turning off the LED or device connected to it.

The `delay(10)` statement introduces a 10-millisecond delay between iterations of the loop to improve the performance of the simulation.

This code essentially reads the input state of pin 2 and mirrors it by setting the output state of pin 13 accordingly. If pin 2 is HIGH, pin 13 will be set HIGH, and if pin 2 is LOW, pin 13 will be set LOW.
