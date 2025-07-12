# elec_task1

This project demonstrates a simple method to control multiple LEDs using push buttons and an Arduino UNO. It was developed as part of a learning exercise during the internship training with smart methods. 

The system includes three push buttons and three corresponding LEDs. The logic ensures that **only one LED can be turned on at any time**, and each button press toggles the state of its associated LED.

---

- LEDs are OFF by default at system startup.
- Pressing a button toggles its corresponding LED:
  - If the LED is OFF, it turns ON.
  - If the LED is already ON, it turns OFF.
- Pressing one button turns OFF any other LED that may be ON — ensuring exclusive LED activation.

---

- 1 x Arduino UNO board  
- 3 x Push buttons  
- 3 x LEDs (any color)  
- 3 x 220Ω resistors (for LEDs)
- 3 x 10KΩ resistors (for pushbuttons)  
- Breadboard and jumper wires  

---

| Button         | Arduino Pin | LED           | Arduino Pin |
|----------------|-------------|---------------|-------------|
| Button 1       | D7          | LED 1         | D13         |
| Button 2       | D4          | LED 2         | D12         |
| Button 3       | D2          | LED 3         | D11         |

---
 The code uses edge detection (from HIGH to LOW) to identify a fresh button press. When a button is pressed, its associated LED toggles, while any other LED is turned OFF. A short delay is included to minimize false triggers.
