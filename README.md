# Vehicle Speed And LED Control AUTOSAR

## Overview

Vehicle Speed And LED Control AUTOSAR is an AUTOSAR-based automotive software project developed using ARTOP/Eclipse. The system acquires wheel speed data, calculates vehicle speed, and controls LED indications based on the processed speed information. The project demonstrates AUTOSAR software architecture design, component communication, system mapping, and system extract generation using ARXML.

---

## Project Statement

The objective of this project is to develop an AUTOSAR-compliant Vehicle Speed and LED Control System that reads wheel speed information, calculates vehicle speed, and controls LED behavior based on the calculated speed. The implementation utilizes AUTOSAR Software Components (SWCs), Sender-Receiver communication, Ports, Runnables, Composition Components, Assembly Connectors, System Mapping, SWC Implementation Mapping, and System Extract generation.

---

## Features

- Wheel speed acquisition and processing
- Vehicle speed calculation
- LED control based on vehicle speed
- AUTOSAR Sender-Receiver communication
- Software Component (SWC) design
- Runnable and Internal Behavior implementation
- Composition and Assembly Connector configuration
- System Mapping and SWC Implementation Mapping
- System Extract creation using ARXML
- ARTOP/Eclipse based development

---

## System Architecture

```text
WheelSpeedASWC
        │
        ▼
WheelSpeed
        │
        ▼
VechicleSpeedASWC
        │
        ▼
VechicleSpeed
        │
        ▼
LedActuatorSWC
        │
        ▼
LedSignal
        │
        ▼
LedControlASWC
```

---

## Software Components

### WheelSpeedASWC
- Acquires wheel speed data.
- Publishes WheelSpeed signal.

### VechicleSpeedASWC
- Reads WheelSpeed.
- Calculates Vehicle Speed.
- Publishes VechicleSpeed signal.

### LedActuatorSWC
- Reads VechicleSpeed.
- Generates LedSignal based on speed conditions.

### LedControlASWC
- Reads LedSignal and Vehicle Speed.
- Controls LED indication logic.

### WheelEcuAbstractionSWC
- Represents ECU abstraction layer for wheel speed acquisition.

---

## Interfaces

### SpeedSRInterface_Wheel
| Data Element |
|-------------|
| WheelSpeed |

### SpeedSRInterface_Vechicle
| Data Element |
|-------------|
| VechicleSpeed |

### SpeedSRInterface_Led
| Data Element |
|-------------|
| LedSignal |

### SpeedCSInterface
| Operation |
|-----------|
| GetSpeed |

---

## Composition Structure

```text
SpeedComposition
│
├── WheelSpeedSwComponentPrototype
├── VechicleSpeedSwComponentPrototype
├── LedActuatorComponentPrototype
├── LedControlComponentPrototype
│
├── Conn_Wheel_to_Vehicle
├── Conn_Vehicle_to_LedActuator
├── Conn_LedActuator_to_LedControl
└── Conn_Vehicle_to_LED
```

---

## AUTOSAR Concepts Used

- Application SW Components
- Sensor Actuator SW Components
- ECU Abstraction SW Components
- Sender-Receiver Interfaces
- Client-Server Interfaces
- Ports (P-Port / R-Port)
- Runnable Entities
- Internal Behaviors
- Composition SW Components
- Assembly Connectors
- Delegation Connectors
- System Mapping
- SWC Implementation Mapping
- System Signals
- ARXML Modeling

---

## Tools Used

- ARTOP Eclipse
- AUTOSAR Classic Platform
- ARXML
- Java Runtime Environment

---

## System Extract Elements

### ECU Instance

```text
SpeedECU
```

### Communication Cluster

```text
SpeedCANCluster
```

### System Signals

```text
WheelSpeedSignal
VehicleSpeedSignal
LedSignalSystem
```

---

## Project Workflow

```text
1. Interface Creation
2. Data Type Creation
3. SWC Development
4. Port Configuration
5. Runnable Configuration
6. Composition Creation
7. Assembly Connector Configuration
8. Top Level Composition
9. Delegation Connectors
10. ECU Mapping
11. SWC Implementation Mapping
12. Sender Receiver To Signal Mapping
13. System Extract Generation
```

---

## Learning Outcomes

- AUTOSAR component design
- Sender-Receiver communication
- SWC integration
- Composition and Connector configuration
- System Mapping and Data Mapping
- System Extract development
- AUTOSAR ARXML modeling

---

