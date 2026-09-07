# Warehouse Flow

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

This flow shows the dependency between warehouse readiness and transportation departure. Delays in picking, staging or door availability directly affect freight-order execution and customer delivery performance.
