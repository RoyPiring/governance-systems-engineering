<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Govern Parallel AI Agents for SCADA

**Project Link:** [View Project](https://learn.nextwork.org/projects/61474dd5-f5d7-4703-b3c2-1b8b78c67cc7)

**Author:** Roy Piring Jr  
**Email:** rpiringhawaii@gmail.com

---

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/61474dd5-f5d7-4703-b3c2-1b8b78c67cc7_oaslftbw)

## Governing a 90-Minute INCOSE Vee Sprint for Critical Infrastructure

### Project scope and mission

In this project, I executed a full INCOSE Vee lifecycle simulation for a municipal water-treatment SCADA modernization effort using parallel AI agent orchestration. The objective was to produce a complete systems engineering artifact package, deploy a running containerized digital twin, and establish a reusable governance framework for coordinating multiple AI engineering agents under safety-critical constraints.

The sprint combined requirements engineering, architecture governance, verification and validation, cybersecurity analysis, and operational risk management into a single coordinated workflow. Instead of treating AI agents as isolated assistants, the project focused on governing them as controlled contributors inside a structured systems engineering process.

## Launching the Program: Environment Setup and Parallel Agent Orchestration

### Step objectives

I configured the engineering environment using Docker Desktop, Python 3.12, Git, Capella, OpenPLC Editor, Wireshark, and Codex Desktop while container pulls and background initialization tasks executed in parallel.

The workspace was structured around a governed program directory containing requirements baselines, architecture artifacts, gate-review templates, metrics dashboards, and agent-specific output boundaries. Five AI agent teams were launched simultaneously with controlled execution scopes and predefined deliverables.

This transformed the environment into a coordinated systems-engineering program rather than a sequence of isolated tooling exercises.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/61474dd5-f5d7-4703-b3c2-1b8b78c67cc7_1etak2bb)

### Agent governance and permission boundaries

AGENTS.md functioned as the operational governance charter for the entire program.

It defined authority boundaries, ownership rules, and artifact locations for each engineering team while preserving final approval authority under the Principal Systems Engineer role. Agents were restricted from modifying artifacts outside their approved domains unless explicitly authorized through gate review.

The important architectural principle was containment. AI agents were treated as scoped contributors with constrained authority rather than unrestricted autonomous actors.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/61474dd5-f5d7-4703-b3c2-1b8b78c67cc7_yd4sd6j4)

## Wave 1: Requirements Engineering and Passing the SRR and PDR Gates

### Step objectives

The first execution wave focused on requirements baselining and architectural review under formal gate criteria.

Agent teams generated stakeholder requirements, system requirements, architectural outputs, and traceability mappings while SRR and PDR reviews validated completeness, quality, and alignment against program objectives.

This established the initial systems-engineering baseline before implementation and simulation work began.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/61474dd5-f5d7-4703-b3c2-1b8b78c67cc7_op0jy8ub)

### SRR gate criteria and requirements quality score

The SRR gate validated requirements quality, traceability coverage, and structural consistency inside Doorstop.

Every stakeholder requirement mapped to at least one system-level requirement, and the overall requirements-quality score averaged 7.0 out of 8.

The focus was not only completeness, but governance integrity. Traceability ensured that no system requirement existed without originating business or operational justification.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/61474dd5-f5d7-4703-b3c2-1b8b78c67cc7_ms5pwatu)

## Wave 2: Launching the ICS Digital Twin and Passing the CDR Gate

### Step objectives

The second execution wave deployed the SCADA digital twin, validated live HMI communication, and advanced the system through the CDR gate.

OpenPLC, FUXA, and containerized networking components were integrated into a live simulation environment while governance artifacts and validation planning continued in parallel.

This phase shifted the project from static engineering documentation into operational system behavior.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/61474dd5-f5d7-4703-b3c2-1b8b78c67cc7_7o96ij6l)

### Container networking and Modbus/TCP communication

The HMI communicated with the PLC over Modbus/TCP using Docker container networking instead of localhost routing.

FUXA connected directly to the PLC container over the shared Docker network using the PLC container’s internal IP address. localhost was intentionally avoided because each container maintains its own isolated network namespace.

This reflects real industrial-control-system behavior where deterministic network routing and protocol isolation matter more than simplified local execution.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/61474dd5-f5d7-4703-b3c2-1b8b78c67cc7_1igufngl)

## Wave 3: V&V Execution, TPM Dashboard, and Closing the Vee

### Step objectives

