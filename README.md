# Environment-Driven Exploration in Reinforcement Learning

This repository explores how **environment-driven changes** can affect exploration and behavior in reinforcement learning-based locomotion tasks.

The project studies three experimental settings:

- **Dropout-based correlated noise**
- **Gravity change during training / evaluation**
- **Position target change across episodes**

The experiments are presented on two locomotion agents:

- **HalfCheetah**
- **Ant**

## Project Overview

Instead of only modifying the learning algorithm, this work investigates how changing parts of the environment or control dynamics can influence exploration behavior in reinforcement learning.

The repository contains modified source files, experiment seeds, and visual results for different environment-driven exploration strategies.

## Repository Structure

```text
.
├── effect_ of_ correlated_noise/
│   ├── dropout_experiment/
│   ├── gravity_change_experiment/
│   ├── position_change_experiment/
│   └── Readme.md
├── gif/
│   ├── ant_dropout.gif
│   ├── ant_gravity.gif
│   ├── ant_position.gif
│   ├── half_cheetah_dropout.gif
│   ├── half_cheetah_gravity.gif
│   ├── half_cheetah_position.gif
│   └── half-cheetah_position2.gif
└── README.md
```

## Experiments

### 1. Dropout Experiment

This experiment applies **correlated noise using dropout** inside the policy / network behavior.

- Modified file: `evonet.cpp`
- Experiment folders contain seeds for both robots:
  - `ANT_seeds`
  - `cheetah_seeds`

#### Results

**HalfCheetah**
<p align="center">
  <img src="./gif/half_cheetah_dropout.gif" alt="HalfCheetah Dropout Experiment" width="45%">
</p>

**Ant**
<p align="center">
  <img src="./gif/ant_dropout.gif" alt="Ant Dropout Experiment" width="45%">
</p>

---

### 2. Gravity Change Experiment

This experiment modifies the locomotion setup by changing the value of the **gravity function**.

- Modified file: `robot_locomotors.py`
- Purpose: test how gravity variation affects locomotion behavior and exploration
- Experiment folders contain seeds for both robots:
  - `ANT_seeds`
  - `cheetah_seeds`

#### Results

**HalfCheetah**
<p align="center">
  <img src="./gif/half_cheetah_gravity.gif" alt="HalfCheetah Gravity Change Experiment" width="45%">
</p>

**Ant**
<p align="center">
  <img src="./gif/ant_gravity.gif" alt="Ant Gravity Change Experiment" width="45%">
</p>

---

### 3. Position Change Experiment

This experiment changes the locomotion target position by modifying `self.walk_target_x` across episodes.

- Modified file: `robot_locomotors.py`
- Purpose: study how changing the target position influences exploration and locomotion adaptation
- Experiment folders contain seeds for both robots:
  - `ANT_seeds`
  - `cheetah_seeds`

#### Results

**HalfCheetah**
<p align="center">
  <img src="./gif/half_cheetah_position.gif" alt="HalfCheetah Position Change Experiment" width="45%">
  <img src="./gif/half-cheetah_position2.gif" alt="HalfCheetah Position Change Experiment 2" width="45%">
</p>

**Ant**
<p align="center">
  <img src="./gif/ant_position.gif" alt="Ant Position Change Experiment" width="45%">
</p>

## Summary

This repository presents a small set of reinforcement learning locomotion experiments where **environmental changes** are used as a mechanism to influence exploration and agent behavior.

The main idea is to evaluate how different perturbations or task modifications — such as **dropout noise**, **gravity variation**, and **position target change** — affect learned locomotion on standard benchmark robots.

## Notes

- Each experiment folder contains its own code modification and seed setup.
- Inner experiment READMEs have been consolidated here into one top-level summary.
- The GIFs provide qualitative results for comparing behavior across the different settings.

## Author

**Muhammad Ilyas Raza**  
Machine Learning | Computer Vision | Robotics | Applied AI
