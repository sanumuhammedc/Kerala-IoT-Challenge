---
layout: default
title: Projects
parent: Level 1
description: "projects done as a part of kerala iot challenge"
permalink: level1/projects
nav_order: 2
---


# **Projects**

This section contains the projects done after doing experiments of kerala iot challenge level 1
{: .fs-6 .fw-300 }


## Create an automatic night lamp model using LDR and LED

### Code


```
int potpin=7;
int ledpin=11;
void setup()
{
  pinMode(ledpin,OUTPUT);// set digital pin 11 as “output”
  pinMode(potpin,INPUT);// set pin 7 as input
}
void loop()
{
  if(digitalRead(potpin) == 1)
  {
    digitalWrite(ledpin,HIGH);
  }
  else
  {
    digitalWrite(ledpin,LOW);
  }
  Serial.println(digitalRead(potpin));
  delay(10);// wait for 0.01 
}
```
### Result

<a href="https://www.youtube.com/shorts/9nMSeni_bOg" target="__blank" >View video of Result</a>


## Create a Digital Dice using 6 LEDs and 1 Push Button

### Code


```
long led_pin;

void setup()
{
  pinMode(8,INPUT);  
  for(int i=2;i<8;i++)
  {
    pinMode(i,OUTPUT);   
  }
}
void loop()
{
  int val = digitalRead(8);
  if(val == LOW)
  {
    led_pin = random(2,8);
    digitalWrite(led_pin, LOW);
  }
  else
  {
    digitalWrite(led_pin, HIGH);
  }
}
```

### Result

<a href="https://www.youtube.com/shorts/9j5IdT0Oug8" target="__blank" >View video of Result</a>

## Create a Digital Dice using 7 Segment Display and Push Button

### Code


```
int a=7;
int b=6;
int c=5;
int d=10;
int e=11;
int f=8;
int g=9;
int dp=4;
long choice;
void digital_1(void) // display number 1
{
	unsigned char j;
  digitalWrite(c,HIGH);// set level as “high” for pin 5, turn on segment c
  digitalWrite(b,HIGH);// turn on segment b
  for(j=7;j<=11;j++)// turn off other segments
  digitalWrite(j,LOW);
  digitalWrite(dp,LOW);// turn off segment dp
}
void digital_2(void) // display number 2
{
unsigned char j;
  digitalWrite(b,HIGH);
  digitalWrite(a,HIGH);
  for(j=9;j<=11;j++)
  	digitalWrite(j,HIGH);
  digitalWrite(dp,LOW);
  digitalWrite(c,LOW);
  digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{
  digitalWrite(g,HIGH);
  digitalWrite(a,HIGH);
  digitalWrite(b,HIGH);
  digitalWrite(c,HIGH);
  digitalWrite(d,HIGH);
  digitalWrite(dp,LOW);
  digitalWrite(f,LOW);
  digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{
  digitalWrite(c,HIGH);
  digitalWrite(b,HIGH);
  digitalWrite(f,HIGH);
  digitalWrite(g,HIGH);
  digitalWrite(dp,LOW);
  digitalWrite(a,LOW);
  digitalWrite(e,LOW);
  digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
  unsigned char j;
  digitalWrite(a,HIGH);
  digitalWrite(b, LOW);
  digitalWrite(c,HIGH);
  digitalWrite(d,HIGH);
  digitalWrite(e, LOW);
  digitalWrite(f,HIGH);
  digitalWrite(g,HIGH);
  digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
  unsigned char j;
  for(j=7;j<=11;j++)
  digitalWrite(j,HIGH);
  digitalWrite(c,HIGH);
  digitalWrite(dp,LOW);
  digitalWrite(b,LOW);
}
void setup()
{
  int i;// set variable
  for(i=4;i<=11;i++)
  pinMode(i,OUTPUT);// set pin 4-11as “output”
  pinMode(13,INPUT);
}
void loop()
{
  int val = digitalRead(13);
  if(val == HIGH)
    choice = random(1,7);
  switch(choice)
  {
    case 1:
    digital_1();
    break;
    case 2:
    digital_2();
    break;
    case 3:
    digital_3();
    break;
    case 4:
    digital_4();
    break;
    case 5:
    digital_5();
    break;
    case 6:
    digital_6();
    break;
  }
} 
```

### Result

<a href="https://www.youtube.com/shorts/Hbkg5ccz6JY" target="__blank" >View video of Result</a>
