# WRO Future Engineers 2026 – Team "Infinity"

## Overview

This repository contains the design documentation, software structure, development notes, and supporting materials for our autonomous robot developed for the **WRO Future Engineers 2026** category.

Our robot is designed as a compact **car-like autonomous vehicle** based on **LEGO Education SPIKE Prime**. The project focuses on creating a robot that demonstrates the essential characteristics of a self-driving car:
- stable motion,
- dedicated steering,
- sensor-based decision making,
- and consistent autonomous behavior.

From the beginning of the project, our main engineering priority was **stability rather than maximum speed**. Instead of designing the robot to move as fast as possible, we focused on building a system that can move predictably, turn reliably, detect field colors at short range, and perform challenge-related tasks in a repeatable and explainable way.

This repository documents not only the final concept, but also the **engineering process** behind it:
- design choices,
- prototyping stages,
- testing and calibration,
- software logic,
- and iterative improvements.

---

## Team Information

**Team Name:** Infinity  
**Country / Region:** Kazakhstan
**School / Organization:** NIS Shymkent Abay

### Team Members
- Islam Yekiya
- Aslan Nysanaly
- Nurtas Nazarbaev

### Coach
- Makhambetova Maral

---

## Project Objective

The main objective of this project is to develop a rule-compliant autonomous vehicle for the **WRO Future Engineers** category using a realistic engineering approach.

The robot was designed to achieve the following goals:
- maintain stable forward motion,
- steer using a car-like front steering mechanism,
- detect important field colors from close range,
- determine route-related behavior autonomously,
- and complete challenge tasks in a reliable and reproducible way.

Our design philosophy is based on the idea that a successful autonomous robot must not only function, but also be:
- understandable,
- mechanically justified,
- logically structured,
- and well documented.

---

## Robot Concept

The robot follows a **four-wheel car-like design**. It is not a differential-drive platform. The system uses:
- **one motor for propulsion**,
- **one motor for steering**,
- and **one color sensor** for close-range color recognition.

This concept was selected because it is closer to the kinematics of a real autonomous car and better reflects the engineering spirit of the Future Engineers category.

The robot is based on **SPIKE Prime** as the main control platform. The design is intentionally compact, mechanically stable, and structured for iterative testing and improvement.

### Main Design Principles
1. **Car-like steering instead of differential drive**
2. **Stable movement instead of maximum speed**
3. **Short-range reliable sensing instead of uncertain long-range detection**
4. **Simple, modular software architecture**
5. **Engineering transparency and reproducibility**

---

## Mechanical Design Summary

The mechanical structure of the robot was built as a rigid four-wheel chassis with separate propulsion and steering functions.

### Chassis
The chassis was designed to be:
- compact,
- balanced,
- structurally rigid,
- and easy to modify during testing.

The central placement of the SPIKE Prime Hub was used to improve balance and reduce instability caused by uneven weight distribution.

### Drive System
The robot uses **one dedicated drive motor** connected to the drivetrain. The propulsion system was developed with emphasis on usable movement and stable floor behavior rather than maximum raw speed.

### Steering System
The robot uses a **separate steering motor** connected to the front wheel steering mechanism. Through repeated tests, the steering system was calibrated to identify:
- center,
- left,
- right,
- and softer correction values.

The introduction of soft steering values improved motion smoothness and reduced overcorrection.

### Design Philosophy
The mechanical design was not optimized for aggressive speed. Instead, it was optimized for:
- predictable path correction,
- stable straight driving,
- and consistent turning behavior.

---

## Electronics and Sensor Integration

The robot uses a simple but structured electronics concept centered around the **SPIKE Prime Hub**.

### Main Components
- **LEGO Education SPIKE Prime Hub**
- **1 propulsion motor**
- **1 steering motor**
- **1 SPIKE Prime color sensor**
- LEGO structural and wheel components

### Sensor Strategy
The main sensor in the current concept is the **SPIKE Prime color sensor**. It is used for **close-range color detection** rather than long-range visual sensing.

This choice was intentional. The sensor performs best when:
- the colored field element is close,
- the distance is controlled,
- and the sensor is mounted low and forward.

