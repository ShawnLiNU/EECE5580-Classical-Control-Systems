# EECE 5580 — Classical Control Systems

**Northeastern University · Seattle Campus**  
**Department of Electrical and Computer Engineering**  
Instructor: [Dr. Xian Li](https://shawnlinu.github.io) | x.li1@northeastern.edu

---

## Course Description

The mathematics of feedback — the idea that a system can measure its own output and use that measurement to correct its behavior — is one of the most consequential ideas in all of engineering. It is what keeps aircraft stable in turbulence, what holds industrial robots on precise trajectories, what regulates insulin pumps, and what will one day allow fully autonomous vehicles to navigate safely at highway speeds. The field is over a century old, but its core principles remain indispensable to every practicing engineer who builds systems that move, heat, pressurize, or position anything.

In this course, you will learn classical control theory the way it was meant to be learned: by applying it to a physical system you build yourself. Working in pairs, you will construct a self-balancing two-wheeled robot from scratch, derive its mathematical model using Lagrangian mechanics, design a controller on paper using root locus and frequency-domain methods, and implement that controller in firmware running at 100 Hz on a microcontroller. The semester ends with a race. The robot that travels five meters the fastest — while staying balanced — wins.

Every concept in the syllabus connects directly to that robot. When you analyze Bode plots in Week 6, it is because your robot's stability margin is what you are computing. When you study integral windup in Week 4, it is because you are about to experience it firsthand.

---

## Course Objectives

By the end of EECE 5580, you will be able to:

- **Model** a physical system as a transfer function or state-space representation, and identify its parameters from experimental step-response data
- **Analyze** time-domain performance (rise time, settling time, overshoot) and connect those specifications to pole locations in the complex plane
- **Design** PID, proportional, and lead/lag compensators using root locus and frequency-domain methods that meet quantitative performance specifications
- **Implement** a digital control loop on embedded hardware and tune it on a real, unstable plant
- **Evaluate** closed-loop stability using the Routh-Hurwitz criterion, root locus, Bode plots, and gain/phase margins
- **Integrate** system identification, controller design, and embedded implementation into a complete engineering project — from mathematical model to working hardware

---

## Resources

### Recommended Textbooks

The course does not require purchasing a textbook. All required material is on the [course wiki](https://github.com/shawnlinu/EECE5580-Classical-Control-Systems/wiki). The following books are excellent references and are available through the Northeastern University library:

- Ogata, K. *Modern Control Engineering* (5th ed.). Pearson, 2010.
- Franklin, G., Powell, J. D., & Emami-Naeini, A. *Feedback Control of Dynamic Systems* (8th ed.). Pearson, 2018.
- Nise, N. *Control Systems Engineering* (7th ed.). Wiley, 2015.
- Åström, K. J., & Hägglund, T. *PID Controllers: Theory, Design, and Tuning* (2nd ed.). ISA, 1995.

### Software

| Tool | Purpose |
|------|---------|
| Python 3.10+ (`python-control`, `scipy`, `numpy`, `matplotlib`) | System modeling, simulation, and Bode/root locus analysis |
| Jupyter Lab | Interactive computation and lab report generation |
| Arduino IDE 2.x | Firmware development for the balancing robot |
| ROS2 Humble | PincherX 100 arm control and data logging |
| Dynamixel Wizard 2.0 | Servo PID register configuration |

See [Prereq 1: Software Setup](https://github.com/shawnlinu/EECE5580-Classical-Control-Systems/wiki/Prereq-1-Software-Setup) for installation instructions.

### Hardware

| Hardware | Role |
|----------|------|
| [PincherX 100 Robot Arm](https://www.trossenrobotics.com/pincherx-100-robot-arm.aspx) (Interbotix / Trossen Robotics) | First platform for system identification, PID, root locus, and Bode labs |
| Student-built two-wheeled balancing robot | Capstone platform — teams build, model, and race their own robot |

The balancing robot uses off-the-shelf components (Arduino Nano, MPU-6050 IMU, L298N motor driver, DC gearmotors with encoders) and a 3D-printed chassis. Total parts cost per team is approximately $60–75. Components are provided by the course.

---

## Repository Structure

```
EECE5580-Classical-Control-Systems/
│
├── code/
│   ├── labs/           # Python scripts for PincherX 100 labs (starter files)
│   ├── arduino/        # Arduino firmware for the balancing robot
│   └── simulation/     # Jupyter notebooks for in-class demonstrations
│
├── hardware/
│   └── chassis/        # STL files for 3D-printed balancing robot chassis
│
└── README.md
```

All lesson pages, lab guides, homework problems, and project specifications live on the **[course wiki](https://github.com/shawnlinu/EECE5580-Classical-Control-Systems/wiki)**.

---

## Course Wiki

**[https://github.com/shawnlinu/EECE5580-Classical-Control-Systems/wiki](https://github.com/shawnlinu/EECE5580-Classical-Control-Systems/wiki)**

The wiki is the primary course reference. It contains:
- Lesson pages with full derivations, equations, and Python examples
- Step-by-step lab procedures with complete, runnable code
- Homework problem sets
- Quick-reference cheat sheets (PID formulas, root locus rules, Bode rules)
- A comprehensive troubleshooting guide for both hardware and software

Pages are added as the semester progresses — check back regularly.

---

## Grading at a Glance

| Component | Weight |
|-----------|--------|
| Homework (4 sets) | 25% |
| Lab reports (7 labs) | 25% |
| Midterm exam | 20% |
| Final project (robot + report + race) | 30% |

---

*"No guts, no glory. No fun, no story." — R. G. Nuranen*
