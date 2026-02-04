# V2.3126 Wiring Reference

## LGX Lite Pancake Motor to EBB42

The Bondtech LGX Lite V2 uses a NEMA14 round 20mm pancake stepper with a JST-XH 4-pin connector.

### Coil Pairs

| Coil | Wire Colors |
|------|-------------|
| A (Coil 1) | Green, Red |
| B (Coil 2) | Yellow, Blue |

### EBB42 Motor Connector Pinout

Pins left to right when viewing the connector on the board:

```
┌────┬────┬────┬────┐
│ B2 │ B1 │ A1 │ A2 │
│ B- │ B+ │ A+ │ A- │
└────┴────┴────┴────┘
```

### Wire to Pin Mapping

| EBB42 Pin | Coil | LGX Lite Wire |
|-----------|------|---------------|
| 1 (B2/B-) | B- | Blue |
| 2 (B1/B+) | B+ | Yellow |
| 3 (A1/A+) | A+ | Green |
| 4 (A2/A-) | A- | Red |

### Verification

**Before powering on**, use a multimeter in continuity/resistance mode:
- Green and Red should show continuity (same coil)
- Yellow and Blue should show continuity (same coil)
- Green/Red to Yellow/Blue should show no continuity (different coils)

### Troubleshooting

| Symptom | Solution |
|---------|----------|
| Motor runs backwards | Swap wires within ONE coil pair (e.g., Green↔Red), or add `!` to `dir_pin` in Klipper |
| Motor vibrates but doesn't turn | Coil pairs are split - verify continuity and re-pair |
| Motor skips/grinds | Check that center two wires (pins 2-3) are correct coil pairs |

### Klipper Configuration

```ini
[extruder]
step_pin: EBBCan:PD0
dir_pin: EBBCan:PD1        # Add ! prefix if direction is reversed
enable_pin: !EBBCan:PD2
rotation_distance: 5.7      # LGX Lite V2 value
microsteps: 16
full_steps_per_rotation: 200

[tmc2209 extruder]
uart_pin: EBBCan:PA15
run_current: 0.65           # Bondtech recommends 0.55-0.65A
stealthchop_threshold: 999999
```

### References

- [BTT EBB42 Documentation](https://github.com/bigtreetech/docs/blob/master/docs/EBB%2042%20CAN.md)
- [Bondtech LGX Lite Quick Start Guide](https://www.bondtech.se/product/lgx-lite-large-gears-extruder/)
