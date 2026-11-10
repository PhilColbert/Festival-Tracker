# Festival Tracker — Project Specification

**Document version:** 0.1  
**Status:** Initial recovered specification  
**Last updated:** 2026-11-10  
**Authority:** This file records requirements supported by the available project conversation. It is not a completed engineering design.

Status labels:
- **FIXED** — explicitly approved or clearly established.
- **PROPOSED** — a candidate direction that still needs approval.
- **UNRESOLVED** — insufficient information; do not assume.

## 1. Project objective

Build a festival-oriented, phone-led tracking and communication system. Portable tracker devices are intended to communicate locally over LoRa, with phones providing the main user interface.

## 2. User experience and phone connection

| ID | Requirement | Status |
|---|---|---|
| UX-001 | Phones are the primary user interface. | FIXED |
| UX-002 | Remove the OLED display from the hardware design. | FIXED |
| UX-003 | A phone communicates with a tracker using Bluetooth Low Energy (BLE). | PROPOSED |
| UX-004 | Phone interface provides configuration and user-facing information. | PROPOSED |
| UX-005 | Supported mobile platforms and minimum OS versions. | UNRESOLVED |

The OLED removal is an approved scope decision. Do not reintroduce an OLED without a new approved change request.

## 3. Radio and networking

| ID | Requirement | Status |
|---|---|---|
| NET-001 | LoRa is used for local/off-grid communication. | FIXED (project direction) |
| NET-002 | Devices form a mesh or relaying network. | PROPOSED |
| NET-003 | Messages and location information can be relayed between devices. | PROPOSED |
| NET-004 | Operation must not depend on internet availability for local radio communication. | PROPOSED |
| NET-005 | Cloud synchronisation when internet connectivity is available. | PROPOSED |
| NET-006 | Radio band, region, channel plan, data rate, airtime and legal duty-cycle limits. | UNRESOLVED |
| NET-007 | Mesh routing, addressing, acknowledgements, retries, duplicate suppression and congestion handling. | UNRESOLVED |

No specific LoRa chipset or module is confirmed by the authoritative project records available in this conversation. Do not treat any previous conversational component suggestion as a frozen bill of materials.

## 4. Location

| ID | Requirement | Status |
|---|---|---|
| LOC-001 | Location is part of the intended tracker experience. | PROPOSED |
| LOC-002 | Phone GPS may provide location to the tracker/application. | PROPOSED |
| LOC-003 | Whether the tracker contains its own GNSS receiver. | UNRESOLVED |
| LOC-004 | Location update interval, accuracy, retention and sharing permissions. | UNRESOLVED |

## 5. Safety and messaging

| ID | Requirement | Status |
|---|---|---|
| SAFE-001 | SOS/emergency messaging is a required project feature. | FIXED (feature requirement) |
| SAFE-002 | SOS traffic receives priority. | PROPOSED |
| SAFE-003 | Delivery acknowledgement, retry, cancellation and escalation behaviour. | UNRESOLVED |
| SAFE-004 | User identity, trusted contacts and emergency workflow. | UNRESOLVED |

The system must not be represented as a guaranteed emergency service. Radio coverage, battery state, network density and device availability can affect delivery.

## 6. Power and physical design

| ID | Requirement | Status |
|---|---|---|
| HW-001 | OLED display is excluded. | FIXED |
| HW-002 | USB-C charging/power connection. | PROPOSED |
| HW-003 | Battery chemistry, capacity, runtime and charging circuit. | UNRESOLVED |
| HW-004 | Enclosure dimensions, ingress protection, mounting and environmental limits. | UNRESOLVED |
| HW-005 | Physical control/button requirements. | UNRESOLVED |

## 7. Hardware and firmware

Exact MCU, LoRa transceiver/module, antenna, sensors, power architecture, pinout, PCB stack-up and firmware framework are **UNRESOLVED** pending confirmation against the intended design. Any candidate parts are to be recorded in a reviewed BOM before implementation.

## 8. App and data

App architecture, phone-to-phone behaviour, backend/cloud provider, accounts, data model, encryption, privacy controls, offline storage and synchronisation conflict handling are **UNRESOLVED**.

## 9. Security and privacy

Security and privacy are project requirements. The specific protocol, key provisioning, authentication, encryption at rest/in transit, lost-device handling, data minimisation, retention and consent flows are **UNRESOLVED** and require explicit design.

## 10. Acceptance and verification

No implementation or verification is claimed by this document. Future changes must record separately whether a feature was:
- inspected,
- automated-tested,
- compiled,
- device-tested,
- or remains unverified.

Acceptance criteria and test hardware are **UNRESOLVED**.

## 11. Change-control rules

1. Every edit requires a logged Change ID, request, baseline and scope before editing.
2. Make only approved changes.
3. Record files changed, preserved functionality, checks/results, issues and version after each change.
4. Unchanged files must be carried forward byte-for-byte and identified as such; do not claim they were rebuilt or tested.
5. Do not claim screenshots, builds, device tests or saves that were not performed.
6. No release with unresolved regressions.
7. Update this specification, change register, manifest and version history together when affected.
