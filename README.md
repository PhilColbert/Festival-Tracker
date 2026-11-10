# Festival Tracker

**Project:** Festival Tracker  
**Repository:** https://github.com/PhilColbert/Festival-Tracker  
**Document baseline:** 0.1  
**Record date:** 2026-11-10

## Purpose
A phone-led festival communication and safety system using portable tracker devices and a LoRa mesh. Phones are the primary user interface; tracker hardware provides local radio communication and associated device functions.

## Current approved direction
- OLED display: **removed**. The design is intended to be used primarily through phones.
- Phone interface: primary user interface.
- Bluetooth Low Energy (BLE): intended phone-to-tracker link.
- LoRa: intended off-grid, local mesh communications.
- SOS / emergency messaging: project requirement; detailed behaviour remains to be specified.

## Important status notice
This repository is the master project record. Read `SPECIFICATION.md`, `CHANGE_REGISTER.md`, `MANIFEST.md`, and `VERSION_HISTORY.md` before making changes.

Items labelled **PROPOSED** are not approved implementation decisions. Items labelled **UNRESOLVED** must not be guessed. No firmware, PCB, app, or device test results are claimed by this initial documentation commit.
