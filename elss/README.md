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

| [Use Case Diagram](https://github.com/pitekopaga/designs/blob/main/elss/use-case-diagram.png) | Shows actors (End User, Cloud Processing Service) and key system functions including Generate Drainage Overlay, Generate Sun Path Overlay, and Modify Virtual Environment |

| [Domain Diagram](https://github.com/pitekopaga/designs/blob/main/elss/domain-diagram.png) | Core domain objects (User, Scan, 3D Model, Overlay, Modification) and their relationships |

| [Activity Diagram](https://github.com/pitekopaga/designs/blob/main/elss/activity-diagram.png) | End-to-end workflow for a farmer assessing a flood-prone field, showing video validation, parallel overlay generation, and optional modification loop |

| [Data Flow Diagram](https://github.com/pitekopaga/designs/blob/main/elss/data-flow-diagram.png) | Information flow with trust boundaries, external entities (Customer, Cloud Processing Service), and threat annotations (T1–T6) |



##### \## Key Design Decisions



\- \*\*Single End User Actor\*\* – Farmers and real estate agents interact with the system identically, so they were consolidated

\- \*\*Cloud Processing Service\*\* – Added as a secondary actor to make external computation explicit

\- \*\*Overlay Terminology\*\* – Replaced "simulation" with "overlay" for accuracy

\- \*\*Threat Modeling\*\* – STRIDE analysis with T1–T6 mapped to DFD elements



##### \## Tools Used



\- Mural – Collaborative diagramming

\- Git / GitHub – Version control

