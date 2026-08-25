# SCAR 🤖

### Surveillance • Control • Automation Robot

SCAR is an Arduino-based robotics project combining **mobility, environmental sensing, live video, and robotic manipulation** into a single mobile platform.

Built as an exploration of robotics and embedded systems, SCAR was designed to be more than a simple remote-controlled car — it combines multiple hardware and software systems to create a versatile robotic platform.

> ⚠️ **Status:** Archived / no longer actively developed.

---

## ⚡ Features

* 🚗 **Mobile Platform** — Motor-driven movement
* 🦾 **Robotic Arm** — Servo-controlled object manipulation
* 📷 **Live Vision** — ESP-based camera system
* 🌡️ **Environmental Sensing** — Collects sensor data while moving
* 🎮 **Remote Control** — Command-based robot control
* 🔋 **Portable Power** — Battery-powered platform
* ☀️ **Solar Support** — Experimental solar-powered operation

---

## 🧠 Architecture

```text
                         ┌─────────────────┐
                         │      SCAR       │
                         │   Main Control  │
                         └────────┬────────┘
                                  │
              ┌───────────────────┼───────────────────┐
              │                   │                   │
              ▼                   ▼                   ▼
        ┌───────────┐       ┌───────────┐       ┌───────────┐
        │  MOVEMENT │       │  SENSORS  │       │ ROBOT ARM │
        └───────────┘       └───────────┘       └───────────┘
              │                   │                   │
              ▼                   ▼                   ▼
           Driving          Environment          Manipulation

                         ┌─────────────────┐
                         │    ESP CAMERA   │
                         └─────────────────┘
                                  │
                                  ▼
                            Live Video
```

---

## 🛠️ Hardware

| Component    | Purpose                    |
| ------------ | -------------------------- |
| Arduino      | Main controller            |
| DC Motors    | Robot movement             |
| Motor Driver | Motor control              |
| Servos       | Robotic arm                |
| Sensors      | Environmental monitoring   |
| ESP Camera   | Live video                 |
| Battery      | Portable power             |
| Solar Panel  | Experimental power support |

---

## 🔩 Bill of Materials

| Component | Qty | Price (INR) | Approx. USD |
|---|---:|---:|---:|
| Arduino UNO R4 WiFi | 1 | ₹1,500 | $17.05 |
| ESP32-CAM | 1 | ₹582 | $6.61 |
| Main chassis | 1 | ₹500 | $5.68 |
| Robotic arm chassis | 1 | ₹1,200 | $13.64 |
| DC geared motors | 4 | ₹90 each | $4.09 |
| Arduino Motor Shield | 1 | ~₹500 | $5.68 |
| Arm servo motors | 4 | ₹150 each | $6.82 |
| SG90 camera servos | 2 | ~₹100 each | $2.27 |
| DHT11 | 1 | ₹90 | $1.02 |
| MQ-2 gas sensor | 1 | ~₹90 | $1.02 |
| HC-SR04 | 1 | ~₹69 | $0.78 |
| Solar panel | 1 | ₹200 | $2.27 |
| **Total** | | **~₹7,081** | **~$80.47** |

---

## 📂 Project Structure

```text
SCAR/
│
├── RoboCar.ino    # Main robot control
├── RoboArm.ino        # Robotic arm control
├── ESPCam.ino         # ESP camera system
│
├── SCAR1.jpg         # Project photos
├── SCAR2.jpg
│
├── SCAR Vid.mp4       # Robot demonstration
├── ESP Cam Vid.mp4    # Camera demonstration
├── Robo Arm Vid.mp4   # Arm demonstration
│
└── README.md
```

---

## 🚗 Movement

The main controller handles SCAR's movement through its motor system.

The robot can be commanded to move and navigate using the control interface implemented in the Arduino firmware.

---

## 🦾 Robotic Arm

SCAR features a multi-servo robotic arm designed to interact with objects.

The arm adds a manipulation capability to the mobile platform, allowing SCAR to do more than simply move around.

---

## 📷 Vision

An ESP-based camera provides SCAR with a live visual feed.

The camera can be mounted on the robot to provide a first-person view while SCAR is being operated.

**Mobility + Vision + Manipulation** is what makes SCAR different from a conventional robot car.

---

## 🌡️ Sensing

SCAR incorporates environmental sensors so that it can gather information while operating.

The sensing system was designed as an experimental platform for combining environmental data with mobile robotics.

---

## 🔋 Power

SCAR uses a portable battery-powered architecture, with solar power explored as an additional way of extending operation.

Power management was an important part of the design because multiple subsystems — motors, servos, sensors, and the camera — operate simultaneously.

---

## 🎯 Goals

SCAR was built to explore:

* Robotics
* Embedded programming
* Motor control
* Servo control
* Sensor integration
* Computer vision
* Hardware-software integration
* Remote robotics
* Power management

The project focused as much on **learning and experimentation** as the final robot itself.

---

## 🧪 What I Learned

Building SCAR meant working across both software and hardware:

```text
Arduino
   ↓
Motor Control
   ↓
Sensors
   ↓
Servo Systems
   ↓
ESP Camera
   ↓
Power Management
   ↓
One Integrated Robot
```

The hardest part wasn't building each subsystem individually — it was making them work together as one system.

---

## 📸 Media

Project photos and demonstration videos are included in the repository.

### SCAR

<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/5f38e3d7-c4ba-4746-b4b3-cbf0790ea804" />
<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/3a0f15d1-45ad-4562-85fb-d9d1335124cc" />


---

## 👨‍💻 Author

**Akshat Jain**

> **SCAR — bringing movement, vision, sensing, and manipulation together in one robot.**
