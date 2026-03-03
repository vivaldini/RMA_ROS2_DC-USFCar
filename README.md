# RMA_ROS2_DC-USFCar

This repository provides the software framework used in the Autonomous Mobile Robots (RMA) course at UFSCar, based on ROS 2 and simulation environments. 
|Component                       |  Version/Setup           | 
| ---------------------------- | ------------------------ |
| Operating System             | Ubuntu 24.04.3 LTS       |
| Robot Operatin System        | ROS 2 - Jazzy
| MRS System                      | [ROS2 MRS UAV system](https://github.com/ctu-mrs/mrs_uav_system/tree/ros2?tab=readme-ov-file#multi-robot-systems-group-uav-system)      | 
| Gazebo                         | Gazebo multi-robot simulator - version 11.13.0     | 


## [Step 1 - Ubuntu 24.04.3 LTS](https://github.com/vivaldini/robotics-and-ros-tutorials/blob/main/Tools-Tutorials/Ubuntu/Ubuntu24.04.3.md)

## Step 2 - Preparing the Environment 

> [!IMPORTANT] 
>### [Install Graphics card/Nvidia](https://github.com/vivaldini/robotics-and-ros-tutorials/tree/main/Tools-Tutorials/Nvidia)

## Step 3 - VS Code

Install VS Code

```bash
sudo snap install code -- classic
```

In VS Code, Extensions (CTRL + Shift + X ) search for the "Robot Developer Extensions for ROS 2" extension from "Ranch Hand Robotics LLC" and install this one instead.

## Step 4 - Install Terminator (Terminal Manager)

Terminator allows you to split the terminal into multiple panes, which is very useful when working with ROS 2, simulations, and multiple nodes simultaneously.

### Installation
```bash
sudo apt-get update
sudo apt-get install terminator
```

### Basic Shortcuts

| Shortcut | Action |
|---------------------|-----------------------------|
| `Ctrl + Shift + O` | Split terminal horizontally |
| `Ctrl + Shift + E` | Split terminal vertically |
| `Ctrl + Shift + X` | Maximize current terminal |
| `Ctrl + Shift + W` | Close current terminal |

[Terminator Keyboard Shortcuts and Options](https://github.com/igniteflow/terminator-keyboard-shortcuts)

## Step 5 - Text editor

You can use any text editor of your preference to edit configuration files and scripts.

### Option 1 - Gedit (Simple GUI Editor)

```bash
sudo apt-get install gedit
```

###  Other Recommended Editors

-  `nano` (beginner-friendly, terminal-based)

-  `vim` (advanced, terminal-based)

-  `VS Code` (full-featured IDE) 


## Step 6 - ROS 2 environment

### [Install and configure your ROS 2 Jazzy Jalisco](https://github.com/vivaldini/robotics-and-ros-tutorials/blob/main/ROS-Tutorials/ROS2_jazzy.md)

