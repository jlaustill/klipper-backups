# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a Klipper configuration backup repository for a **Voron 2.4r2** 3D printer (serial V2.3126), managed by [Klipper-Backup](https://github.com/Staubgeborener/klipper-backup). Backups are created automatically on boot.

## Printer Architecture

- **Controller**: Octopus Pro with native CAN bus
- **Toolhead**: EBB42 (CAN-connected)
- **Bed Probe**: BTT Eddy Duo v1.0 (CAN) - used for bed mesh ONLY
- **Z Endstop**: Klicky with Omron D2F-01F - used for Z height ONLY

### Critical Design Principle

Eddy handles bed mesh shape detection. Klicky handles Z=0 reference. These roles must never be mixed.

## File Types

- `*.cfg` - Klipper configuration files
- `*.txt` - Setup notes and documentation

## Sensitive Files (gitignored)

- `.env`, `secrets.conf` - credentials
- `printer-*_*.cfg` - timestamped config backups
- `*.bak`, `*.bkp` - backup files
