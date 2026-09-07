# SAP SCM Transportation Management & Warehouse Logistics

## Week 4 Internship Project

This repository documents a **Transportation Management and Warehouse Logistics project using SAP SCM concepts**, with emphasis on **SAP Transportation Management (TM)**, **SAP Extended Warehouse Management (EWM)**, and **SAP SCM / SNP Transport Load Builder (TLB)** principles.

The fictional **Deccan Harvest Foods Pvt. Ltd.** scenario continues from the earlier weeks and models approximately **150 tonnes of weekly finished-goods movement** from Hyderabad to markets in Telangana, Andhra Pradesh, and Karnataka.

> **Project type:** Internship planning simulation and SAP configuration blueprint. It is not presented as a live production-system implementation.

## Final Report

📄 [**Open the Week 4 Optimized Word Report**](docs/SAP_SCM_Week4_Transportation_Warehouse_Logistics_Hrudhai_Optimized.docx)

## Project Objective

The project demonstrates how transportation and warehouse activities can be synchronized to improve logistics performance through:

- freight and transportation planning
- carrier and vehicle-capacity management
- transportation-lane design
- load consolidation
- SAP TM freight-unit / freight-order concepts
- SAP EWM warehouse tasks, waves, staging and door management
- picking, packing, loading and goods issue
- ERP ↔ TM ↔ EWM information synchronization
- KPI monitoring, validation and risk controls

## Scenario

The simulation uses a central Hyderabad warehouse supporting regional movements to Telangana, Andhra Pradesh and Karnataka through road FTL, local/LTL and rail-linked options.

Warehouse assumptions include:

- **4,000 pallet positions**
- **6 dock doors**
- approximately **60 pallet positions of staging capacity**
- average occupancy of approximately **78.75%**
- peak occupancy of approximately **92%**

## Transportation Workflow

```mermaid
flowchart LR
    A[ERP / Delivery Demand] --> B[SAP TM Planning]
    B --> C[Freight Units / Freight Orders]
    C --> D[Carrier / Mode / Capacity]
    D --> E[Planned Departure]
    E --> F[SAP EWM Wave & Picking]
    F --> G[Staging / Packing]
    G --> H[Door Assignment / Loading]
    H --> I[Goods Issue & Dispatch]
    I --> J[Delivery / KPI Review]
```

Detailed notes are available in [`docs/transportation-workflow.md`](docs/transportation-workflow.md).

## Warehouse Logistics Flow

```mermaid
flowchart LR
    A[Available Stock] --> B[Warehouse Task]
    B --> C[Wave Release]
    C --> D[Picking]
    D --> E[Staging]
    E --> F[Packing / HU]
    F --> G[Door Assignment]
    G --> H[Loading]
    H --> I[Goods Issue]
    I --> J[Transportation Dispatch]
```

Detailed notes are available in [`docs/warehouse-logistics.md`](docs/warehouse-logistics.md).

## Worked Examples

### 1. Transport consolidation

A Vijayawada example compares fragmented loads with a consolidated transportation plan:

- vehicle utilization improves from approximately **70.3% to 93.75%**
- **one truck trip per week** is avoided
- illustrative freight saving: approximately **₹26,000 per week**
- annualized illustrative saving: approximately **₹13.52 lakh**

### 2. Picker-travel improvement

A slotting example reduces modeled picker travel from:

**29.76 km/day → 21.12 km/day**

This is approximately a **29% reduction**.

### 3. Dock turnaround

The modeled dock turnaround improves from:

**110 minutes → 75 minutes**

This is approximately a **31.8% improvement**.

## SAP Concepts Applied

| Area | Concepts used |
|---|---|
| Transportation Planning | freight demand, mode, carrier, capacity and routes |
| SAP TM | freight units, freight orders, planning and execution concepts |
| SAP EWM | storage types, bins, warehouse tasks, waves, staging and doors |
| Warehouse Execution | picking, packing, handling units, loading and goods issue |
| SAP SCM / SNP | Transport Load Builder concepts and shipment consolidation |
| Integration | ERP, TM and EWM synchronization concepts |
| Monitoring | vehicle fill, dock turnaround, occupancy, picking productivity and OTIF |
| Risk Management | carrier, capacity, stock, congestion, interface and demand risks |

## Key KPIs

- vehicle fill / utilization
- freight cost per tonne
- on-time dispatch
- OTIF / delivery performance
- warehouse occupancy
- picker travel and productivity
- dock turnaround time
- staging congestion
- stock accuracy
- freight and warehouse exception frequency
- interface / synchronization errors

## Risk and Contingency Planning

The project evaluates operational risks such as carrier no-show, vehicle breakdown, low load utilization, dock congestion, picking delay, inventory mismatch, master-data error, integration failure, peak occupancy and demand spikes.

See [`docs/risk-analysis.md`](docs/risk-analysis.md).

## Validation Approach

The report includes ten proposed validation tests covering:

1. route and destination accuracy
2. carrier / mode selection
3. vehicle-capacity checks
4. freight-order timing
5. wave-to-departure alignment
6. picking completion
7. staging readiness
8. door assignment
9. goods-issue synchronization
10. KPI and exception monitoring

## Repository Structure

```text
SAP-SCM-Transportation-Warehouse-Logistics/
|
|-- README.md
|-- docs/
|   |-- SAP_SCM_Week4_Transportation_Warehouse_Logistics_Hrudhai_Optimized.docx
|   |-- transportation-workflow.md
|   |-- warehouse-logistics.md
|   `-- risk-analysis.md
|
`-- diagrams/
    |-- tm-ewm-flow.md
    |-- transport-consolidation.md
    `-- warehouse-flow.md
```

## Supporting Diagrams

- [`TM–EWM Operational Flow`](diagrams/tm-ewm-flow.md)
- [`Transport Consolidation`](diagrams/transport-consolidation.md)
- [`Warehouse Flow`](diagrams/warehouse-flow.md)

## Learning Outcomes

This project strengthened my understanding of how transportation planning and warehouse execution depend on each other. A transport plan is only executable when stock, picking, staging and dock readiness are synchronized with the planned departure time.

The exercise also demonstrated how load consolidation, warehouse slotting, dock planning, KPI monitoring and exception management can improve logistics performance when supported by accurate master data and clear operational controls.

## Author

**Hrudhai Prem Kumar Patwari**  
SAP SCM / SAP MM Learner | IT Operations Professional

---

### Academic / Internship Use

This repository is a learning and internship project. Company names, quantities, capacities, freight costs, warehouse dimensions and performance results are fictional and are used only to demonstrate SAP SCM transportation and warehouse-logistics concepts.
