# Swerve_robot
This is my take on creating a controller for 4 wheeled swerve robot
# Swerve Drive Robot ROS2 Package

This repository contains a ROS2 package for the control of a 4-wheeled swerve drive robot. The package includes:

- A Gazebo simulation environment.
- Joystick control integration.
- A custom controller node for operating the robot.

## Package Overview

The ROS2 package provides launch files and nodes to simulate and control a swerve drive robot. Below is a step-by-step guide to get started.

## Installation

1. Ensure you have ROS2 installed on your system. Refer to the [ROS2 installation guide](https://docs.ros.org/en/rolling/Installation.html) for your platform.
2. Clone this repository into your ROS2 workspace:

    ```bash
    cd ~/ros2_ws/src
    git clone https://github.com/<your-username>/Swerve_robot.git
    ```
3. Build the package:

    ```bash
    cd ~/ros2_ws
    colcon build
    ```
4. Source the workspace:

    ```bash
    source ~/ros2_ws/install/setup.bash
    ```

## Usage

### 1. Launch the Gazebo Simulation

To start the Gazebo simulation environment for the robot, run:

```bash
ros2 launch amr_description gazebo.launch.py
```

### 2. Start the Joystick Controller

If you want to control the robot using a joystick, run:

```bash
ros2 launch amr_description joystick.launch.py
```

Ensure your joystick is connected and recognized by the system.

### 3. Run the Controller Node

To operate the custom controller node for the swerve drive robot, execute:

```bash
ros2 run amr_description controller
```

## File Structure

```
├── amr_description
│   ├── launch
│   │   ├── gazebo.launch.py
│   │   ├── joystick.launch.py
│   ├── amr_description
│   │   ├── controller.py
│   ├── urdf
│   │   ├── robot.urdf.xacro
│   ├── config
│   │   ├── joystick.yaml
│   └── ...
```

## Features

- **Gazebo Simulation**: A realistic environment to test and visualize robot movements.
- **Joystick Control**: Seamless integration with joystick devices for manual control.
- **Custom Controller**: An optimized node for operating a swerve drive mechanism.

## Contributing

Contributions are welcome! If you encounter any issues or have suggestions for improvement, feel free to open an issue or submit a pull request.



Happy swerving!
