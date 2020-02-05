---
layout: post
title: Shell EcoMarathon Asia 2019
category: projects
---

Developing an autonomous electric race car.

## Introduction

![<img src="{{ site.baseurl }}/images/project_images/semautoteam.JPG" alt="Team photo of NTU SEM 2019 Autonomous"/>]()

Shell EcoMarathon is a competition held by Shell for universities to develop the most efficient track vehicles. Contestants are judged based on speed, efficiency and a race. In 2019, an Autonomous Vehicle category was added.

## Overview of Task

![<img src="{{ site.baseurl }}/images/project_images/semauto.jpg" alt="An image of the autonomous car"/>]()

 - Design a system to translate navigation instructions from a Jetson TX2 to the signals required by the actuators
 - Design the overall system architecture of the car
 - Suggest sensors required to augment the Velodyne LIDAR system

## Outcomes

### Translation System
I settled on an Arduino-based embedded platform, a Teensy 3.5, due to its fast processor and 5V input-tolerance.

I also prototyped a circuit to allow for connections to various actuator controllers, sensors, and the Jetson TX2, keeping in mind modularity of components in the circuit to allow for fast replacement in the event of a device malfunction.

The firmware of the system I wrote allowed access to sensor data. It also had a PID controller in place to allow for better positioning accuracy and speed. Finally, it had debug options with support for remote control operation as well as ROS support through the use of ROSSerial.

### System Architecture

I designed and advised the hardware and computing team on the possible architecture of the car, to ensure reliable operation and graceful failures. Redundancy and safeguards were put in place to ensure safety of everyone working on the car.

### Sensor Augments
Based on the requirements of the tasks within the competition, I suggested the use of a Radar system and an ultrasonic rangefinder system to augment the LIDAR of the car for near-range and far-range obstacles. The ultrasonic rangefinders also helped to cover the blind spots of the single LIDAR due to its mounting position on the car.

The pros and cons of each sensor system was weighted to ensure each covers the other's weaknesses. Implementation issues were discussed to ensure we had a strong understanding of the possible limitations and pitfalls of the sensors.

## Conclusion

![<img src="{{ site.baseurl }}/images/project_images/semteam.JPG" alt="Team photo of NTU SEM 2019"/>]()

While the competition category was withdrawn in the end (due to the lack of autonomous competitors), I have gained a lot through my own research during the development of this car, as well as through discussing various issues with those who have expertise in differing areas.

The autonomous car was in the end stripped of autonomy and put in to the efficiency category instead, where it got respectable results despite it being an autonomy-first vehicle.

(Here's a video of a low speed control test of the car via remote control)

<iframe width="560" height="315" src="https://www.youtube.com/embed/9p-S8K_eDsI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen> </iframe>