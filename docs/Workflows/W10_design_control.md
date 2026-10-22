---
title: System Design&Control
layout: default
nav_order: 11
parent: Learning Workflows
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
 

# Design and Control of Manufacturing Systems
{:.no_toc}

This learning workflow addresses the design and control of a manufacturing system using modern digital technologies, with particular emphasis on extended reality (XR). It guides students through a practical, hands-on learning experience based on a realistic virtual environment representing a manufacturing facility. By integrating pedagogical and technical elements, the workflow supports the development of industrial engineering knowledge and skills.

The workflow is based on a digital twin of a pick-and-place cell. The use of open and cross-platform technologies is recommended to make this XR-based learning approach more accessible and reusable in higher education.


## 1. Learning Objectives

The knowledge addressed by this learning workflow is organised into four categories: factual, conceptual, procedural, and metacognitive knowledge.

**1. Factual Knowledge**

- **1.1** *Knowledge of terminology*: ability to recognize and differentiate between various types of equipment and components within a manufacturing system. This includes knowing terms such as conveyor, robot, sensor, actuator, control panel, etc.

- **1.2** *Knowledge of specific details and elements*: ability to identify the role and properties of assets, e.g. functioning states of an actuator, range of action of a sensor, source and destination of parts.

**2. Conceptual Knowledge**

- **2.1** *Knowledge of classifications and categories*: ability to classify equipment based on its function within the manufacturing system, such as a Cartesian robot for handling and a conveyor for transportation.

- **2.2** *Knowledge of principles and generalizations*: ability to comprehend how the parts are moved within the manufacturing system, specifically the event-driven logic where sensors and actuators interact to control the system's response.

- **2.3** *Knowledge of theories, models, and structures*: ability to understand how the system's behavior is defined via UML statecharts.

**3. Procedural Knowledge**

- **3.1** *Knowledge of subject-specific skills and algorithms:* ability to define goals and process plans of a manufacturing system*;* ability to apply performance evaluation techniques; ability to use a communication protocol like MQTT to control a manufacturing system; ability to program the behavior of actuators.

- **3.2** *Knowledge of subject-specific techniques and methods:* ability to model the behavior of sensors and actuators using UML statecharts; ability to design an integrated manufacturing system considering the behavior of the single assets.

- **3.3** *Knowledge of criteria for determining when to use appropriate procedures*: ability to analyze system behavior and identify when a component is not performing as expected, allowing the student to troubleshoot and apply corrective procedures.

**4. Metacognitive Knowledge**

- **4.1** *Self-knowledge:* ability to evaluate one's own confidence in the responses and solutions to the exercises.

Table 1 summarises the intended learning outcomes (ILOs) and their associated knowledge types.

| **ILO** | **Knowledge type** | **ILO description**                                                                                                                                                                               |
|---------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| I1      | 1.1                | Identify sensors, actuators, and control panels                                                                                                                                                   |
| I2      | 1.2                | Understand the properties of assets, e.g. functioning states of an actuator, range of action of a sensor, source and destination of parts.                                                        |
| I3      | 2.1                | Understand the role of assets within the manufacturing system based on their function, such as a Cartesian robot for handling and a conveyor for transportation.                                  |
| I4      | 2.2                | Identify the flow of parts within the manufacturing system in the virtual environment, specifically the event-driven logic where sensors and actuators interact to control the system's response. |
| I5      | 2.3                | Understand the system's behavior by modeling UML statecharts.                                                                                                                                     |
| I6      | 3.1                | Define the goals and processes of a manufacturing system.                                                                                                                                         |
| I7      | 3.1                | Apply performance evaluation techniques to assess the performance of the system                                                                                                                   |
| I8      | 3.1                | Control a manufacturing system using a communication protocol like MQTT                                                                                                                           |
| I9      | 3.2                | Design the behavior of sensors and actuators using UML statecharts                                                                                                                                |
| I10     | 3.2                | Design an integrated manufacturing system considering the behavior of the single assets in a conceptual model of the system.                                                                      |
| I11     | 3.3                | Identify when an asset is not performing as expected and apply corrective procedures.                                                                                                             |
| I12     | 4.1                | Estimate the confidence with respect to replies and numerical solutions provided.                                                                                                                 |

