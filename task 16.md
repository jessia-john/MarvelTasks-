# TASK 16: Datasheets report writing:

## What is L293 d
---
The L293D is a **quadruple high-current half-H drivers**. It is designed to provide bidirectional drive currents of up to 600-mA at voltages from 4.5 V to 36 V. It is designed to drive inductive loads such as relays, solenoids, DC and bipolar stepping motors, as well as other high-current/high-voltage loads in positive-supply applications.
![l293d](https://raw.github.com/jessia-john/Marvel/5d83c1a6551a98732a656569fee13b2593902dae/IMG_0117.jpeg)
### Charateristics
-   Wide Supply-Voltage Range: 4.5 V to 36 V
-   Separate Input-Logic Supply
-   Internal ESD Protection
-   High-Noise-Immunity Inputs
-   Output Current 1 A Per Channel (600 mA for L293D)
-   Peak Output Current 2 A Per Channel (1.2 A for L293D)
-   Output Clamp Diodes for Inductive Transient Suppression (L293D)

### Block diagram
![Block diagram](https://raw.github.com/jessia-john/Marvel/50c421e18a3868ac3e92b6c2f543bd6f170080e3/IMG_0103.png)

---
### Pin diagram 
---
![Pin diagram](https://raw.github.com/jessia-john/Marvel/cf86e884ab876a03c6b49f4a7c66aa51bbbf344d/IMG_0104.png)

| Pin | Name | Description |
| :--- | :--- | :--- |
| 1 | ENABLE 1-2 | Master control pin that enables the left side of the IC (Motor 1) when HIGH. |
| 2 | INPUT 1 | Logic input that controls the state/direction of Output 1. |
| 3 | OUTPUT 1 | Connected to one terminal of the first DC motor. |
| 4 | GND | Ground pin; also used as a heat sink for the IC. |
| 5 | GND | Ground pin; also used as a heat sink for the IC. |
| 6 | OUTPUT 2 | Conneted to the second terminal of the first DC motor. |
| 7 | INPUT 2 | Logic input that controls the state/direction of Output 2. |
| 8 | Vs (Vcc2) | Power supply pin for the motors (typically 4.5V to 36V). |
| 9 | ENABLE 3-4 | Master control pin that enables the right side of the IC (Motor 2) when HIGH. |
| 10 | INPUT 3 | Logic input that controls the state/direction of Output 3. |
| 11 | OUTPUT 3 | Connected to one terminal of the second DC motor. |
| 12 | GND | Ground pin; also sed as a eat sik for the IC. |
| 13 | GND | Ground pin; also used as a heat sink for the IC. |
| 14 | OUTPUT 4 | Connected to the second terminal of the second DC motor. |
| 15 | INPUT 4 | Logic input that controls the state/direction of Output 4. |
| 16 | Vss (Vcc1) | Internal logic power supply pin (typically 5V). |



### Working
Suppose we want to use a motor of rating 12V and 1A, if we connect it with an microcontroller , say Arduino, the Arduino will be able to supply only 5V but the motor does not rotate. Thus we require to amplify the input current in order to drive the motor.

#### Motor driver :
A **motor driver** is basically a current *amplifier* which takes a low-current signal from the microcontroller and gives out a proportionally higher current signal which can control and drive a motor.
<br>In most cases, a transistor can act as a switch and perform this task which drives the motor in a single direction.

**Changing direction of motor:**
**H-Bridge**
Turning a motor ON and OFF requires only one switch to control a single motor in a single direction. What if you want to reverse its direction? The simple answer is to reverse its polarity. We can use a H-Bridge for this.
The H-Bridge is typically an electrical circuit that enables a voltage to be applied across a load in either direction to an output. This means you can essentially reverse the direction of current and thus reverse the direction of the motor. 

| Enable 1 | Input 1 | Input 2 | Function |
| :--- | :--- | :--- | :--- |
| 1 | 1 | 0 | Rotates Anti-clockwise (Reverse) |
| 1 | 0 | 1 | Rotates Clockwise (Forward) |
| 1 | 1 | 1 | OFF (Braking) |
| 1 | 0 | 0 | OFF (Idle) |
| 0 | X | X | OFF (Disabled) |

![H-h bridge](https://raw.github.com/jessia-john/Marvel/5d83c1a6551a98732a656569fee13b2593902dae/IMG_0106.gif) 


A H-bridge is fabricated with four switches like S1, S2, S3 and S4. When the S1 and S4 switches are closed, then a +ve voltage will be applied across the motor. By opening the switches S1 and S4 and closing the switches S2 and S3, this voltage is inverted, allowing invert operation of the motor.

![Pwm](https://raw.github.com/jessia-john/Marvel/5d83c1a6551a98732a656569fee13b2593902dae/IMG_0105.png)
This L293D IC works on the basic principle of H-bridge, this motor control circuit allows the voltage to be flowing in any direction. As we know that the voltage must be change the direction of being able to rotate the DC motor in both the directions. Hence, H-bridge circuit using L293D ICs are perfect for driving a motor. Single L293D IC consists of two H-bridge circuits inside which can rotate two DC motors separately. Generally, these circuits are used in robotics due to its size for controlling DC motors.

The above is used to control the direction of a motor to control speed we make use of PWM. 

**Controlling speed of motor using Pulse Width Modulation (PWM)**
To control speed of motor using pwm (pulse width modulation ) the Enable pin (Pin 1 or Pin 9) is used.
To **regulate speed**, you apply a Pulse Width Modulation (**PWM**) signal to the driver’s **Enable pin**, rapidly switching the motor's power on and off to vary the average voltage it receives. For a functional setup, the L293D's logic pin (VCC1) must be powered by the microcontroller, while the motor supply pin (VCC2) connects to an external battery, ensuring all components share a **common ground** to complete the circuit safely.

- Pulse Width Modulation (PWM) changes a motor's speed by rapidly switching the power on and off to control the average voltage delivered to the motor terminals. A DC motor has physical inertia and internal inductance, so it does not stop and start instantly; instead, it smoothens these rapid pulses into a steady rotational speed.

- The main principle of pwm is duty cycle.
- 0% duty cycle - This indicates the signal and hence motor is OFF.
- 50% duty cycle- The signal is ON for half the time.
- 100% duty cycle: The signal is always ON. The motor runs at maximum speed.
- 

![pwm](https://raw.github.com/jessia-john/Marvel/5d83c1a6551a98732a656569fee13b2593902dae/IMG_0113.png)

### Applications

1.  **Microcontroller Interfacing**: Acts as a bridge between low-power controllers like Arduino/Raspberry Pi and high-power motors that require up to 36V.
2. **DC Motor Control**: Drives two DC motors independently, allowing for bidirectional rotation and speed control in small robots or RC cars.
3.  **Home Automation**: Powers small actuators for mechanical tasks like opening motorized curtains, blinds, or electronic door latches.

