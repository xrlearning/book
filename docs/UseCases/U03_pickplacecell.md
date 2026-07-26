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

The Pick & Place Cell is an automated manufacturing system designed to execute handling, sorting, and transfer operations in a discrete production environment. The cell's behavior is governed by event-driven logic where sensors and digital actuators interact to determine the system's response to operating conditions. Communication within the system can be managed through industrial protocols like Modbus TCP/IP or MQTT.

The virtual pick&place cell consists of several assets (see Figure 1-Figure 9):

- Conveyors: The scene includes two main conveyor belts, Conveyor 1 and Conveyor 2. Conveyor 1 carries boxes to be filled, while Conveyor 2 transports the items that will be picked up.

- Detection Barriers: Both conveyors are equipped with sensor-receiver pairs that detect the presence, passage, and correct positioning of objects.

- Cartesian Robot: A programmable robotic arm is primarily aimed at picking individual items from Conveyor 2 and place them into boxes on Conveyor 1.

- Objects: The system manipulates two types of objects, i.e. items (Simple-shaped parts that are picked from Conveyor 2 and placed into boxes) and boxes (containers that move along Conveyor 1 to be filled with items by the robot).

- Control Panel: the main user interface. It is equipped with four physical buttons (Start, Stop, Initialization, Emergency) and a three-position State Selector for choosing the operational mode. A potentiometer is also included to select the number of items to be placed in each box.

- Signal Pole: A vertical pole with three lights (red, yellow, green) provides visual feedback on the system's operational status.

- Unloading Slides: Located at the end of each conveyor, these slides enable the physical evacuation of materials once processing is complete.

- Protective Grids: The cell also includes solid grids to protect critical areas and perforated grids that support functional elements like the Control Panel.

<img src="U03_media/image1.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 1: Cartesian robotic arm used for pick and place operations.

<img src="U03_media/image2.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 2: Basic item shape manipulated by the robot.

<img src="U03_media/image3.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 3: Transport box used for item collection.

<img src="U03_media/image4.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 4: Control Panel with physical interface (buttons, selectors)

<img src="U03_media/image5.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 5: Slide used for unloading processed items

<img src="U03_media/image6.jpeg" style="width:2.63125in;height:1.32604in" />

Figure 6: Conveyor belt with motor for item transport

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

The basic system configuration is designed to operate in distinct production modes:

- State 0: parts enter Conveyor2; parts go through Conveyor2; parts are evacuated if the Mode0 stops.

- State 1: boxes enter Conveyor1; boxes are picked and placed on Conveyor2; boxes exit from Conveyor2.

- State 2: the user selects the number of parts to be put in the box; parts and boxes appear on Conveyor2 and Conveyor1, respectively; both conveyors move; sensors detect parts and boxes; parts picked from Conveyor2 and placed in a box on Conveyor1; Conveyor1 moves.


The [visualization of this use case](https://difactory.github.io/DF/scenes/UC/PickPlaceCell_old.html) in a VR environment is supported by [VEB.js](../Tools#vebjs).
