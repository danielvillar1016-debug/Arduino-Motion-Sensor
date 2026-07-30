# Arduino-Motion-Sensor
This project involves the design and implementation of a motion-activated distance detection system using an ultrasonic sensor and a microcontroller. The system continuously measures the distance between the sensor and nearby objects and translates this data into real-time visual and auditory outputs.
Distance thresholds are represented using three LEDs: a green LED activates at approximately 12 inches, a yellow LED activates alongside the green LED at 7.96 inches, and a red LED activates when the object is closer than 3.96 inches. When the minimum distance threshold is crossed, an active buzzer emits repeated alerts until the object is removed from the detection range. This system demonstrates principles of sensor integration, conditional logic, and embedded system design.

Materials & Components:

 RexQualis Uno R3 (Arduino-compatible microcontroller)
 HC-SR04 Ultrasonic Distance Sensor
 3 LEDs (Red, Yellow, Green)
 3 × 1000 Ω resistors
 Active buzzer
 Breadboard
 10 Jumper wires (male–male)
10 Jumper Wires (male-female)
USB 5V power source


Objective:
The objective of this project was to design and implement a motion-activated distance detection system capable of measuring object proximity in real time and providing clear visual and auditory feedback based on predefined distance thresholds.


Methodology / System Operation:
The ultrasonic sensor emits high-frequency sound pulses and measures the time required for the echo to return after reflecting off an object. The microcontroller processes this time-of-flight data to calculate distance.

Based on the calculated distance, conditional logic activates LEDs to indicate proximity levels. When the minimum distance threshold is crossed, an active buzzer is triggered to provide an audible alert until the object moves out of range.

Circuit / Pin Configuration:
• Ultrasonic sensor trigger pin connected to digital pin 9
• Ultrasonic sensor echo pin connected to digital pin 10
• LEDs connected to digital pins 11, 12, and 13 with 1000 Ω resistors
• Active buzzer connected to digital pin 8
• Common ground shared across all components



Software Logic Overview:
The Arduino executes a continuous control loop that triggers the ultrasonic sensor, measures echo return time, and computes object distance in real time. This distance value is evaluated using conditional logic against predefined proximity thresholds to determine system behavior. Based on the comparison results, the microcontroller activates the appropriate LED indicators to represent increasing proximity and triggers an audible alert when the minimum threshold is crossed. System outputs update continuously to reflect changes in object position, and distance values are printed to the Serial Monitor for real-time validation and debugging.

Testing & Results:
The system was tested by placing objects of varying widths and heights at measured distances in front of the ultrasonic sensor while observing LED and buzzer responsiveness. The system reliably detected and responded to objects within the defined operating range. Objects positioned extremely close to the sensor (less than approximately 3 cm) were not consistently detected due to the physical limitations and minimum sensing distance of the ultrasonic sensor, resulting in reduced responsiveness at very close proximity.

Challenges & Iterations:
During development and testing, several challenges were encountered. Ultrasonic readings became inconsistent when objects were positioned extremely close to the sensor (below approximately 3 cm), which is consistent with the HC-SR04’s minimum sensing distance. Minor fluctuations also occurred due to object angle and surface reflectivity. These issues were addressed by defining proportional distance thresholds and validating readings using the Serial Monitor. Overall system reliability improved through iterative testing and threshold tuning.

 

