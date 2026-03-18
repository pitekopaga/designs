### \# Environmental Landscape Scanner \& Simulator (ELSS)



A mobile application that generates 3D terrain models and environmental overlays from video footage. Users upload video of a property, and the system produces topographic maps with visual overlays showing water drainage patterns and seasonal sun exposure.



##### \## System Overview



ELSS transforms standard smartphone video into actionable environmental insights:

\- \*\*3D Terrain Mapping\*\* – Generates topographic models from walking video

\- \*\*Drainage Overlays\*\* – Visualizes water flow paths and pooling areas

\- \*\*Sun Path Overlays\*\* – Shows shadow patterns across seasons

\- \*\*Soil Analysis\*\* – Estimates basic soil composition from visual cues

\- \*\*What-If Modifications\*\* – Add virtual trees or structures to test scenarios



##### \## Diagrams



| Diagram | Description |

|---------|-------------|

| \[Use Case Diagram](260316\_UseCaseDiagram\_Scott.png) | Shows actors (End User, Cloud Processing) and key system functions |

| \[Domain Diagram](260310\_DomainDiagramV3.png) | Core domain objects and their relationships |

| \[Activity Diagram](260310\_ActivityDiagram\_Scott.png) | End-to-end workflow for a farmer assessing a flood-prone field |

| \[Data Flow Diagram](260317\_DFD\_Scott.png) | Information flow with trust boundaries and threat annotations |



##### \## Key Design Decisions



\- \*\*Single End User Actor\*\* – Farmers and real estate agents interact with the system identically, so they were consolidated

\- \*\*Cloud Processing Service\*\* – Added as a secondary actor to make external computation explicit

\- \*\*Overlay Terminology\*\* – Replaced "simulation" with "overlay" for accuracy

\- \*\*Threat Modeling\*\* – STRIDE analysis with T1–T6 mapped to DFD elements



##### \## Tools Used



\- Mural – Collaborative diagramming

\- Git / GitHub – Version control

