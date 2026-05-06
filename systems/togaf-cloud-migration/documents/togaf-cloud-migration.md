<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Architect a Cloud Migration with TOGAF

**Project Link:** [View Project](https://learn.nextwork.org/projects/eeeabe80-d81b-4d19-931c-d17f6dacac2a)

**Author:** Roy Piring Jr  
**Email:** rpiringhawaii@gmail.com

---

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/eeeabe80-d81b-4d19-931c-d17f6dacac2a_r7t4x9nb)

## The Mission: Architecting a Cloud Migration for GreenLeaf Groceries

This project defines a cloud migration strategy using the TOGAF ADM framework for GreenLeaf Groceries.

The goal is to move from fragmented on-premise systems to a structured cloud architecture, ensuring the migration is driven by business outcomes, not just infrastructure changes.

## Building the EA Workbench

### Tools and environment setup

The workbench establishes structure for managing architecture artifacts.

Folders are organized by ADM phase, ensuring each stage of the migration is documented and traceable. This creates a controlled environment where decisions, models, and outputs remain aligned throughout the lifecycle.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/eeeabe80-d81b-4d19-931c-d17f6dacac2a_rt4j7bqe)

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/eeeabe80-d81b-4d19-931c-d17f6dacac2a_hx2f9wla)

The numbered prefixes help with maintaining order within the project folder structure because they ensure that the folders corresponding to each TOGAF ADM phase are sequentially organized.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/eeeabe80-d81b-4d19-931c-d17f6dacac2a_zy6p4mcr)

## Defining Architecture Principles (Preliminary Phase)

### Governing principles for the migration

Architecture principles define how decisions are made across the migration.

Prioritizing cloud-native solutions ensures systems are designed for scalability, cost efficiency, and long-term flexibility, rather than replicating on-premise limitations in the cloud.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/eeeabe80-d81b-4d19-931c-d17f6dacac2a_xt4p9bwk)

### First Architecture Decision Record

The first ADR documents the decision to use TOGAF ADM as the governing framework.

This establishes a structured approach for planning, decision-making, and traceability across all phases of the migration.

## Crafting the Architecture Vision (Phase A)

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/eeeabe80-d81b-4d19-931c-d17f6dacac2a_r4tn7bqx)

### Stakeholder mapping and concerns

Stakeholders are classified based on influence and impact.

This ensures communication and priorities are aligned with business objectives, reducing risk during the migration process.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/eeeabe80-d81b-4d19-931c-d17f6dacac2a_qp5xv8ht)

### Architecture Vision statement

The vision translates business problems into measurable targets.

Reducing cost, increasing availability, and enabling new services provide a clear direction for the target architecture.

## Modeling the Baseline Business Architecture (Phase B)

### ArchiMate business layer — current state

The baseline model captures how GreenLeaf operates today.

Business actors, processes, and services are mapped to identify inefficiencies and gaps in current operations.

### Baseline narrative: how GreenLeaf operates today

The current state is fragmented across stores.

Each location operates independently with separate POS systems, manual inventory tracking, and disconnected supplier processes. 

This lack of integration limits visibility and prevents efficient decision-making.

## Modeling the Target Technology Architecture and Analyzing Gaps (Phase D)

### ArchiMate technology layer — future state

The target architecture defines a centralized, cloud-based system.

It introduces integrated services, scalable infrastructure, and managed platforms that replace manual and disconnected processes.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/eeeabe80-d81b-4d19-931c-d17f6dacac2a_rn4t7bxe)

### Gap analysis: baseline to target

The gap analysis identifies what must change to reach the target state.

Relationships between infrastructure, technology services, and business services clarify how cloud systems will support business operations. This ensures the design is driven by outcomes, not just technical implementation

### C4 System Context diagram and ADR

The system context diagram defines system boundaries and external interactions.

The ADR captures risks such as missing monitoring, backup, and availability controls, which would result in outages and operational instability if not addressed.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/eeeabe80-d81b-4d19-931c-d17f6dacac2a_qz3a6ywn)

## 💎 Secret Mission: Phase E Opportunities & Solutions Roadmap

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/eeeabe80-d81b-4d19-931c-d17f6dacac2a_kw7m3xp2)

### Prioritized work packages and Gantt timeline

Work packages break the migration into manageable steps.

The timeline ensures dependencies are sequenced correctly and progress is measurable throughout the migration.

## Project Wrap-Up and Portfolio Delivery

### What you built

This project delivers a structured cloud migration plan aligned to TOGAF ADM.

It includes architecture models, gap analysis, ADRs, and a phased execution roadmap that connects business goals to technical implementation.

### Key concepts mastered

Core concepts include TOGAF ADM, architecture modeling, gap analysis, and structured decision-making through ADRs.

These concepts enable consistent planning and governance across complex technology transformations.

### Next steps and reuse

This project took about 65 minutes. The main challenge was aligning multiple artifacts across phases while keeping the architecture consistent.

The next step is applying this approach to real cloud environments, focusing on secure architecture design and implementation.

---

*Built with [NextWork](https://learn.nextwork.org) - [View this project](https://learn.nextwork.org/projects/eeeabe80-d81b-4d19-931c-d17f6dacac2a)*
