---
title: Tools
layout: default
nav_order: 4
has_children: true
---





{: .no_toc }
<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>



# XR Learning Tools
{:.no_toc}

This chapter presents the relevant tools supporting the execution of the XR Learning Workflows. 


## VEB.js

**VEB.js** (Virtual Environment based on Babylon.js) is a web-based VR tool for immersive visualization and interaction with virtual factory and manufacturing scenarios, directly accessible through a standard web browser. It supports XR-enabled exploration of products, processes, and systems, making it suitable for training, analysis, and collaborative engineering activities. Official resources include the online [documentation](https://virtualfactory.gitbook.io/vlft/tools/vebjs), a browser-based [demo application](https://difactory.github.io/DF/tools/VEBjs.html) showcasing core functionalities, and documented [use cases](https://difactory.github.io/repository/) illustrating how VEB.js can be applied in industrial and educational contexts within the Virtual Factory framework.

Built on top of Babylon.js, VEB.js inherits all core rendering and interaction capabilities (e.g., lighting, physics, animation, WebXR integration), while introducing a higher abstraction layer that separates interaction logic from geometric representation. Its architecture is data-driven, meaning that:
- 3D assets (e.g., robots, conveyors, sensors) are loaded from GLTF models generated via CAD and mesh editing pipelines;
- Behaviors and logic are externally defined via .json configuration files structured around semantic ontologies;
- Interactive dynamics are implemented using finite state machines (based on state- charts), which define transitions, animations, and control actions over time.

VEB.js provides other key functionalities like:
- Dynamic instantiation and hierarchical placement of scene elements based on spatial coordinates and parent-child relations;
- Declarative behavior specification, through JSON-based configuration without re- quiring hardcoded logic;
- Centralized lifecycle management for user interface elements and 3D objects;
- Support for scene re-export, enabling updates and version control via modified JSON outputs.

Babylon.js and VEB.js support WebXR that is a web standard developed and maintained by the W3C (World Wide Web Consortium). It provides APIs (Application Programming Interfaces), which are standardized sets of functions that allow developers to interact with complex system components, such as VR headsets or motion controllers, without needing to manage low- level hardware instructions. Through these APIs, WebXR enables developers to create immersive experiences directly in the browser, supporting both augmented reality (AR) and virtual reality (VR). It is compatible with a wide variety of devices, including VR headsets (e.g., Meta Quest), AR glasses, and smartphones. One of its key advantages is hardware abstraction: a single codebase can be used across different platforms, whether immersive (e.g., Head Mounted Displays) or non-immersive (desktop screens), with built-in support for spatial tracking, controller input, and environmental sensing.

## OntoGuiWeb

**OntoGuiWeb** is a web-based tool for browsing, querying, and interacting with ontologies used in virtual factory and manufacturing-related applications. It provides a user-friendly graphical interface to explore ontology structures, classes, properties, and instances directly in the browser, supporting knowledge-driven engineering, data integration, and semantic modeling activities. Official resources include the online [documentation](https://virtualfactory.gitbook.io/vlft/tools/ontoguiweb) and a a browser-based [demo application](https://difactory.github.io/DF/tools/OntoGuiWeb.html).

 The main window of OntoGuiWeb is a Control Panel that can manage (networks of) ontology modules and gives access to specific tools that are relevant for learning workflows:

- *Asset Design* for the definition and characterization of assets
- *System Design* for the design of a production system in terms of part types, process plans, process steps, production systems, system elements
- *Performance Evaluation* for the definition of production plans that are need to evaluate the performance of a production system.
- *MQTT Sync* that provides an MQTT client to publish a message on a topic and subscribe to topics
- *Virtual Environment* that enables the automatic and parametric generation of a virtual scene in [VEB.js](#vebjs) based on the content of an ontology module
- *Graphs Eng* that visualizes graphs representing parts/part types, processes and production systems.
- *StateChart* that support the design and visualization of UML StateChart modeling the behavior of assets.


## Cutset and Bourjault Application

This application has been developed using Unity and is available [online](https://github.com/xrlearning/repo/tree/main/Tools/Cutset_Bourjault).

## Gearbox Application

This application has been developed using Unity and is available [online](https://github.com/xrlearning/repo/tree/main/Tools/Gearbox).
