---
title: Pick & Place Cell
layout: default
nav_order: 3
parent: Use Cases
---

{:.no_toc}
<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details> 


# Pick & Place Cell
{:.no_toc}

## Description

The Pick & Place Cell is an automated manufacturing system designed to execute handling, sorting, and transfer operations in a discrete production environment. The cell's behavior is governed by event-driven logic where sensors and digital actuators interact to determine the system's response to operating conditions. Communication within the system can be managed through industrial protocols like Modbus TCP/IP or MQTT.

The virtual pick&place cell consists of several assets (see Figure 1-Figure 9):

- Cartesian Robot: A programmable robotic arm is primarily aimed at picking individual items from Conveyor 2 and place them into boxes on Conveyor 1 (Figure 1).

- Objects: The system manipulates two types of objects, i.e. items (Simple-shaped parts that are picked from Conveyor 2 and placed into boxes) and boxes (containers that move along Conveyor 1 to be filled with items by the robot). See Figures 2 and 3.

- Control Panel: the main user interface (Figure 4). It is equipped with four physical buttons (Start, Stop, Initialization, Emergency) and a three-position State Selector for choosing the operational mode. A potentiometer is also included to select the number of items to be placed in each box.

- Conveyors: The scene includes two main conveyor belts, Conveyor 1 and Conveyor 2. Conveyor 1 carries boxes to be filled, while Conveyor 2 transports the items that will be picked up. (Figure 5)

- Unloading Slides: Located at the end of each conveyor, these slides enable the physical evacuation of materials once processing is complete. (Figure 6)

- Signal Pole: A vertical pole with three lights (red, yellow, green) provides visual feedback on the system's operational status. (Figure 7)

- Protective Grids: The cell also includes solid grids to protect critical areas and perforated grids that support functional elements like the Control Panel. (Figure 8)

- Detection Barriers: Both conveyors are equipped with sensor-receiver pairs that detect the presence, passage, and correct positioning of objects. (Figure 9)

## Digital Model

The [scene configuration](https://xrlearning.github.io/repo/UseCases/PickPlaceCell/PickPlaceCell.json) and the [3D models](https://github.com/xrlearning/repo/tree/main/UseCases/PickPlaceCell/models) (Fugures 1-9) of the use case are available online. The [use case can be visualized](https://xrlearning.github.io/repo/UseCases/PickPlaceCell/PickPlaceCell.html) using [VEB.js](../Tools#vebjs) tool (see Figures 10 and 11).


<img src="U03_media/image1.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 1: Cartesian robotic arm used for pick and place operations.

<img src="U03_media/image2.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 2: Basic item shape manipulated by the robot.

<img src="U03_media/image3.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 3: Transport box used for item collection.

<img src="U03_media/image4.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 4: Control Panel with physical interface (buttons, selectors)

<img src="U03_media/image6.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 5: Conveyor belt with motor for item transport

<img src="U03_media/image5.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 6: Slide used for unloading processed items

<img src="U03_media/image7.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 7: Signal pole indicating system state.

<img src="U03_media/image8.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 8: Perforated protective grid supporting the Control Panel

<img src="U03_media/image9.jpeg" style="width:3.12021in;height:1.61854in" />

Figure 9: Barrier sensors for object detection on conveyors

The whole cell and each of its assets are shown in Figure 10 and Figure 11.

<img src="U03_media/image10.jpeg" style="width:5.5in;height:3.37602in" />

Figure 10: Full view of the Pick&Place cell.

<img src="U03_media/image11.jpeg" style="width:5.54781in;height:3.12931in" />

Figure 11: Full view of the Pick&Place cell, including labels of each asset.
