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

## Unity

**Unity** is the main development tool used for the Gearbox learning application. It is a real-time development environment for creating interactive 3D experiences, and was used here to bring together the virtual gearbox, the workshop environment and the learning activities in a single XR application. The final application is designed to run on Meta Quest headsets, allowing learners to work with the virtual product in an immersive environment.

The workshop, gearbox and tools are organised in Unity scenes and reusable objects. The gearbox components were imported as separate parts so that learners can inspect them, pick them up, move them and place them in the appropriate assembly positions. This makes it possible to reproduce the spatial relationships between the parts and to practise the assembly and disassembly procedures rather than simply viewing a completed model.

Unity was also used to implement the application's interaction and learning features. These include controller and hand-based interaction, object movement, snapping parts into place, mechanical animations, menus, instructions, audio and visual feedback. Custom scripts connect these elements and manage the progression through the different activities, from introductory interaction and information scenes to guided practice and performance-oriented tasks.

The application uses Unity to provide feedback during the exercises. It can count correctly placed pieces, record actions or mistakes, measure the time taken to complete an activity and present the results at the end. Unity's interface, animation, physics and audio features therefore support both the presentation of the learning content and the practical interaction with the [planetary gearbox](./UseCases/U01_gearbox.md#planetary-gearbox-for-a-mobile-crane-winch).

## Meta XR SDK

The **Meta XR SDK** is the software toolkit used to connect the Unity application with Meta Quest headsets. It provides the basic XR features needed for the Gearbox learning experience, including headset tracking, controller input and support for hand-based interaction. Using the SDK allowed the application to be experienced directly in the headset rather than as a conventional desktop 3D scene.

The SDK was used to configure the virtual hands and Meta Quest controllers that learners use to interact with the gearbox and the workshop tools. It provides the interaction components for pointing at, grabbing and releasing objects, as well as hand poses and snap-based interactions. These features make it possible for learners to handle individual gearbox parts and place them in the correct positions during assembly and disassembly.

The Meta XR SDK also supports other aspects of the immersive experience, such as spatial audio and haptic feedback. Together with Unity's scenes and application scripts, it helps translate the learner's movements into meaningful actions and provides immediate feedback during the exercises. The SDK therefore forms the connection between the Meta Quest hardware and the interactive learning content developed in Unity.

## Blender

**Blender** is a 3D content-creation tool used in the asset-production stage of the Gearbox application. It was used to create and prepare much of the three-dimensional content required for the virtual workshop, including the gearbox, its individual components, tools, furniture and other accessories. These assets provide the visual representation of the product and the environment in which the learning activities take place.

The gearbox was prepared as a collection of separate parts rather than as a single model. This organisation is important for the learning experience because Unity can use the individual components as interactive objects. Learners can therefore handle the parts independently and observe how they fit together during the assembly and disassembly exercises. Blender files are also present for gearbox animations and for the models used to populate the workshop.

Blender was also used to prepare animations and to make the models suitable for use in the application. The resulting models and animations were exported in formats that Unity can import, and were then brought into the Unity project. In Unity, they were assigned materials, interactive behaviours and positions within the learning scenes. Blender thus supported the creation and preparation of the visual content, while Unity brought that content together with the XR interaction and educational logic.

This workflow separates the production of the 3D assets from the development of the application itself. Changes to the geometry, appearance or animation of a component can be prepared in Blender and then updated in Unity, where the asset can be tested as part of the complete learning activity. The [project's repository](https://github.com/xrlearning/repo/tree/main) contains the Blender source files and the converted assets used by the Unity project.

## Autodesk Inventor

**Autodesk Inventor** is the Computer-Aided Design (CAD) tool used to prepare the models for the planetary gearbox Use Case. It was used to represent the [gearbox](./UseCases/U01_gearbox.md#main-components-and-design-features) as a mechanical assembly made up of individual parts, such as gears, shafts and other components. This provided an accurate digital representation of the product before it was adapted for the immersive learning application.

The assembly structure prepared in Inventor helped define how the components relate to one another and how they fit together. The separate parts could then be used to illustrate the construction of the planetary gearbox and to support the assembly and disassembly activities. This was particularly useful for creating a learning experience in which students can understand both the appearance of the components and their position within the complete mechanism.

The Inventor models were subsequently prepared for use in the rest of the asset-production workflow. After conversion and export, the geometry could be further adapted in Blender and imported into Unity, where it was combined with materials, animations and interactive behaviours. Autodesk Inventor therefore provided the mechanical design basis for the planetary gearbox, while Blender and Unity supported its preparation and use in the XR learning environment.
