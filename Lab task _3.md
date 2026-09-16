# Mars Rover Mission Control - Requirements Analysis & Change Management

## 1. Requirement analysis (From Engineering Notes)

### Functional Requirements (FRs)

**FR-01:** The rover shall receive and execute valid commands sent from Mission Control.

**FR-02:** The rover shall report its telemetry data, including current position, battery level, temperature, and communication status.

**FR-03:** The system shall reject any invalid or unauthorized commands.

**FR-04:** The rover shall automatically enter Safe Mode upon detecting a critical battery or thermal condition.

**FR-05:** The system shall send command execution status updates back to Mission Control.

**FR-06:** The system shall record all commands and critical events with timestamps and operator IDs for audit logs.

### Non-Functional Requirements (NFRs)

**NFR-01 (Performance):** Command processing shall complete within 5 seconds after a command is received by the rover.

**NFR-02 (Security):** Only authenticated Mission Control operators shall be permitted to issue rover commands.

**NFR-03 (Reliability / Fault Tolerance):** The system shall continue operating despite temporary communication interruptions.

**NFR-04 (Scalability):** The system shall support communication with multiple rovers simultaneously.

---

## 2. Updated Requirements (After Change Requests)

### Change Request CR-01 — Emergency Safety

**Original Requirement (FR-04):** The rover shall enter Safe Mode when a critical battery or thermal condition is detected.

**Updated Requirement (FR-04):** The rover shall enter Safe Mode within 3 seconds when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level.

**Impact:** Adds specific quantitative triggers including a 3-second time frame and explicit thermal or battery thresholds, transforming part of the behavior into a strict safety-critical response time constraint.

### Change Request CR-02 — Mission Expansion

**Original Requirement (NFR-04):** The system shall support communication with multiple rovers simultaneously.

**Updated Requirement (NFR-04):** The system shall support at least 20 simultaneously connected rovers.

**Impact:** Converts a vague non-functional requirement into a measurable and testable capacity and scalability metric.

### Change Request CR-03 — Security Upgrade

**Original Requirement (NFR-02):** Only authenticated Mission Control operators shall be permitted to issue rover commands.

**Updated Requirement (NFR-02):** The system shall require authenticated and role-authorized operators before accepting rover commands.

**Impact:** Enhances security from basic identity verification (authentication) to fine-grained access control through Role-Based Access Control (RBAC).