Table 1: ILOs with associated knowledge type

## 2. Use Case

The workflow is applied to a [pick-and-place cell](../UseCases/U03_pickplacecell), an automated manufacturing system designed to perform handling, sorting, and transfer operations in a discrete-production environment.

The cell provides a testbed for:

- analysing the structure and behaviour of a manufacturing system;
- modelling sensors, actuators, and control logic;
- designing and evaluating system reconfigurations;
- testing control strategies through virtual commissioning;
- demonstrating the modularity and reusability of the XR learning workflow.



## 3. Learning Activities

The learning activities are organized into two levels of increasing difficulty:

1)  *Understanding how a manufacturing system operates and is controlled*. Students are provided with an existing manufacturing system in which the behaviour of sensors and actuators is represented through UML statecharts. A predefined sequence of control actions demonstrates how the system performs a production mission, such as moving parts from a source to a destination while carrying out the required operations.

2)  *Reconfiguring and controlling a manufacturing system*. Students design a reconfiguration of the existing manufacturing system to satisfy new production requirements. Existing assets may be reused, duplicated, or supplemented with new asset types and properties. Students define the process plan, model asset behaviour, configure the integrated system, evaluate its performance, and test its operation through virtual commissioning.

Each level consists of tasks associated with specifics ILOs as reported in Table 2.

| Task ID | Task | Description | Related ILOs |
|:--------|:-----|:------------|:-------------|
| T1.1 | Identify assets in the manufacturing system | Analyse the existing manufacturing system and identify its relevant assets. | I1 |
| T1.2 | Characterise existing assets | Document the properties and functions of the assets used in the manufacturing system, including sensors, actuators, Cartesian robots, conveyors, and control devices. | I2, I3 |
| T1.3 | Analyse the existing manufacturing system | Analyse system behaviour and the flow of parts. Represent the system layout using appropriate diagrams, model its behaviour using UML statecharts, and evaluate its performance. | I4, I5, I7 |
| T2.1 | Define the process plan | Define the production goal, required operations, and operation sequence for the reconfigured manufacturing system. | I6 |
| T2.2 | Design asset behaviour | Identify the assets required by the reconfigured system and model the behaviour of its sensors and actuators using UML statecharts. | I9 |
| T2.3 | Design the integrated system | Configure the manufacturing system by integrating individual assets and their behaviours. Define asset placement, component interactions, operating modes, and responses to user commands and sensor data. | I10 |
| T2.4 | Assess system performance | Evaluate the performance of the reconfigured manufacturing system using suitable indicators and compare the results with the specified requirements. | I7 |
| T2.5 | Perform virtual commissioning | Test the integrated system in the virtual environment. Operate the control panel, trigger system events, verify the operating logic, and test an MQTT-based controller against the production goals. | I8, I9, I10 |
| T2.6 | Conduct final testing and revisions | Test the complete system, identify unexpected behaviour, troubleshoot problems, implement revisions, and assess confidence in the proposed solutions. | I11, I12 |

*Table 2. Learning tasks and related intended learning outcomes.*

## 4. Technology

Virtual reality provides the level of immersion required for students to explore, analyse, and operate a virtual manufacturing system. The workflow can be accessed in desktop mode using a conventional web browser or in immersive mode using a compatible VR headset.

### 4.1 Assets and scene configuration
{:.no_toc}

