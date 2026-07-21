# MH-001 — System Requirements Specification

- Document ID: MH-001
- Version: 0.1
- Status: Draft
- Project: MeshHub
- Date: 2026-07-21
- Author: Jaco Le Roux

## Revision History

| Version | Date | Description |
|---|---|---|
| 0.1 | 2026-07-21 | Initial document framework |

## 1. Purpose

This document defines the system-level requirements for MeshHub Revision A.

MeshHub is a modular, solar-powered outdoor platform designed to power and support two independent communication modules while sharing a common solar power system, rechargeable battery system, enclosure, and supporting power infrastructure.

This specification defines what the system shall achieve. It does not define the detailed electrical design, component selection, PCB layout, enclosure design, or manufacturing implementation.

---

## 2. Scope

MeshHub Revision A includes:

- Shared solar power input
- Rechargeable battery system
- Battery charging
- Battery protection
- Regulated power distribution
- Two independently powered communication modules
- Two independent external antenna connections
- Outdoor enclosure
- Replaceable communication modules
- Documentation required for assembly, testing and operation

The initial target configuration supports:

- Communication Module 1 using official MeshCore firmware
- Communication Module 2 using official Meshtastic firmware

Both communication modules are initially based on the Seeed Studio XIAO nRF52840 together with the Wio SX1262 radio module.

Revision A does not include:

- Custom MeshCore firmware
- Custom Meshtastic firmware
- Custom LoRa radio hardware
- Cloud services
- Mobile applications
- Remote firmware updating
- Advanced telemetry unless approved in a future revision

---

## 3. Definitions and Abbreviations

| Term | Definition |
|------|------------|
| MeshHub | The complete modular solar-powered platform. |
| Revision A | First hardware release of MeshHub. |
| Communication Module | Replaceable processing and radio module powered by MeshHub. |
| CM1 | Communication Module 1. |
| CM2 | Communication Module 2. |
| MeshCore | Official MeshCore firmware. |
| Meshtastic | Official Meshtastic firmware. |
| LoRa | Long Range radio technology. |
| XIAO nRF52840 | Seeed Studio MCU module used in the initial design. |
| Wio SX1262 | Seeed Studio LoRa radio module used in the initial design. |
| Official firmware | Firmware released by the original project without modification. |
| Unattended operation | Continuous operation without routine local user intervention. |

---

## 4. System Overview

MeshHub Revision A is a shared power and mechanical platform for two independent communication modules.

The platform receives energy from an external solar panel, stores energy in a rechargeable battery system, and distributes regulated power independently to Communication Module 1 (CM1) and Communication Module 2 (CM2).

The communication modules shall remain logically independent. A failure, reboot, firmware issue, or replacement of one communication module shall not require the other communication module to be reconfigured or replaced.

The communication modules share:

- Solar generation
- Battery storage
- Charging system
- Battery protection
- Mechanical enclosure
- Internal power distribution

The communication modules do not share:

- Firmware
- LoRa network configuration
- RF signal paths
- External antennas

## 5. Functional Requirements

### FR-001 Solar Power

The system shall accept power from an external photovoltaic solar panel suitable for charging the installed battery system.

### FR-002 Energy Storage

The system shall operate from a rechargeable battery system capable of supporting unattended operation.

### FR-003 Battery Charging

The system shall safely charge the installed battery system from the solar input.

### FR-004 Battery Protection

The system shall protect the battery against unsafe operating conditions.

### FR-005 Regulated Power

The system shall provide regulated power suitable for the supported communication modules.

### FR-006 Independent Communication Modules

The system shall support two independently powered communication modules.

### FR-007 Replaceable Modules

Each communication module shall be replaceable without requiring modification of the MeshHub Core hardware.

### FR-008 Independent Operation

Operation, reboot, firmware failure, or replacement of one communication module shall not require the other communication module to be restarted or reconfigured.

### FR-009 External Antennas

Each communication module shall have an independent external antenna connection.

### FR-010 Outdoor Installation

The system shall be suitable for permanent outdoor installation when assembled in the approved enclosure.

### FR-011 Documentation

The project shall include sufficient documentation to allow a third party to assemble, configure and test the hardware.

### FR-012 Official Firmware

Revision A shall support official, unmodified firmware for the supported communication modules.

## 6. Non-Functional Requirements

### NFR-001 Reliability

The system shall be designed for reliable unattended outdoor operation.

### NFR-002 Maintainability

The system shall be designed so that replaceable components can be serviced without replacing the entire platform.

### NFR-003 Modularity

The platform shall support independent replacement of communication modules.

### NFR-004 Documentation

The project shall include sufficient documentation to reproduce the hardware.

### NFR-005 Open Hardware

The project shall be developed using publicly available tools, components where practical, and openly published design documentation.

### NFR-006 Safety

The design shall prioritize safe battery charging, storage and operation.

### NFR-007 Scalability

The architecture shall allow future hardware revisions without fundamentally changing the core design philosophy.

### NFR-008 Simplicity

The design shall favor simplicity, reliability and serviceability over unnecessary features.

### NFR-009 Standard Firmware

The platform shall support official upstream firmware wherever practical rather than maintaining custom firmware.

### NFR-010 Long Service Life

The platform shall be designed for continuous outdoor operation over multiple years with normal maintenance.

## 7. Constraints

### CON-001

Revision A shall use official, unmodified MeshCore firmware.

### CON-002

Revision A shall use official, unmodified Meshtastic firmware.

### CON-003

Revision A shall not require modification of the supported communication modules.

### CON-004

The communication modules shall remain independently replaceable.

### CON-005

The design shall use commercially available components wherever practical.

### CON-006

The project shall be developed using KiCad as the primary ECAD tool.

### CON-007

The project shall maintain complete engineering documentation within the repository.

### CON-008

Architecture changes require explicit approval before implementation.

## 8. Assumptions

### ASM-001

A suitable solar installation location is available.

### ASM-002

The installed solar panel is correctly sized for the selected battery configuration.

### ASM-003

Supported communication modules continue to be commercially available or suitable replacements become available.

### ASM-004

Official MeshCore and Meshtastic firmware continue to support the selected communication modules.

### ASM-005

The enclosure is installed according to the published assembly instructions.

### ASM-006

Routine maintenance such as battery replacement may be required during the operational life of the system.

### ASM-007

Future hardware revisions will maintain the overall modular design philosophy where practical.

## 9. Acceptance Criteria

The MeshHub Core Revision A design shall be considered complete when:

### AC-001

The system can safely operate from solar power and the supported battery system.

### AC-002

The system can independently power two supported communication modules.

### AC-003

Each communication module can be installed and replaced independently.

### AC-004

The design documentation is sufficient for a third party to reproduce the hardware.

### AC-005

The assembled hardware successfully completes bench testing.

### AC-006

The assembled hardware successfully completes field testing.

## 10. Open Questions

### OQ-001

Final battery chemistry and capacity selection.

### OQ-002

Final solar panel size and mounting options.

### OQ-003

Final enclosure design and environmental sealing.

### OQ-004

Selection of the primary power management integrated circuits.

### OQ-005

Selection of external connectors and service interfaces.

### OQ-006

Verification testing required before production release.
