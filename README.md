# MeshHub

MeshHub is a professional open-source hardware project for a modular, solar-powered outdoor platform intended to operate two independent LoRa radio modules. It is being developed with an emphasis on reliability, maintainability, and clear separation between editable engineering sources and generated manufacturing outputs.

## Current Status

MeshHub is currently in the requirements, research, and architecture-definition phase. Component selection and electrical requirements are not yet approved, and schematic, PCB, enclosure, manufacturing, and test-design work has not started.

> **Warning:** MeshHub hardware is not yet ready to build. This repository does not currently contain an approved design or complete manufacturing information.

## Initial Target Configuration

The initial target configuration is:

- Two independent Seeed Studio XIAO nRF52840 modules
- Two Wio-SX1262 radio modules
- Official MeshCore firmware on one radio system
- Official Meshtastic firmware on the other radio system
- Shared solar, battery, enclosure, and supporting power infrastructure
- Two external antennas

This target configuration records the current high-level direction and does not constitute a completed electrical or mechanical specification.

## Core Design Principles

- Keep the two radio systems electrically and logically independent.
- Use official, unmodified radio firmware for Revision A.
- Keep radio modules replaceable.
- Prioritize reliability and unattended outdoor operation.
- Maintain modularity in the power and enclosure platform.
- Separate editable source files from generated manufacturing outputs.
- Base engineering decisions on approved requirements and documented primary sources.
- Require explicit approval for architecture changes.

## Repository Layout

- `docs/` — requirements, architecture, component-selection research, decisions, assembly documentation, and user guides
- `hardware/` — KiCad project sources and templates
- `libraries/` — project-managed KiCad libraries, 3D models, and component datasheets
- `enclosure/` — editable CAD sources, exchange formats, and drawings
- `manufacturing/` — PCB, assembly, BOM, fabrication, and release outputs
- `testing/` — hardware tests, fixtures, procedures, and results
- `images/` — renders, photographs, diagrams, and documentation images

Repository working rules and approved high-level decisions are recorded in `AGENTS.md`.

## License

To be selected.
