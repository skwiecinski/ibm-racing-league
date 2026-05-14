# IBM AI Racing League 2026 - Team LeCoders

**Technologies:** Python 3.x | **Simulator:** TORCS | **AI Assistant:** IBM Granite

This repository contains the source code for our autonomous driver, developed for the **IBM AI Racing League – Country Challenge 2026**. Our agent controls a car in the TORCS (The Open Racing Car Simulator) environment, optimizing lap times while maintaining a flawless racing line.

---

## About the Project

The goal of this project was to build Python-based software capable of autonomously navigating a racing track by reacting in real-time to sensor data (e.g., speed, angle, distance from track edges).

### Our Approach
We started by building a simple, cautious, rule-based controller with a safe speed limit. From there, we optimized our control algorithms (steering, acceleration, and braking), which allowed us to achieve a smooth, stable run and set a highly competitive qualifying lap time.

---

## Requirements

To run this project on your local machine, you will need:
* **Python 3.x**
* **TORCS Simulator** (The Open Racing Car Simulator)
* **SCR Patch** (Simulated Car Racing) installed in the main game directory.

---

## Installation and Setup

1. **Clone the repository:**
   `git clone https://github.com/skwiecinski/ibm-racing-league`

2. **Prepare the TORCS simulator:**
   * Launch the TORCS game.
   * Navigate to: `Race` -> `Quick Race` -> `Configure Race`.
   * In the drivers section, select only one bot: `scr_server 1`.
   * Choose a track and start the race (`New Race`). The game will pause, waiting for a UDP server connection on port 3001.

---

## How to Run

Once TORCS is waiting at the starting line, execute our main script in your terminal:

`python torcs_jm_par.py`

---

## Repository Structure

* `torcs_jm_par.py` - The core file containing the logic for our autonomous driver (steering angle calculations, speed control).
* `snakeoil3_gym.py` - The UDP client providing the communication interface, specifically tailored for integration with the Gym environment.
* `snakeoil3_jm2.py` - An alternative UDP client providing direct communication between our Python scripts and the TORCS simulator.
* `gym_torcs.py` - The OpenAI Gym environment wrapper that bridges the Reinforcement Learning agent with the TORCS simulator.

---

## IBM Granite Usage

In accordance with the competition guidelines, we actively utilized the **IBM Granite** family of models throughout our development process. This AI tool assisted us with:
* **Code Generation:** Quickly building the skeleton of our Python classes and the main operational loop.
* **Refactoring & Debugging:** Analyzing UDP communication errors with TORCS and optimizing our code structure for improved readability and performance.
* **Documentation:** Helping formulate clear, concise code comments and structuring this README.md file.

---

### Hotlap

Youtube playlist of our hotlaps - https://www.youtube.com/playlist?list=PLuDfD_42YwUmNA1c_ylSWtB4cw8wVigCp

---

## Team LeCoders
* **Szymon Kwieciński**
* **Krzysztof Bieszczad**
* **Marek Znamirowski**
* **Mateusz Chęciński**
* **Kamil Karwacki**
