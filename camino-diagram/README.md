# 🛒 Camino - Grocery Inventory Management System Architecture

This directory contains the complete architectural design for Camino, a regional grocery chain's inventory management system. The artifacts follow Kruchten's 4+1 architectural view model and demonstrate full-stack architectural thinking from requirements through deployment.

## 🏛️ Architectural Views

### 1. Logical View - Domain Models

| Artifact | Description |
|----------|-------------|
| [Domain Logical View 1](./domain-logical-view1.png) | Initial comprehensive noun extraction from user scenarios. Captures every concept mentioned including personalized recommendations, seasonal trends, and specific products. |
| [Domain Logical View 2](./domain-logical-view2.png) | Refined model following Rosenberg's guidelines. Reduced to 8 core entities with proper aggregation relationships. |

**Key Decisions**:
- Composition (filled diamond) for Location→Inventory (inventory can't exist without store)
- Aggregation (open diamond) for Inventory→Product (products exist independently)
- Excluded GUI elements (per Rosenberg's guidelines)

---

### 2. Use Case View - System Scope

| Artifact | Description |
|----------|-------------|
| [Use Case Diagram](./use-case.png) | Maps interactions across four actor roles with «extends» and «includes» relationships. |

**Actors**:
- **Floor Employee** - Daily operations (track movements, flag issues)
- **Store Manager** - Central decision-maker (rebalance inventory, coordinate suppliers)
- **HQ Analyst** - Strategic planning (demand forecasting, sourcing opportunities)
- **Supplier** - External partner (update availability, confirm deliveries)

---

### 3. Process View - Dynamic Behavior

| Artifact | Description |
|----------|-------------|
| [Activity Diagram](./activity-process-view.png) | End-to-end workflow following Store Manager Caroline through her daily routine, including decision points for low stock, replenishment methods, and supplier coordination. |

**Process Flows**:
- Morning login and dashboard review
- Low stock identification and replenishment
- Sales data analysis and forecasting
- Supplier communication

---

### 4. Physical View - Deployment Architecture

| Artifact | Description |
|----------|-------------|
| [Deployment Diagram](./block-deployment-view.png) | Hybrid cloud-edge architecture showing five parallel flows through the system. |

**Flows**:
1. **Dashboard Access** - Workstation → Load Balancer → Auth Service → Inventory Service
2. **Sales Processing** - POS → Load Balancer → App Server → Sales DB / Analytics DB
3. **Real-time Inventory** - Barcode Scanner → Edge Server → API Gateway → Inventory Service
4. **Order Management** - Workstation → Load Balancer → API Gateway → Inventory Service → Supplier APIs
5. **Personalization** - POS → Load Balancer → App Server → Analytics → Customer DB

**Design Rationale**: Hybrid cloud-edge architecture chosen for:
- **Resilience**: Store operations continue during internet outages
- **Performance**: Sub-second latency for critical in-store operations
- **Maintainability**: Centralized cloud updates with local edge execution
- **Cost**: Reduced bandwidth vs pure cloud; lower hardware costs vs fully on-premise

---

## 🧠 Architectural Decisions Summary

| Decision | Rationale |
|----------|-----------|
| 8-core domain model | Balance completeness with clarity; focus on essential concepts |
| Hybrid cloud-edge deployment | Optimize for resilience, performance, and cost |
| Proper UML notation | Methodological rigor per Rosenberg and Kruchten |
| Excluded GUI from domain | Keep model focused on business concepts, not implementation |
| Explicit forecast-supplier relationship | Capture real business process from scenario |