The purpose of this project is to construct and demonstrate the operation of a greenhouse automation system using a microcontroller. The automation system reads the ambient light and temperature and controls the greenhouse's ventilation fan and shading mechanism accordingly. The system performs the following functions:

(a) In the idle state (when the automation is powered on), a scrolling message "Press the button to start" is displayed on the screen. LEDs LED1 and LED2 are off. The DC motor does not rotate, and the servo motor's axis is at 180 degrees (shading fully open).

(b) When button SW1 is pressed for the first time, the greenhouse automation is activated. The display shows the message "Greenhouse Automation ON" for 3 seconds, and then the automation reads the ambient light level Ev and temperature T and displays them on the screen in Lux and °C with one decimal point accuracy.

(c) When the light level Ev is greater than half of Ev max, the shading mechanism of the greenhouse is fully closed [M2 Servo -> 0°]. When the light level Ev is less than half of Ev max, the shading mechanism operates in proportion to the light intensity [0° - 180°], meaning strong light results in full shading [0°], while weak light results in no shading [180°]. During the operation of the shading mechanism, LED2 lights up, and when the mechanism stops, LED2 turns off.

The light level Ev is determined by the equation: log(Ev) = -1.5 * log(RLDR) + 7.2.

(d) When the temperature T is higher than half of Tmax, the greenhouse's ventilation fan is activated and rotates at a variable angular speed [0% - 100%] proportional to the temperature (high temperature results in high speed). When the temperature T is lower than half of Tmax, the fan is deactivated. During the fan's operation, LED1 lights up, and when the fan stops, LED1 turns off.

(e) When button SW1 is pressed for the second time, the greenhouse automation is deactivated. The display shows the message "Greenhouse Automation OFF" for 3 seconds, and the automation returns to the idle state (a). All of the above functions are controlled by a microcontroller using multitasking software.

This project aims to automate the greenhouse environment by monitoring light and temperature and adjusting the shading and ventilation systems to maintain the optimal conditions for plant growth.
