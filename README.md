# CustomRobotGazebo
Structural design of autonomous car in xacro for Gazebo simulation

# Custom Robot Model for ROS and Gazebo

This project contains a custom mobile robot model developed using Xacro/URDF
for simulation in ROS and Gazebo.

The goal was to create a configurable four-wheel robotic platform that could
be used for autonomous robotics experiments, including sensor integration,
navigation, mapping, and later physical prototyping.

## Features

- Custom robot body geometry
- Four-wheel mobile platform
- Reusable Xacro macros for wheels and legs
- Continuous wheel joints
- Collision and visual models
- Inertial properties for simulation
- Gazebo friction and contact parameters
- ROS control transmissions
- `gazebo_ros_control` integration
- LiDAR integration through Xacro
- Parameterized dimensions for robot body and wheels

## Robot Structure

The model uses Xacro properties to define key dimensions such as:

- Wheel diameter and width
- Body length, width, and height

Reusable Xacro macros are used to generate the robot's wheel and leg
components, reducing duplicated URDF code.

## Gazebo Integration

Gazebo-specific parameters are defined for the wheel links, including:

- Friction coefficients
- Contact stiffness and damping
- Simulation material properties

Each wheel joint is connected to a transmission using
`VelocityJointInterface`, allowing the model to be integrated with ROS control.

The model also loads the `gazebo_ros_control` plugin for simulated actuator
control.

## Sensors

The model was designed with LiDAR integration in mind and includes a Xacro
include for Gazebo LiDAR simulation.

The broader project explored using this robot architecture for autonomous
navigation, mapping, and parking-related robotics experiments.

## Technologies

- ROS
- Gazebo
- Xacro
- URDF
- `gazebo_ros_control`
- Robot kinematics
- LiDAR integration

## Project Context

This work was developed as part of autonomous robotics research and prototyping.
It was intended to provide a simulation model before implementation and testing
on physical robotic hardware.
