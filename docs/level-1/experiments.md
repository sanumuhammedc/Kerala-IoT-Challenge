---
layout: default
title: Experiments
parent: Level 1
description: "experiments done as a part of kerala iot challenge"
permalink: level1/experiments
nav_order: 1
---


# **Experiments**

This section contains the experiments done as part of kerala iot challenge level 1
{: .fs-6 .fw-300 }

## **Experiment 1 : Hello World Led Blinking**

### Components Required

- Arduino Uno Board
- USB Cable
- LED (Any Color) x 1 Nos
- 220 OHM Resistor X 1 Nos
- Breadboard
- Jumper Wires (Male to Male ) X 2 Nos

### Circuit diagram

![circuit diagram](../../images/exp1.png "Circuit Diagram")

### Code

```
int ledPin = 10; // define digital pin 10.
void setup()
{
pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
}
void loop()
{
digitalWrite(ledPin, HIGH); // set the LED on.
delay(1000); // wait for a second.
digitalWrite(ledPin, LOW); // set the LED off.
delay(1000); // wait for a second
}
```



