# ROS 2 TurtleSim Spiral Publisher and Subscriber

This repository contains a ROS 2 package that demonstrates a simple publisher-subscriber mechanism using TurtleSim. The publisher sends linear and angular velocity commands to control the movement of the turtle in a spiral pattern, while the subscriber listens to the velocity commands and logs them.

## Package Contents

- **Publisher Node:** `MinimalPublisher` - Publishes velocity commands to control the turtle's movement.
- **Subscriber Node:** `MinimalSubscriber` - Subscribes to the velocity topic and logs the received commands.

https://github.com/user-attachments/assets/686e0a66-9b57-48f0-a74e-491654a8ef95

## Requirements

- ROS 2 Humble
- Python 3

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/SwekeR-463/ROS2.git
cd ROS2
```

## Build the Package
```bash
colcon build --packages-select py_spiral
source install/setup.bash
```
## Run the Publisher Node
```bash
ros2 run py_spiral py_spiral_pub <linear_velocity> <initial_angular_velocity> <angular_increment>
```
## Example
To run the publisher node with a linear velocity of 2.0, an initial angular velocity of 1.0, and an angular increment of 0.1, use:
```bash
ros2 run py_spiral py_spiral_pub 2.0 1.0 0.14
```
## Run the Subscriber Node
In another terminal, run the subscriber node to listen to the velocity commands:
```bash
ros2 run py_spiral py_spiral_sub
```
## Example Output
The subscriber will log messages similar to the following:
```bash
[INFO] [<timestamp>]: Received - Linear Velocity : 2.000000, Angular Velocity : 1.100000
```
