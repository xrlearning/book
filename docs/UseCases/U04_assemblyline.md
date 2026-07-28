---
title: Assembly Line
layout: default
nav_order: 4
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


# Assembly Line
{:.no_toc}

## Description

This use case consists in an assembly line that produces self-closing concealed cabinet hinges. The assembly line includes 19 workstations, each performing specific tasks (e.g., pick and place, screw tightening, riveting) to assemble the components of the self-closing concealed cabinet hinge. These components are shown in Figure 1 and listed in Table 1. The sequence of operations is detailed in Table 2, indicating the input components and the workstation responsible for each operation. Work-in-progress hinges are moved along the line on a pallet.

<img src="U04_media/image6.png" style="width:3.0973in;height:2.68929in" />

Figure 1: Hinge components

| **Component ID** | **Label** |
|------------------|-----------|
| Wing             | 1         |
| WingScrew        | 2         |
| Clip             | 3         |
| Pin1-1           | 4         |
| Connector1       | 5         |
| Spring           | 6         |
| Pin1-2           | 7         |
| Connector2       | 8         |
| Pin1-3           | 9         |
| Box              | 10        |
| Hook             | 11        |

Table 1: Hinge components with label

| **Operation ID** | **Operation type** | **Input Component** | **Station ID** | **Description**                                                                            |
|------------------|--------------------|---------------------|----------------|--------------------------------------------------------------------------------------------|
| 1                | pick&place         | Wing                | PPW1           | Wing is picked from the upstream buffer and placed on the rotating table.                  |
| 2                | tightening         | WingScrew           | T1             | WingScrew is aligned to the corresponding hole on the Wing and screwed.                    |
| 3                | pick&place         |                     | PPH1           | The wip hinge is taken from the rotating table and placed on a conveyor.                   |
| 4                | pick&place         |                     | RPP1           | A robot of workstation RPP1 picks the wip hinge from a conveyor and places it on a pallet. |
| 5                | pick&place         | Clip                | PP1            | Clip is assembled on Wing, hooking to the WingScrew.                                       |
| 6                | pin insertion      | Pin1-1              | PI1            | Pin1-1 is inserted to fix Clip on Wing.                                                    |
| 7                | riveting           |                     | R1             | Pin1-1 is riveted.                                                                         |
| 8                | pick&place         | Connector1          | PP2            | Connector1 is assembled on Wing.                                                           |
| 9                | pick&place         | Spring              | PP3            | Spring is assembled on Wing.                                                               |
| 10               | pin insertion      | Pin1-2              | PI2            | Pin1-2 is inserted to fix Connector1 and Spring on Wing.                                   |
| 11               | riveting           |                     | R2             | Pin1-2 is riveted.                                                                         |
| 12               | pick&place         | Connector2          | PP4            | Connector2 is assembled on Wing.                                                           |
| 13               | pin insertion      | Pin1-3              | PI3            | Pin1-3 is inserted to fix Connector2 on Wing.                                              |
| 14               | riveting           |                     | R3             | Pin1-3 is riveted.                                                                         |
| 15               | pick&place         | Box                 | PP5            | Box is assembled on Wing.                                                                  |
| 16               | pin insertion      | Hook                | PI4            | Hook is inserted to fix Box on Wing.                                                       |
| 17               | riveting           |                     | R4             | Hook is riveted.                                                                           |
| 18               | inspection         |                     | C1             | The finished hinge is visually inspected by a camera.                                      |
| 19               | pick&place         |                     | CB1            | The finished hinge is picked from the pallet and placed in a box.                          |

Table 2: Operations and workstations


## Online resources

The [scene configuration](https://xrlearning.github.io/repo/UseCases/AssemblyLine/AssemblyLine.json) and the [3D models](https://github.com/xrlearning/repo/tree/main/UseCases/AssemblyLine/models) (Figures 2-8) of the use case are available online. The [assembly line can be visualized](https://xrlearning.github.io/repo/UseCases/AssemblyLine/AssemblyLine.html) using [VEB.js](../Tools#vebjs) tool (Figures 9 and 10).


<img src="U04_media/fig2.png" style="width:2.63125in" />

Figure 2: Hinge.

<img src="U04_media/fig3.png" style="width:2.63125in" />

Figure 3: Pallet.

<img src="U04_media/fig4.png" style="width:2.63125in" />

Figure 4: Pin insertion station.

<img src="U04_media/fig5.png" style="width:2.63125in" />

Figure 5: Riveting station.

<img src="U04_media/fig6.png" style="width:2.63125in" />

Figure 6: Inspection camera station

<img src="U04_media/fig7.png" style="width:2.63125in" />

Figure 7: UR pick and place station

<img src="U04_media/fig8.png" style="width:2.63125in" />

Figure 8: Conveyor


<img src="U04_media/fig9.png" style="width:4.5in" />

Figure 9: Assembly line (upstream part)

<img src="U04_media/fig10.png" style="width:4.5in" />

Figure 10: Assembly line (downstream part)



