# 8051 LED Blinking Project

A simple embedded systems project that demonstrates how to blink an LED using the 8051 microcontroller. This project is ideal for beginners learning microcontroller programming and interfacing.

## 📖 Overview

The program continuously turns an LED ON and OFF with a delay between each state change. It helps students understand:

- GPIO port operation
- Delay generation
- Assembly language programming
- Basic hardware interfacing

## 🛠 Components Required

- 8051 Microcontroller
- LED
- 220Ω Resistor
- Crystal Oscillator (11.0592 MHz)
- Capacitors
- Power Supply (5V)
- Breadboard and Connecting Wires

## 🔌 Circuit Connection

| Component | Connection |
|------------|------------|
| LED Anode | P1.0 |
| LED Cathode | Ground through 220Ω resistor |

## 💻 Program

```assembly
ORG 0000H

START:
SETB P1.0
ACALL DELAY

CLR P1.0
ACALL DELAY

SJMP START

DELAY:
MOV R7,#255
D1: MOV R6,#255
D2: DJNZ R6,D2
DJNZ R7,D1
RET

END
```

## ▶️ Working

1. LED connected to Port 1.0 is turned ON.
2. Delay routine creates a visible pause.
3. LED is turned OFF.
4. Another delay is generated.
5. The process repeats indefinitely.

## 📚 Learning Outcomes

- Understanding 8051 architecture
- Port programming
- Delay generation techniques
- Embedded system fundamentals

## 🚀 Future Improvements

- Multiple LED patterns
- Traffic light controller
- LED chaser circuit
- PWM brightness control

## 📄 License

This project is open-source and available under the MIT License.

## 👨‍💻 Author

Jobin Manuel

Electronics and Communication Engineering Student
