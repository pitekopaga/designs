# 🏗️ Software Architecture \& Design Portfolio

Welcome to my architecture portfolio. This repository contains a curated collection of software design artifacts that demonstrate my approach to system design, requirements analysis, and architectural decision-making. Each project showcases different aspects of the software development lifecycle, from initial user research through deployment architecture.

## 📋 Repository Structure

designs/

├── good2go-persona/ # User personas for Good To Go! tolling system
├── elss/ # Environmental Landscape Scanner & Simulator
├── camino-diagram/ # Complete architecture for Camino grocery inventory system
└── README.md # You are here

### 🚗 Good To Go! - Tolling System Personas \[View](/good2go-persona)
Problem: Design a modern tolling system that serves diverse user needs across Washington State.
Artifacts:

\- Alex Johnson - Non-resident business traveler needing quick, reimbursable payments
\- David Rodriguez - Fleet manager requiring multi-vehicle cost allocation
\- Maya Chen - Daily commuter seeking automated HOV scheduling


### 🌱 ELSS - Environmental Landscape Scanner & Simulator [View](/elss)
Problem: Enable real estate agents and small-scale farmers to analyze terrain, water drainage, and seasonal sun exposure without hiring expensive surveyors or consultants.
Artifacts:

\- User Personas: Real estate agent and small-scale farmer with SPICIER scenarios
\- Use Case Diagram: End user interactions and cloud processing service integration
\- Domain Diagram: Core entities including User, Scan, 3D Model, Overlay, and Modification
\- Activity Diagram: End-to-end workflow from video upload to overlay generation
\- Requirements: 22 functional and 13 non-functional requirements
\- Threat Analysis: DFD with trust boundaries and STRIDE-based threat table
  

### 🛒 Camino - Grocery Inventory Management System \[View](/camino-diagram)
Problem: Design an inventory system for a regional grocery chain that needs real-time tracking, supplier coordination, and predictive analytics.
Artifacts:

1\. Domain Models (Logical View)

Two iterations showing the evolution from comprehensive noun extraction to refined, methodology-compliant domain models

\- Domain Logical View 1 - Complete noun extraction from user scenarios
\- Domain Logical View 2 - Refined model following Rosenberg's guidelines (8 core entities)

2\. Use Case Diagram

Maps all system interactions across four actor roles

\- Floor Employees (daily operations)
\- Store Managers (decision-making)
\- HQ Analysts (strategic planning)
\- Suppliers (external integration)

3\. Activity Diagram (Process View)
\*End-to-end workflow showing Caroline's daily routine from login to supplier coordination\*

4\. Deployment Architecture (Physical View)
Five flows showing the hybrid cloud-edge deployment strategy

\- Flow 1: Dashboard Access
\- Flow 2: Sales Processing
\- Flow 3: Real-time Inventory Tracking
\- Flow 4: Order Management \& Supplier Coordination
\- Flow 5: Customer Personalization