he final execution wave focused on verification and validation, technical performance measurement, and closure of the Vee lifecycle.

The system executed the V&V suite, conducted the TRR gate review, published requirements evidence, and generated the Digital Thread visualization alongside TPM dashboards and risk-burndown reporting.

This phase validated not only system functionality, but lifecycle completeness and governance maturity.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/61474dd5-f5d7-4703-b3c2-1b8b78c67cc7_zwi4d9rn)

### V&V pass rate and residual risk posture

The V&V execution completed with a 100% pass rate across all eleven validation scenarios.

No open hazards remained after the TRR review, although one residual risk tied to wording ambiguity in SYS-008 and SYS-010 remained formally accepted and documented.

The important distinction was that residual risk was governed transparently rather than hidden behind a simplified “all clear” result.

### Gate trail and FCA proof of compliance

The project maintained explicit gate-trail tagging across SRR, PDR, CDR, and TRR approvals.

The FCA gate remained in HOLD status because full bidirectional traceability between STK, SYS, SUB, and TEST artifacts had not yet been fully validated through governed Doorstop records.

This decision reinforced engineering discipline by prioritizing evidence completeness over premature closure.

## Director Package: Executive Summary and Program Sign-Off

### Step objectives

The final delivery package consolidated engineering outputs, KPIs, governance evidence, and executive recommendations into an audit-ready release artifact.

This included readiness validation, program metrics, final gate status, and a formal go/no-go recommendation for CSEP submission readiness.

The output was designed to communicate equally well to technical reviewers, auditors, and executive stakeholders.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/61474dd5-f5d7-4703-b3c2-1b8b78c67cc7_8czq21dd)

### Go/no-go recommendation and supporting evidence

The final recommendation was GO for CSEP submission based on successful V&V execution, completed gate reviews, and validated operational evidence across the systems-engineering lifecycle.

Readiness indicators included a 100% V&V pass rate, complete stakeholder-to-system requirement coverage, zero unresolved operational hazards, and validated governance artifacts across SRR, PDR, CDR, and TRR phases. Traceability evidence, risk controls, and digital-thread outputs demonstrated that the program met the required engineering and compliance objectives for release readiness.

This reinforced that AI-augmented systems engineering can still maintain formal governance, auditability, and lifecycle discipline while accelerating delivery through parallel agent execution.

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/61474dd5-f5d7-4703-b3c2-1b8b78c67cc7_y7vpks7w)

## Secret Mission: Suricata IDS Integration and Security KPIs

![Image](https://learn.nextwork.org/refreshed_maroon_timid_jujube/uploads/61474dd5-f5d7-4703-b3c2-1b8b78c67cc7_vbt6asjy)

### Modbus attack detection scenarios and water treatment safety impact

I extended the simulation by integrating Suricata IDS monitoring into the SCADA environment to model industrial attack detection scenarios.

The detection rules targeted unauthorized Modbus operations such as EMERGENCY_STOP coil writes and chlorine-dosing register manipulation. These scenarios represent realistic operational threats capable of disrupting treatment operations or introducing unsafe chemical conditions inside a municipal water system.

This transformed the digital twin from a functional simulation into a security-aware operational environment.

## Reflections: Tools, Concepts, and the Value of AI-Augmented Systems Engineering

### Key tools and concepts

This project combined Docker, Python, Git, Capella, OpenPLC Editor, Wireshark, Codex Desktop, and Suricata into a governed systems-engineering workflow.

The concepts reinforced throughout the sprint included INCOSE Vee lifecycle execution, requirements traceability, industrial protocol validation, AI-agent governance, verification and validation methodology, cybersecurity monitoring, and digital-thread management.

### Time and effort reflection

This project took approximately two hours to complete. The most difficult part was coordinating governance and orchestration behavior across multiple AI agent teams while preserving auditability and engineering discipline.

The Codex execution environment introduced additional operational friction around interface limitations and orchestration visibility, which became the primary bottleneck during parallel execution phases.

### Personal learning goals

The biggest takeaway was understanding how AI agents can participate in systems engineering workflows without bypassing governance and verification requirements.

The next area I want to advance is building larger reusable governance frameworks capable of directing AI agents across longer-running engineering programs and multi-phase infrastructure modernization efforts.

---

*Built with [NextWork](https://learn.nextwork.org) - [View this project](https://learn.nextwork.org/projects/61474dd5-f5d7-4703-b3c2-1b8b78c67cc7)*
