# MeshHub Repository Instructions

## Project

MeshHub is a modular, solar-powered outdoor platform intended to operate two independent LoRa radio modules.

The initial target configuration uses:

- Seeed Studio XIAO nRF52840
- Wio-SX1262 radio modules
- Official MeshCore firmware on one module
- Official Meshtastic firmware on the other module

## Roles

The project owner and system architect approve all architectural and electrical decisions.

Codex acts as the implementation assistant.

Codex must not independently change the project architecture, electrical strategy, supported radio modules, firmware strategy, battery configuration, solar configuration, enclosure strategy, or connector philosophy.

## Working Rules

1. Do not create or modify files unless explicitly instructed.
2. Do not make unapproved architecture decisions.
3. Do not invent technical specifications.
4. Use complete files rather than partial snippets when creating project documents.
5. Base technical claims on primary sources such as official datasheets, schematics, standards, or manufacturer documentation.
6. Record important approved engineering decisions in docs/decisions/.
7. Keep editable source files separate from generated manufacturing outputs.
8. Do not commit, push, merge, tag, or create releases unless explicitly instructed.
9. Before modifying existing files, inspect the current contents.
10. After changes, report all modified and created files and show git status.

## Locked High-Level Decisions

- MeshHub is a modular outdoor power and enclosure platform.
- Revision A supports two independent radio modules.
- The initial radio platform is Seeed XIAO nRF52840 with Wio-SX1262.
- The radio modules use official, unmodified firmware.
- One module may run MeshCore and the other Meshtastic.
- The two radio systems remain electrically and logically independent.
- Both radios share the solar, battery, enclosure, and supporting power infrastructure.
- Two external antennas are used.
- Radio modules must remain replaceable.
- No custom radio firmware is planned for Revision A.
- Reliability takes priority over optional features.
- The design must support unattended outdoor operation.
- Architecture changes require explicit approval.

## Current Status

The project is in the requirements, research, and architecture-definition phase.

Do not create schematic or PCB design content until component selection and electrical requirements have been approved.