For this reason, the color sensor was installed in the **front lower part of the robot**, facing downward/forward so that it can identify field colors when the robot reaches the correct sensing range.

### Power and Integration Philosophy
The project prioritizes integrated and manageable system design. The electronics are kept as simple as possible to improve:
- reliability,
- ease of testing,
- and reproducibility.

---

## Software Architecture Summary

The software was developed using a **modular structure**, where each subsystem can be tested separately before full integration.

### Software Modules
The software concept includes the following logical blocks:
- configuration values,
- drive control,
- steering control,
- sensor reading,
- decision logic,
- challenge execution logic.

### Development Method
The robot software was developed incrementally:
1. movement test,
2. steering calibration,
3. sensor test,
4. decision logic,
5. integrated autonomous behavior.

This method reduced debugging complexity and made the engineering process more traceable.

### Control Philosophy
The software is designed around **stability-first control**. This means:
- no unnecessarily aggressive steering,
- no unstable reaction to single readings,
- no premature optimization for speed.

Instead, the robot is intended to:
- move steadily,
- interpret sensor input reliably,
- and apply repeatable actions.

---

## Open Challenge Strategy

For the Open Challenge, the robot is designed to use **field color recognition** to determine route direction.

### Direction Selection
The robot uses the color sensor to detect important field colors at the beginning of the run:
- if **blue** is detected first, the robot selects one driving direction,
- if **orange** is detected first, it selects the opposite direction.

### Driving Philosophy
After the direction is selected, the robot follows a stable movement strategy. The priority is:
- to remain consistent,
- to avoid unnecessary steering oscillation,
- and to complete the route in a controlled way.

At this stage of development, the team intentionally prioritizes **stable lap execution** over aggressive speed.

---

## Obstacle Challenge Strategy

For the Obstacle Challenge, the robot relies on close-range color detection to interpret field instructions.

### Rule Interpretation
The intended logic follows the competition meaning of colors:
- **red** corresponds to one side-selection behavior,
- **green** corresponds to the opposite side-selection behavior.

### Control Goal
The goal is to ensure that the robot:
- detects the relevant color reliably,
- applies a controlled directional response,
- and returns to stable forward motion.

---

## Engineering Development Process

The robot was not developed in a single step. It was created through a structured engineering process involving:
- concept selection,
- chassis construction,
- drivetrain testing,
- steering calibration,
- sensor placement experiments,
- software development,
- repeated testing,
- and iterative refinement.

### Main Development Stages
1. **Concept definition**
2. **Mechanical prototyping**
3. **Steering calibration**
4. **Sensor placement testing**
5. **Software integration**
6. **Stability refinement**

---

## Key Engineering Decisions

Several decisions strongly influenced the final concept of the robot.

### 1. Stability over speed
The team intentionally chose not to optimize the robot for maximum speed at the early stage. A slower but reliable robot is more valuable in autonomous competition than a fast but unstable one.

### 2. Car-like steering over differential drive
A steering-based design was selected to reflect realistic vehicle behavior and improve control quality.

### 3. Close-range sensing over long-range uncertainty
The SPIKE color sensor was used in the environment where it performs best: short-range detection. This made the sensing logic simpler and more reliable.

### 4. Modular software design
By separating movement, steering, sensing, and decisions into logical modules, the team made the project easier to test, debug, explain, and document.

### 5. Iterative improvement
The project was developed through repeated observation and correction rather than by assuming the first design would be final.

---

## Current Development Status

At the current stage, the robot already demonstrates the following:
- stable four-wheel chassis,
- one-motor propulsion concept,
- dedicated steering system,
- short-range color recognition,
- rule-oriented autonomous decision logic,
- and a structured engineering development process.

The robot is still under refinement, but the current prototype already reflects the main engineering principles required for Future Engineers:
- mobility,
- separate steering,
- sensing,
- software-controlled decisions,
- and reproducible development.

---

## Repository Structure

WRO-Future-Engineers/
├── README.md
├── LICENSE
├── .gitignore
├── src/
├── hardware/
├── mechanical/
├── docs/
├── journal/
└── media/
