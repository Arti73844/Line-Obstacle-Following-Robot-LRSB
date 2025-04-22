# 🤖 Line and Obstacle-Following Robot Using LRSB Algorithm

An autonomous robot built using the **LRSB (Left-Right-Straight-Back)** pathfinding algorithm. It intelligently follows lines and avoids obstacles in real-time using sensor-based feedback mechanisms and embedded C programming.

---

## 🚀 Project Overview

- **Goal:** Create an intelligent mobile robot capable of line-following and dynamic obstacle avoidance.
- **Algorithm:** LRSB - a rule-based algorithm prioritizing Left → Right → Straight → Back decisions.
- **Microcontroller Logic:** Real-time path correction via embedded C code.

---

## 🧰 Tools & Components

| Component         | Purpose                          |
|------------------|----------------------------------|
| IR Sensors        | Line detection                   |
| 1D Sonar Sensor   | Obstacle detection               |
| L298 Motor Driver | Dual motor control               |
| BO Motors         | Robot mobility                   |
| Microcontroller   | Logic implementation             |
| Embedded C        | Core programming language        |

---


## 🧠 How the LRSB Algorithm Works

1. **Left:** First check if left path is open
2. **Right:** If left is blocked, check right
3. **Straight:** If both sides are blocked, attempt straight
4. **Back:** If all fail, rotate 180° to backtrack

```c
if (left_clear) {
    turnLeft();
}
else if (right_clear) {
    turnRight();
}
else if (straight_clear) {
    moveForward();
}
else {
    turnBack();
}

----
├── code/
│   └── main.c                  # Embedded C code
├── docs/
│   └── circuit.png             # Circuit diagram
├── media/
│   └── demo.gif / demo.mp4     # Demo visuals
├── README.md                   # Project description

----
⚙️ How to Run
Upload main.c code to the microcontroller (e.g., ATmega328 or 8051).

Power the motor driver and sensor setup via regulated 5V supply.

Place the robot on a marked line and observe obstacle avoidance in action!

📚 Learnings
Embedded systems programming in C

Real-time sensor feedback control

Implementing custom logic algorithms for mobile robots

Hardware-software interaction

🌟 Future Improvements
Add PID control for smoother line-following

Use 2D LiDAR for improved obstacle detection

Implement SLAM for advanced navigation
