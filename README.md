# CubeSat Attitude Determination & Control System (ADCS)

A full 3-axis attitude determination and control simulation for a 3U CubeSat, built in Python from scratch.

## What it does
Simulates the brain that keeps a satellite pointed in the right direction while flying through space. Without this, a satellite tumbles randomly and becomes useless — cameras can't take pictures, antennas can't talk to Earth, solar panels don't face the sun.

## What is simulated
- Quaternion kinematics and Euler rigid body dynamics
- PD controller with reaction wheel actuator saturation (1 mNm limit)
- Three real disturbance torques: gravity gradient, solar radiation pressure, magnetic
- Gyroscope bias and sensor noise
- TRIAD algorithm for attitude estimation from magnetometer and sun sensor

## Results
- Controller stabilizes a 30° off-axis tumbling CubeSat to within 0.02° in under 10 seconds
- TRIAD attitude estimation error stays under 1° steady state over 120 seconds
- Quaternion norm holds at 1.00000 throughout — zero numerical drift

## Tools
Python, NumPy, SciPy, Matplotlib, Jupyter Notebook

## Real world application
Every satellite in orbit has a version of this running on it — Hubble, Planet Labs, Starlink, GPS. This simulation replicates the core math used in real flight software.

## Author
Salim Saadoon — Aerospace Engineering Student, Wichita State University
