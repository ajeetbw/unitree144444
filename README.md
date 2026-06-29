# Unitree Robot SDK Version 2
Unitree Robot SDK Version 2 is a comprehensive software development kit designed to provide a seamless interface for interacting with Unitree robots. This SDK enables developers to create custom applications, integrate with existing systems, and leverage the capabilities of Unitree robots.

## Project Description
The Unitree Robot SDK Version 2 is built to provide a robust and flexible framework for developing robot applications. It offers a wide range of features, including motion control, sensor integration, and communication protocols. This SDK is designed to support various use cases, from research and development to industrial automation and robotics applications.

## Tech Stack
The Unitree Robot SDK Version 2 is built using a combination of technologies, including:
* **Programming Languages:** C++, Python
* **Frameworks:** CMake, GCC
* **Libraries:** Eigen, Boost, YAML-CPP, SPDLOG, FMT
* **Operating Systems:** Ubuntu 20.04 LTS (supported on both aarch64 and x86_64 architectures)

## Installation and Startup
To install and start using the Unitree Robot SDK Version 2, follow these steps:

### Prerequisites
* Install the required dependencies: `apt-get update` and `apt-get install -y cmake g++ build-essential libyaml-cpp-dev libeigen3-dev libboost-all-dev libspdlog-dev libfmt-dev`

### Building the SDK
1. Create a build directory: `mkdir build`
2. Navigate to the build directory: `cd build`
3. Run CMake: `cmake ..`
4. Build the SDK: `make`

### Installing the SDK
To install the SDK system-wide, run: `sudo make install`
Alternatively, to install the SDK to a custom directory (e.g., `/opt/unitree_robotics`), use: `cmake .. -DCMAKE_INSTALL_PREFIX=/opt/unitree_robotics` followed by `sudo make install`

## Basic Usage
The Unitree Robot SDK Version 2 provides a range of APIs for controlling and interacting with Unitree robots. For example, the `state_machine` module allows you to define and execute custom state machines, while the `h1` module provides an interface for controlling the H1 robot's parallel mechanism.

### State Machine Example
To use the state machine module, create a `params.json` file with the desired configuration:
```json
{
    "dt": 0.01,
    "kp": 40.0,
    "kd": 1.0,
    "init_pos": [
        0.0,
        0.9,
        -1.8,
        0.0,
        0.9,
        -1.8,
        0.0,
        0.9,
        -1.8,
        0.0,
        0.9,
        -1.8
    ]
}
```
Then, use the `state_machine` API to load and execute the state machine.

### H1 Parallel Mechanism Control
The H1 parallel mechanism control interface provides a range of commands for controlling the robot's ankle joints. For example, you can use the `PR Mode` to control the pitch and roll joints directly.

| Command Name            | Variable |
| ----------------------- | -------- |
| Feedforward Torque      | `tau`    |
| Target Angle            | `q`      |
| Target Angular Velocity | `dq`     |
| Joint Stiffness         | `kp`     |
| Joint Damping           | `kd`     |

## Contributing
The Unitree Robot SDK Version 2 is an open-source project, and we welcome contributions from the community. To contribute, please fork the repository, make your changes, and submit a pull request.

## Licensing
The Unitree Robot SDK Version 2 is licensed under the [MIT License](https://opensource.org/licenses/MIT). By using or contributing to this project, you agree to the terms and conditions of the license.