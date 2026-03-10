---
name: Task
about: Create a task to track work that needs to be done
title: "[Task]: "
labels: task
assignees: ''

---

## Description
Implement an improved Loss of Signal (LOS) detection mechanism using two separate timers:
1. **Heartbeat Timeout (Timer 1)**: Measures duration since last heartbeat message received. If no heartbeat for X seconds, trigger LOS.
2. **Packet Loss Threshold (Timer 2)**: Counts consecutive missed packets using sequence numbers. If missed packets exceed threshold, trigger LOS.

## Requirements
- Remove radio disconnect check dependency
- Add configurable parameters:
  - `heartbeat_timeout`: Max duration (sec) without heartbeat to trigger LOS (default: 10.0)
  - `packet_loss_threshold`: Max consecutive missed packets to trigger LOS (default: 5)
- When LOS is triggered:
  - Switch to Station mode
  - Disable Navigation, Voyage, Maneuver, DP modes
  - Allow manual override to Idle or Direct modes only
- When LOS recovers:
  - Re-enable all modes

## Affected Components
- `rkse_navigation`: `IsLossOfSignal` behavior node
- `swadheen_bringup`: `los_behavior.xml` behavior tree

## Acceptance Criteria
- [ ] LOS triggers when heartbeat timeout exceeded
- [ ] LOS triggers when packet loss threshold exceeded
- [ ] Station mode forced on LOS trigger
- [ ] Auto modes (Navigation, Voyage, Maneuver, DP) disabled during LOS
- [ ] Manual override to Idle/Direct allowed during LOS
- [ ] All modes re-enabled on LOS recovery
