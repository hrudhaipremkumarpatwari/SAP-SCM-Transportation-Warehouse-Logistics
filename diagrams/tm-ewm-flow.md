# SAP TM–EWM Operational Flow

```mermaid
flowchart LR
    A[ERP / Demand & Delivery Data] --> B[SAP TM Planning]
    B --> C[Freight Units / Freight Orders]
    C --> D[Planned Departure & Capacity]
    D --> E[SAP EWM Wave / Picking]
    E --> F[Staging & Packing]
    F --> G[Door Assignment & Loading]
    G --> H[Goods Issue / Dispatch]
    H --> I[Transit & Delivery]
    I --> J[KPI / Exception Review]
    J --> B
```

The key integration principle is that transportation planning should drive realistic warehouse cut-off, staging and loading timing, while warehouse execution status confirms whether the planned shipment is actually ready to depart.
