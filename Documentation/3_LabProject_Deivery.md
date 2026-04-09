# **LAB SESSION 1: Bet Jufresa, Maria Rovira and Carla Dueñas**
## **1. Objective of the lab session**

The objective of this lab session was to measure and visualize the 3D orientation of an object in real time using an IMU sensor connected to an ESP32 microcontroller.

This system allows to obtain the Roll, Pitch and Yaw (RPY) orientation angles, which describe the rotation of an object with respect to a global reference system.

## **2. Theoretical Background**
The system is based on an IMU (Inertial Measurement Unit), which integrates:
- Accelerometer = measures linear acceleration
- Gyroscope = measures angular velocity
- Compass = provides a reference to the real-world orientation

From these measurements, the system computes the orientation using:
- Roll = rotation around the X-axis
- Pitch = rotation around the Y-axis
- Yaw = rotation around the Z-axis

These orientation values are transmitted via WiFi to a computer, where they are visualized in a virtual environment.

## **3. Lab Procedure**
The lab session started with the setup of the working environment. This included configuring the project using GitHub and Visual Studio Code, as well as programming the ESP32 microcontroller through the PlatformIO extension. The device was then connected to the laboratory WiFi network to enable communication between the hardware and the computer. As an initial step, a simple LED blinking program was executed on the ESP32 in order to verify that the board was correctly configured and functioning.

Once the setup was completed, the IMU system was integrated into the ESP32. The Endowrist_IMU program was uploaded to the board, allowing it to read the sensor data provided by the IMU. The ESP32 processed this information to compute the orientation of the device in terms of Roll, Pitch, and Yaw angles. These orientation values were then transmitted in real time via WiFi using a UDP communication protocol.

To visualize the orientation data, we used RoboDK. We opened a 3D environment where a virtual object could move according to the data received. A Python script was used to receive the Roll, Pitch, and Yaw values sent by the ESP32 and apply them to the virtual object. As a result, the object in the simulation moved in real time. When we moved the ESP32 with our hands, the virtual object moved in the same way, which showed that the system was working correctly and sending the data properly.

<img width="624" height="245" alt="Screenshot 2026-03-24 at 13 55 21" src="https://github.com/user-attachments/assets/53eea693-4102-4ef3-ba05-e84de67cc016" />

We also changed the object from a plane to a surgical needle and used sliders to simulate the orientation. This helped us understand how Roll, Pitch, and Yaw affect the movement.

<img width="623" height="325" alt="Screenshot 2026-03-24 at 13 55 56" src="https://github.com/user-attachments/assets/07db9da2-a0d8-4b71-849d-f45d47dd533c" />

<img width="626" height="320" alt="Screenshot 2026-03-24 at 13 56 07" src="https://github.com/user-attachments/assets/204bab7b-8ec0-43e3-bacc-346b19050cb7" />

## **4. Results**
- The orientation data was sent in real time
- The movement of the ESP32 matched the movement of the virtual object
- The Roll, Pitch, and Yaw system worked correctly

## **5. Conclusions**
This lab helped us understand how to connect hardware, like the ESP32 and the IMU sensor, with software. We also learned how to work with real-time data and how to show the 3D orientation of an object in a virtual environment. These tools are useful for many engineering applications, especially in robotics and biomedical engineering.