A digital twin of the pick-and-place cell was developed to support teaching and research activities. The [online resources](../UseCases/U03_pickplacecell#online-resources) include:

- three-dimensional asset models in **glTF** format;
- scene configurations defined in JSON;
- structured data describing the assets and their relationships.

The JSON scene configuration follows a dedicated [schema](https://virtualfactory.gitbook.io/vlft/kb/instantiation/assets/json).

### 4.2 Visualisation with VEB.js
{:.no_toc}

The use case can be visualised using [VEB.js](../Tools#vebjs), a prototype web-based VR application built around a reconfigurable, model-driven approach.

The [Pick-and-Place Cell demo](https://difactory.github.io/DF/scenes/UC/PickPlaceCell_old.html) can be accessed through a compatible web browser without installing a dedicated desktop application.

### 4.3 Data authoring with OntoGuiWeb
{:.no_toc}

The digital model of the pick-and-place cell can be authored and explored using [OntoGuiWeb](../Tools#ontoguiweb). OntoGuiWeb provides a graphical interface for creating and examining model instances represented through OWL ontologies.

### 4.4 MQTT communication
{:.no_toc}

MQTT is a lightweight publish-subscribe messaging protocol commonly used in Internet of Things and industrial applications. Within this workflow, MQTT supports bidirectional communication between the virtual environment and an external controller.

The virtual environment can:

- publish messages describing the current states of sensors and other assets;
- subscribe to topics that provide commands for actuators;
- exchange messages structured according to an agreed JSON schema.

VEB.js can operate as both an MQTT publisher and subscriber. An external controller can therefore receive the current state of virtual assets, execute the control logic, and send commands back to the virtual environment.
## 5. User Experience

The user experience is designed to support intuitive exploration and interaction. The virtual environment represents a simplified industrial facility and allows students to examine the manufacturing system without the access, safety, and scheduling constraints associated with physical equipment.

Students can explore the environment and retrieve information about individual assets. Depending on the available data, the asset information may include:

- name and identifier;
- dimensions and position;
- functional description;
- operating state;
- relationships with other components.

The workflow supports two interaction modes:

- **Desktop mode:** interaction through a mouse and keyboard.
- **Immersive mode:** interaction through a VR headset and motion controllers.

In immersive mode, a ray-casting mechanism acts as a virtual pointer for selecting objects and operating buttons or switches from a distance. Students can also grab and move designated virtual objects, such as boxes or workpieces. Snap zones may be used to guide object placement, improve precision, and reduce interaction errors.

The assessment of the learning task is carried out by analyzing the output of the various tasks, as defined in Table 3.

Assessment is based on the outputs produced during each learning task. The assessment strategy combines questionnaires, review of formal models, automated validation, performance comparison, observation of system behaviour, and student self-assessment.

| Task ID | Task | Expected output and assessment method |
|:--------|:-----|:--------------------------------------|
| T1.1 | Identify assets in the manufacturing system | Completed questionnaire or asset inventory. The response is assessed for the correct identification and classification of relevant assets. |
| T1.2 | Characterise existing assets | Completed asset-description template or questionnaire. The response is assessed for the correct identification of asset properties, functions, and relationships. |
| T1.3 | Analyse the existing manufacturing system | System-layout diagram, UML statecharts, and performance results. The models are assessed for logical correctness and consistency with the observed system behaviour. |
| T2.1 | Define the process plan | A process plan represented as a diagram, JSON document, ontology, or equivalent structured model. The plan is checked for the presence and correct sequence of the required operations. |
| T2.2 | Design asset behaviour | UML statecharts representing sensor and actuator behaviour. The statecharts are assessed for logical correctness, completeness, and consistency with the system requirements. |
| T2.3 | Design the integrated system | A formal system configuration, represented as an ontology, JSON document, diagram, or equivalent model. The configuration is assessed for logical consistency, component compatibility, and alignment with the production goals. |
| T2.4 | Assess system performance | A set of calculated performance indicators and a short interpretation of the results. The indicators can be compared with reference values or design requirements. |
| T2.5 | Perform virtual commissioning | An executable virtual scenario, recorded animation, video, or test report demonstrating the behaviour of the system and its MQTT-based control. |
| T2.6 | Conduct final testing and revisions | A final report documenting the tests, identified problems, corrective actions, revised solution, and student confidence assessment. |

*Table 3. Expected outputs and assessment methods for the learning tasks.*


