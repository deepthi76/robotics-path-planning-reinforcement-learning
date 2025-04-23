# Project Description:	
This project presents a reinforcement learning-based framework for autonomous robot navigation using Deep Reinforcement Learning (DRL) in a simulated environment built on ROS 2 and Gazebo. The robot is trained to perform goal-directed navigation tasks in complex indoor environments by learning policies that map sensor observations (mainly LiDAR data) to velocity commands, without relying on traditional path-planning algorithms.
A practical scenario of autonomous delivery systems is considered for this project. In such systems, delivery robots are expected to travel between various locations (e.g : pickup points and dispatch locations) while adapting to dynamic and cluttered environments. Traditional methods like A* or Dijkstra’s algorithms require pre-mapped routes and cannot easily handle dynamic obstacles or unpredictable layouts. DRL enables robots to learn optimal behavior directly from trial and error, improving adaptability and decision-making in real-world conditions.
By interacting with the environment, the robot learns to navigate from arbitrary start positions to dynamically changing goal points while minimizing the number of collisions and optimizing travel time.

#Project Objectives:
The primary objectives of the project are:
Train a robot using DRL to reach dynamic target positions while avoiding static and dynamic obstacles.
Integrate the learning agent into a ROS 2 ecosystem, enabling real-time simulation and future transfer to physical robots.
Visualize the performance of modern DRL algorithms (TD3 and SAC) for continuous navigation tasks.
Apply the learned navigation strategy to a delivery scenario, such as routing between various drop-off and pick up points in a warehouse.
For example, in an urban food delivery scenario, an autonomous robot might be tasked with delivering an order from a restaurant kitchen to a customer’s apartment within a residential complex or university campus. Rather than relying on fixed GPS paths—which may not account for real-time changes like roadblocks, pedestrians, or construction—the DRL-trained robot can dynamically adjust its route based on the environment.

#System Design
The system uses ROS 2 and Gazebo to simulate an autonomous food delivery robot navigating toward specified goals in an urban or campus-like setting. The robot is a differential-drive mobile platform equipped with a 2D LiDAR sensor that provides 360° obstacle detection.
Each delivery task is modeled as a navigation goal—e.g., delivering food from a restaurant (start) to a customer’s apartment or hostel room (goal). The robot must navigate through walkways, corridors, or shared spaces while avoiding collisions with pedestrians, bikes, and other delivery robots.
The core ROS 2 nodes include:
Observation Node: Collects LiDAR scans and goal position (distance and angle).
Action Node: Converts learned actions into ROS 2 velocity commands.
Reward Node: Computes real-time feedback based on navigation performance.
This modular setup allows seamless testing and retraining of delivery policies in varied simulated environments that closely resemble real-world delivery zones.

