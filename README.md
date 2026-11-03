# Automatic Sensor-Based LED Control System Using STM32

## Aim

To interface a digital sensor with an STM32 microcontroller and automatically control an LED according to the sensor output.

## Apparatus Required

| S. No. | Component | Quantity |
|---:|---|---:|
| 1 | STM32 development board | 1 |
| 2 | Digital sensor or push button | 1 |
| 3 | LED | 1 |
| 4 | 220–330 Ω resistor | 1 |
| 5 | Breadboard | 1 |
| 6 | Jumper wires | As required |
| 7 | USB cable | 1 |

## Algorithm



## Program
ORG 0000H

START:
    MOV P2,#00H      ; LED ON (active LOW)
    ACALL DELAY
    MOV P2,#0FFH     ; LED OFF
    ACALL DELAY
    SJMP START

DELAY:
    MOV R7,#255
L1: MOV R6,#255
L2: DJNZ R6,L2
    DJNZ R7,L1
    RET

END
## Circuit Diagram
<img width="762" height="637" alt="image" src="https://github.com/user-attachments/assets/c06ca9fd-ce87-4781-8fc9-9c5f827d8720" />


## Result

The digital sensor was successfully interfaced with the STM32 microcontroller. The LED connected to `PA5` turned ON when the sensor input at `PA0` was HIGH and turned OFF when the sensor input was LOW.
