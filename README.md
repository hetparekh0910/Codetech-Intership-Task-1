## Name : Het Parekh
## Company : CODTECH IT SOLUTIONS
## ID : CT0806DH
## Domain : Embedded Systems
## Duration : December 2024 to January 2025
## Mentor : Muzammil Ahmed
---
### Arduino LED Blinking on Tinkercad
This project demonstrates how to use an Arduino to create a simple LED blinking circuit. The simulation is performed on *Tinkercad*, a user-friendly platform for designing and testing circuits online.

### Technology Used  
- *Arduino IDE* (optional for offline testing)  
- *Tinkercad* (for online simulation and circuit design)

---

### Components Required  
- Arduino Uno  
- LED  
- Resistor (220 ohms)  
- Breadboard  
- Connecting wires  

---

### Circuit Diagram  
The circuit consists of an Arduino Uno connected to an LED through a 220-ohm resistor. The positive terminal of the LED (anode) is connected to *Pin 13* on the Arduino, and the negative terminal (cathode) is connected to the ground (GND) through the resistor.
![image](https://github.com/user-attachments/assets/32b3edc9-5b1c-466a-a15e-564dd8b122f8)

---

### Features  
- *Arduino Uno* serves as the microcontroller to control the LED.  
- The LED alternates between ON and OFF states with a one-second delay, demonstrating basic control using digital pins.  

---

### Code  

int ledCount = 6; 
int ledPins[] = { 8, 9, 10, 11, 12, 13}; 
int ledDelay = 300;

void setup() { 
  for (int thisLed = 0; thisLed < ledCount; thisLed++) { 
    pinMode(ledPins[thisLed], OUTPUT); 
  } 
}

void loop() { 
  digitalWrite(ledPins[4], HIGH); 
  delay(ledDelay); 
  digitalWrite(ledPins[4], LOW); 
  for (int offset = 1; offset <= 4; offset++) { 
    digitalWrite(ledPins[4 - offset], HIGH); 
    digitalWrite(ledPins[4 + offset], HIGH); 
    delay(ledDelay); 
    digitalWrite(ledPins[4 - offset], LOW); 
    digitalWrite(ledPins[4 + offset], LOW); 
  } 
  delay(ledDelay);

  for (int offset = 4; offset >= 1; offset--) { 
    digitalWrite(ledPins[4 - offset], HIGH); 
    digitalWrite(ledPins[4 + offset], HIGH); 
    delay(ledDelay); 
    digitalWrite(ledPins[4 - offset], LOW); 
    digitalWrite(ledPins[4 + offset], LOW); 
  } 
  digitalWrite(ledPins[4], HIGH); 
  delay(ledDelay); 
  digitalWrite(ledPins[4], LOW); 
  delay(ledDelay);

  for (int thisLed = 0; thisLed < 5; thisLed++) { 
    digitalWrite(ledPins[thisLed], HIGH); 
    delay(ledDelay); 
    digitalWrite(ledPins[thisLed], LOW); 
  } 
  digitalWrite(ledPins[4], HIGH); 
  delay(ledDelay); 
  digitalWrite(ledPins[4], LOW); 
  delay(ledDelay); 
  digitalWrite(ledPins[4], HIGH); 
  delay(ledDelay); 
  digitalWrite(ledPins[4], LOW); 
  for (int thisLed = 5; thisLed < 9; thisLed++) { 
    digitalWrite(ledPins[thisLed], HIGH); 
    delay(ledDelay); 
    digitalWrite(ledPins[thisLed], LOW); 
  } 
  delay(ledDelay);

  for (int thisLed = 0; thisLed < ledCount; thisLed += 2) { 
    digitalWrite(ledPins[thisLed], HIGH); 
    delay(ledDelay); 
    digitalWrite(ledPins[thisLed], LOW); 
  } 
  delay(1000);

  for (int thisLed = 1; thisLed < ledCount; thisLed += 2) { 
    digitalWrite(ledPins[thisLed], HIGH); 
    delay(ledDelay); 
    digitalWrite(ledPins[thisLed], LOW); 
  } 
  delay(1000); 

}

### Simulation Video


https://github.com/user-attachments/assets/c65430cb-99ee-4e0a-8466-685002ce20b6

