# Warehouse Logistics

The Week 4 warehouse design uses SAP EWM concepts to connect inventory handling with transportation execution.

## Warehouse Structure

The fictional distribution warehouse is modeled with **4,000 pallet positions**, **6 dock doors**, and approximately **60 pallet positions of staging capacity**.

## Operational Flow

1. Receive or make stock available for outbound planning.
2. Determine storage type, bin and activity area.
3. Create warehouse tasks for picking.
4. Group tasks into waves where appropriate.
5. Pick and confirm stock.
6. Move goods to staging.
7. Pack and prepare handling units.
8. Assign the load to the appropriate door.
9. Complete loading and goods issue.
10. Reconcile warehouse and transportation status.

## Worked Examples

- Average occupancy: **78.75%**
- Peak occupancy: **92%**
- Picker-travel model: **29.76 km/day → 21.12 km/day**, about **29% reduction** after slotting improvements
- Dock turnaround: **110 minutes → 75 minutes**, about **31.8% improvement**

## Improvement Logic

Fast-moving items should be placed closer to picking and staging areas, while wave timing should be aligned with planned truck departures. High peak occupancy should trigger tighter slotting, replenishment and staging controls to avoid congestion.
