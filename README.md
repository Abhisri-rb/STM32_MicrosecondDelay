# STM32_MicrosecondDelay

## 📌 Description
This project demonstrates how to generate a square wave using microsecond delay on STM32.

A hardware timer (TIM2) is configured to provide precise microsecond timing, and a GPIO pin is toggled to produce a square wave that can be observed on an oscilloscope.

---

## 🎯 Objective
- Generate square wave using microsecond delay
- Understand timer-based delay
- Verify output using oscilloscope

---

## ⚙️ Hardware Used
- STM32F401CDU6 (or similar STM32 board)
- Oscilloscope
- Jumper wires

---

## 🧠 Working Principle
TIM2 is configured such that:

1 timer tick = 1 microsecond

The timer counts in microseconds, and the GPIO pin is toggled after a fixed delay, producing a square wave.

---

## ⏱️ Timer Configuration
- Timer: TIM2  
- Prescaler: 84 - 1  
- System Clock: 84 MHz  
- Timer Frequency: 1 MHz  
- Resolution: 1 µs  

---

## 💻 Code Implementation

### 🔹 Start Timer
```c
HAL_TIM_Base_Start(&htim2);
