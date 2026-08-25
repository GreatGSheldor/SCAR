# SCAR — Project Journal

**Project:** SCAR
**Week:** 17–23 August 2026
**Total estimated time:** 17 hours

---

## 17 August — Starting the Project

**4:00 PM – 6:00 PM**
**2 hours**

Started working on SCAR as a robotics project.

The first part was getting the main idea together and deciding what the robot would contain. The project was split into three main code sections:

* `RoboCar.ino` — main robot
* `RoboArm.ino` — robotic arm
* `ESPCam.ino` — camera

The main robot was going to handle the car itself, while the arm and camera would be separate parts.

**Notes:**

I wanted the different parts to be testable separately instead of putting everything into one large Arduino program.

---

## 18 August — RoboCar

**4:00 PM – 7:00 PM**
**3 hours**

Worked on the main car code.

`RoboCar.ino` uses the Adafruit Motor Shield library and controls four DC motors. It also has two servos and two sensors.

The important sensor connections in the code are:

* MQ-2 → `A8`
* DHT11 → `A9`

The DHT11 is used for temperature and humidity readings, while the MQ-2 is read through its analog value.

The car also uses serial commands for control.

### Commands tested/implemented

```text
F  → Forward
B  → Backward
L  → Left
R  → Right
S  → Stop
```

There are also commands for the servos and sensor readings.

The main goal for the day was getting the different parts of the car control into one program rather than testing every component independently.

---

## 19 August — Sensors

**4:30 PM – 6:30 PM**
**2 hours**

Worked on the sensor part of `RoboCar.ino`.

The DHT11 is initialized on pin `A9` and is used to get:

* Temperature
* Humidity

The MQ-2 is connected to `A8`.

The serial interface was also set up so that sensor values could be requested while the robot is running.

### Serial commands

```text
T → Temperature
H → Humidity
G → MQ-2 reading
```

This made the sensor section separate from the movement commands.

The main thing checked here was that the sensor commands didn't interfere with the motor commands.

---

## 20 August — RoboArm

**4:00 PM – 7:00 PM**
**3 hours**

Worked on the robotic arm separately from the car.

`RoboArm.ino` uses four servos:

```text
Servo 1 → Pin 3
Servo 2 → Pin 5
Servo 3 → Pin 6
Servo 4 → Pin 9
```

The arm is controlled through serial input.

The program accepts commands in the form:

```text
s1 <angle>
s2 <angle>
s3 <angle>
s4 <angle>
```

For example, an input for servo 1 contains the servo number followed by the requested angle.

The servo angle is limited before being written to the servo, so values outside the allowed range aren't directly sent to the motor.

The arm was kept as its own Arduino program instead of combining it with the car program.

---

## 21 August — ESP Camera

**4:00 PM – 7:00 PM**
**3 hours**

Worked on the camera part.

`ESPCam.ino` is separate from the Arduino car and arm programs.

The ESP camera code:

* Connects the ESP to Wi-Fi
* Starts a web server
* Provides a camera stream
* Has a flash control
* Displays the camera feed through a browser

The stream uses MJPEG frames.

There is also a flash endpoint, so the flash can be switched on and off from the web interface.

### Basic flow

```text
ESP Camera
     ↓
Wi-Fi
     ↓
Web Server
     ↓
Browser
     ↓
Live Camera Feed
```

The camera was tested separately from the car and arm.

---

## 22 August — Putting the Project Together

**3:00 PM – 6:00 PM**
**3 hours**

At this point the individual parts were documented separately:

```text
RoboCar
├── Motors
├── Servos
├── DHT11
└── MQ-2

RoboArm
└── 4 Servos

ESPCam
├── Camera
├── Wi-Fi
├── Web Server
└── Flash
```

The next step was documenting how these parts fit into SCAR.

I also went through the available photos and videos and organized them with clearer names.

The final repository uses:

```text
SCAR1.jpg
SCAR2.jpg

SCAR Vid.mp4
ESP Cam Vid.mp4
Robo Arm Vid.mp4
```

The code files were also renamed to:

```text
RoboCar.ino
RoboArm.ino
ESPCam.ino
```

---

## 23 August — Final Testing & Documentation

**11:00 AM – 3:00 PM**
**4 hours**

Did a final pass through the three programs and the project media.

The main things checked were:

### RoboCar

* Four motor control
* Forward/backward/left/right/stop commands
* Servo commands
* DHT11 readings
* MQ-2 readings

### RoboArm

* Four servo connections
* Serial servo commands
* Servo angle handling

### ESPCam

* Camera initialization
* Wi-Fi connection
* Web server
* Camera stream
* Flash control

After checking the separate systems, I finished the project README and organized the repository.

The final repository contains the three Arduino programs, two project photos and three demonstration videos.

---

# Final Structure

```text
SCAR/
│
├── RoboCar.ino
├── RoboArm.ino
├── ESPCam.ino
│
├── SCAR1.jpg
├── SCAR2.jpg
│
├── SCAR Vid.mp4
├── ESP Cam Vid.mp4
├── Robo Arm Vid.mp4
│
└── README.md
```

---

# Time Summary

| Date      | Work                       |     Time |
| --------- | -------------------------- | -------: |
| 17 Aug    | Project setup              |      2 h |
| 18 Aug    | RoboCar                    |      3 h |
| 19 Aug    | Sensors                    |      2 h |
| 20 Aug    | RoboArm                    |      3 h |
| 21 Aug    | ESPCam                     |      3 h |
| 22 Aug    | Integration & organization |      3 h |
| 23 Aug    | Testing & documentation    |      4 h |
| **Total** |                            | **20 h** |

**Total estimated work: ~20 hours**

---

## Final Result

The project ended up as three separate systems:

**RoboCar** handles the vehicle, motors and sensors.

**RoboArm** handles the four servo motors of the arm.

**ESPCam** handles the camera, Wi-Fi connection, web server, video stream and flash.

Together they make up **SCAR**.
