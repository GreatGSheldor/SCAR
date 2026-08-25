# August 17: Planning SCAR

I started by planning what I wanted SCAR to have. I wanted the project to have more than just the basic car, so I split it into a few separate parts instead of trying to make everything one program.

The main parts were the car itself, the sensors, the robotic arm and the ESP camera.

I decided to keep the car, arm and camera as separate programs so I could work on and test them independently.

<img width="1540" height="881" alt="image" src="https://github.com/user-attachments/assets/8d49f01b-7555-4fde-8ca1-bfdd4b5b74f4" />

**Total time spent: 2 hours**

# August 18: Circuit and Code

I worked on the main electronics and the code for the car.

The main car uses four DC motors through the AFMotor library. I also added two servos, a DHT11 and an MQ-2 to the car program.

The DHT11 is connected to A9 and the MQ-2 to A8. The car is controlled through serial commands for movement, servo control and sensor readings.

I also worked on the separate robotic arm code. The arm uses four servos on pins 3, 5, 6 and 9 and is controlled through serial commands such as `s1 90`.

<img width="1893" height="1016" alt="image" src="https://github.com/user-attachments/assets/496b39ac-13f3-4d1a-a15a-4087996c2433" />

<img width="3840" height="2160" alt="IMG_20260825_100836_910" src="https://github.com/user-attachments/assets/4f0cdc7c-71da-4e87-b992-46b56c2940dd" />

**Total time spent: 5 hours**

# August 20: ESP Camera

I worked on the camera part separately from the Arduino programs.

The ESP camera connects to Wi-Fi and starts a web server. The server provides the camera stream and also has a flash control.

I tested the camera separately and checked that the stream could be opened through the web interface.

<img width="1893" height="1016" alt="image" src="https://github.com/user-attachments/assets/3afbdf54-fa3d-43ef-a492-3f8a15947e00" />

**Total time spent: 3 hours**

# August 23: Building and Testing SCAR

After working on the separate parts, I put the project together and tested the actual hardware.

I checked the car movement, the sensors, the robotic arm and the camera separately and then went through the available demonstrations.

The final repository also contains the SCAR photos and separate videos for the car, ESP camera and robotic arm.

<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/a42c82af-8f31-49b6-921a-d762b609a642" />

**Total time spent: 4 hours**
