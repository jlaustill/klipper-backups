# V2.3126 Documentation Index

Documentation collected for Voron 2.4r2 reassembly.

## Downloaded PDFs

| File | Component | Source |
|------|-----------|--------|
| `Voron_2.4r2_Assembly_Manual.pdf` (72MB) | Frame assembly | [VoronDesign GitHub](https://github.com/VoronDesign/Voron-2) |
| `BTT_Octopus_Pro_Manual.pdf` (2.8MB) | Mainboard | [BigTreeTech GitHub](https://github.com/bigtreetech/BIGTREETECH-OCTOPUS-Pro) |
| `BTT_EBB42_CAN_Manual.pdf` (232KB) | Toolhead board | [BigTreeTech/RatRig](https://github.com/bigtreetech/EBB) |
| `BTT_Eddy_Series_Manual.pdf` (2.9MB) | Bed probe | [BigTreeTech GitHub](https://github.com/bigtreetech/Eddy) |
| `BTT_Universal_Turbo_Kit_Manual.pdf` (1.2MB) | CPAP cooling | [BigTreeTech GitHub](https://github.com/bigtreetech/Universal-Turbo-Kit) |
| `BTT_Smart_Filament_Sensor_V2_Manual.pdf` (2.9MB) | Filament runout | [BigTreeTech GitHub](https://github.com/bigtreetech/smart-filament-detection-module) |
| `Bondtech_LGX_Lite_Quick_Start.pdf` (3.2MB) | Extruder setup | [Bondtech](https://www.bondtech.se/product/lgx-lite-large-gears-extruder/) |
| `Bondtech_LGX_Lite_Maintenance.pdf` (5.0MB) | Extruder maintenance | [Bondtech](https://www.bondtech.se/product/lgx-lite-large-gears-extruder/) |
| `Phaetus_Dragon_Voron_Manual.pdf` (1.6MB) | Hotend (ST/HF) | [Phaetus GitHub](https://github.com/Phaetus/Phaetus-x-VORON-Hotend-ST) |

## Klicky Probe Documentation (Markdown)

The Klicky Probe project doesn't provide PDFs. Documentation is in `Klicky_Probe/`:

- `README.md` - Voron 2.4 installation guide (mounting, BOM, assembly)
- `Klipper_Macros_README.md` - Klipper macro setup and configuration

**Source:** [jlas1/Klicky-Probe](https://github.com/jlas1/Klicky-Probe)

## Wiring Reference

Custom wiring documentation created during reassembly:

- `wiring.md` - LGX Lite pancake motor to EBB42 pin mapping, coil pairs, troubleshooting

## Online Resources

These resources are not downloaded but may be useful:

- [Klipper Eddy Probe Documentation](https://www.klipper3d.org/Eddy_Probe.html) - Official Klipper docs
- [BTT Eddy Wiki](https://bttwiki.com/Eddy.html) - Additional configuration guides
- [Voron Documentation](https://docs.vorondesign.com/) - Official Voron docs
- [GadgetAngel Octopus Pinout Diagram](https://github.com/GadgetAngel/BTT_Octopus_Color_PIN_Diagram) - Color-coded pinouts
- [Voron SFS Setup Guide](https://docs.vorondesign.com/community/howto/samwiseg0/btt_smart_filament_sensor.html) - Klipper config for filament sensor

## Reassembly Order (Suggested)

1. Frame assembly (Voron manual)
2. Electronics mounting (Octopus Pro manual)
3. CAN wiring (EBB42 manual)
4. Hotend assembly - Dragon Voron ST (Phaetus manual)
5. Extruder mounting - LGX Lite (Bondtech quick start)
6. Toolhead wiring
7. Smart Filament Sensor installation (SFS V2 manual)
8. Klicky probe installation (Klicky_Probe/)
9. Eddy probe mounting (Eddy manual)
10. Universal Turbo Kit installation (Turbo Kit manual)
11. Firmware flashing and calibration
