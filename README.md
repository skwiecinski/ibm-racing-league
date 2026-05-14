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

The connection will be established via the `snakeoil3.py` client, and the car will automatically start driving using our algorithm.

---

## Repository Structure

* `torcs_jm_par.py` - The core file containing the logic for our autonomous driver (steering angle calculations, speed control).
* `snakeoil3.py` - The UDP client providing the communication interface between our Python script and the TORCS simulator.
* `lap_video.mp4` - A video recording of our fastest qualifying lap.

---

## IBM Granite Usage

In accordance with the competition guidelines, we actively utilized the **IBM Granite** family of models throughout our development process. This AI tool assisted us with:
* **Code Generation:** Quickly building the skeleton of our Python classes and the main operational loop.
* **Refactoring & Debugging:** Analyzing UDP communication errors with TORCS and optimizing our code structure for improved readability and performance.
* **Documentation:** Helping formulate clear, concise code comments and structuring this README.md file.

---

## Team LeCoders
* **Szymon Kwieciński**
* **Krzysztof Bieszczad**
* **Marek Znamirowski**
* **Mateusz Chęciński**
* **Kamil Karwacki**
