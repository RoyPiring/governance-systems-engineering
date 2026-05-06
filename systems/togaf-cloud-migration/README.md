# Architect a Cloud Migration with TOGAF

> Inside the [Governance Systems Engineering](../../README.md) portfolio · *Systems aligned to enterprise governance, security, and architecture standards.*

## Overview

This project defines a cloud migration strategy using the TOGAF ADM framework for GreenLeaf Groceries.

The goal is to move from fragmented on-premise systems to a structured cloud architecture, ensuring the migration is driven by business outcomes, not just infrastructure changes.

The architecture is built across **7 phases**, anchored by **The Mission: Architecting a Cloud Migration for GreenLeaf Groceries** on the input side and **💎 Secret Mission: Phase E Opportunities & Solutions Roadmap** at the end. Each phase is listed in the Implementation section below.

## Architecture

```mermaid
---
title: Architect a Cloud Migration with TOGAF
---
%%{init: {"theme":"base","themeVariables": {"primaryColor":"#1B4332","primaryTextColor":"#F4D03F","primaryBorderColor":"#F4D03F","secondaryColor":"#264653","tertiaryColor":"#2F5233","lineColor":"#F4D03F","fontFamily":"ui-monospace, SFMono-Regular, Menlo, Consolas, monospace","fontSize":"13px"}}}%%
flowchart TD
    classDef datastore fill:#264653,stroke:#F4D03F,stroke-width:2px,color:#FFFFFF
    classDef service fill:#1B4332,stroke:#F4D03F,stroke-width:2px,color:#F4D03F
    classDef event fill:#7B42BC,stroke:#F4D03F,stroke-width:2px,color:#FFFFFF
    classDef io fill:#0d1117,stroke:#F4D03F,stroke-width:1.5px,color:#F4D03F,font-style:italic







    BizDrivers[/Business Drivers: Cost, Availability, New Services/]
    Stakeholders[/Stakeholder Concerns/]

    subgraph TOGAF_ADM["TOGAF ADM - GreenLeaf Groceries"]
        Prelim(Preliminary: EA Workbench and Principles)
        PhaseA(Phase A: Architecture Vision)
        PhaseB(Phase B: Baseline Business Architecture)
        PhaseCD(Phase C and D: Data, App, Tech Architectures)
        PhaseE(Phase E: Opportunities and Solutions)
        PhaseF(Phase F: Migration Planning)

        Gate1{{Governance Gate: Principles Approved}}
        Gate2{{Governance Gate: Vision Sign-off}}
        Gate3{{Governance Gate: Gap Analysis Review}}

        ADR1[(ADR-001: Adopt TOGAF ADM)]
        ADR2[(ADR-002: Cloud-Native First)]
        ADR3[(ADR-003: Monitoring and Backup Risks)]
        Repo[(Architecture Repository - ABBs and ArchiMate Models)]
    end

    subgraph CloudTarget["Target Cloud Architecture"]
        Baseline[/Baseline: Fragmented POS, Manual Inventory, Disconnected Suppliers/]
        Target[/Target: Centralized Cloud, Integrated Services, Managed Platforms/]
        C4[(C4 System Context Diagram)]
        Roadmap[(Work Packages and Gantt Roadmap)]
    end

    BizDrivers -->|inform| Prelim
    Stakeholders -->|map to| PhaseA
    Prelim -->|principles| Gate1
    Gate1 -->|approved| PhaseA
    Prelim -->|emits| ADR1
    Prelim -->|defines| ADR2
    PhaseA -->|vision| Gate2
    Gate2 -->|sign-off| PhaseB
    PhaseB -->|current state| Baseline
    Baseline -->|inputs to| PhaseCD
    PhaseCD -->|future state| Target
    PhaseCD -->|emits| C4
    PhaseCD -->|gap analysis| Gate3
    PhaseCD -->|risks| ADR3
    Gate3 -->|approved| PhaseE
    PhaseE -->|prioritized| Roadmap
    Roadmap -->|sequenced| PhaseF
    PhaseF -->|delivers| Target

    ADR1 -.governs.-> Repo
    ADR2 -.governs.-> Repo
    ADR3 -.governs.-> Repo
    PhaseB -.artifacts.-> Repo
    PhaseCD -.artifacts.-> Repo
    PhaseE -.artifacts.-> Repo
class ADR1,ADR2,ADR3,Repo,C4,Roadmap datastore
class Gate1,Gate2,Gate3 event

    class ADR1,ADR2,ADR3,Repo,C4,Roadmap datastore
    class Prelim,PhaseA,PhaseB,PhaseCD,PhaseE,PhaseF service
    class Gate1,Gate2,Gate3 event
    class BizDrivers,Stakeholders,Baseline,Target io
```

The diagram shows the topology and data flow of the system as built. The full architectural narrative, with screenshots and prose, lives in [`documents/togaf-cloud-migration.md`](./documents/togaf-cloud-migration.md).

## Implementation

This system is built across **7 phases**:

1. **The Mission: Architecting a Cloud Migration for GreenLeaf Groceries** — This project defines a cloud migration strategy using the TOGAF ADM framework for GreenLeaf Groceries.
2. **Building the EA Workbench**
3. **Defining Architecture Principles (Preliminary Phase)**
4. **Crafting the Architecture Vision (Phase A)**
5. **Modeling the Baseline Business Architecture (Phase B)**
6. **Modeling the Target Technology Architecture and Analyzing Gaps (Phase D)**
7. **💎 Secret Mission: Phase E Opportunities & Solutions Roadmap**

For the full walkthrough with screenshots and step-by-step content, see [`documents/togaf-cloud-migration.md`](./documents/togaf-cloud-migration.md).

## Validation

Build outcomes verified end-to-end. Each phase below is captured with screenshots, configuration, and observable behavior in [`documents/togaf-cloud-migration.md`](./documents/togaf-cloud-migration.md):

- ✅ The Mission: Architecting a Cloud Migration for GreenLeaf Groceries
- ✅ Building the EA Workbench
- ✅ Defining Architecture Principles (Preliminary Phase)
- ✅ Crafting the Architecture Vision (Phase A)
- ✅ Modeling the Baseline Business Architecture (Phase B)
- ✅ Modeling the Target Technology Architecture and Analyzing Gaps (Phase D)
- ✅ 💎 Secret Mission: Phase E Opportunities & Solutions Roadmap
