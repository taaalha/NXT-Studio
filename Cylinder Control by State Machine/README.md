# Goal
The goal of this program was to implement state machine control of a double acting cylinder. There were 3 tasks 

# Task 1
Upon pressing the start button for the first time after deployment, the cylinder should move to the retracted position from the initial position and stop.

# Task 2
In this task manual control of the cylinder was developed. 

## Specifications

- Once the start button is pressed the cylinder should move from its base position to extended and stop.
- Once the cylinder stops, upon pressing the start button, the cylinder should go back to its base position and stop.
- If the “EMERGENCY STOP” button is pressed during the operation, the cylinder should immediately return to base position and stop.

## HMI Interaction Implementations
- Whenever the cylinder is in motion, the LED on the start button should be TURNED OFF. Once the cylinder stops at either position the LED should be TURNED ON. The LED being turned off would mean that the cylinder is in motion and the button can’t be pressed.
- When the “EMERGENCY STOP” button is pressed, the LED on the emergency button should TURN ON, and stay on until the cylinder reaches the base position and stops.


# Task 3
In this task, an automatic mode of operation was developed. Whereupon starting the automatic mode of operation, the cylinder should complete 2 full cycles and then stop at the base position.

## Specifications

- “Automatic Control” button on the HMI has to be used to switch to the automatic mode. Upon pressing the “automatic control” the implementation should go to automatic mode but the process should not start.
- To start the cycles, use the “Start” button i.e. once the system is in automatic mode and the start button is pressed, it should start with the operation and perform the desired number of cycles.
- If the automatic mode is enabled but the operation has not started and the “AUTOMATIC CONTROL” button is pressed again, the system should go back to the manual mode.
- If the “EMERGENCY STOP” button is pressed during the operation, the cylinder should immediately return to base position and stop.

## HMI Interaction Implementations

- Upon selection of the automatic control mode i.e. by pressing the automatic control button, the LED on the “AUTO” button should be TURNED ON and it should remain TURNED ON until the required number of cycles are not completed. It should only TURN OFF when the cylinder stops. This being highlighted would indicate the system is in automatic mode.
- Once the automatic mode is started by pressing the “START” button, the LED on the “START” button should be TURNED OFF. Once the cylinder completes the required number of cycles and stops, the LED should be TURNED ON. The LED being turned off would mean that the cylinder is in motion and the button can’t be pressed.
- When the “STOP” button is pressed, the LED on the emergency button should TURN ON, and stay on until the cylinder reaches the base position and stops.








# Some screenshots
![image](https://user-images.githubusercontent.com/87899535/135574667-127b351e-86a6-481f-8c22-f21f8023f723.png)
![image](https://user-images.githubusercontent.com/87899535/135574817-4b11f9ac-fd87-4ec6-8e45-6659e72082db.png)

**Note**: This exercise was part of the course ELEC-C8201 "Control and Automation" at Aalto University Finland. 



