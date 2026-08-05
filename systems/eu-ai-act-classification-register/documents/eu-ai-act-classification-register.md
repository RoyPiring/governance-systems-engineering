<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# EU AI Act Classification Register

**Project Link:** [View Project](https://nextwork.ai/projects/eaf5900d-2071-4e30-a3fc-12fa086b4b99)

**Author:** Roy Piring Jr: Sr. Cloud Engineer | Architect  
**Email:** rpiringhawaii@gmail.com

---

![Image](https://nextwork.ai/refreshed_maroon_timid_jujube/uploads/eaf5900d-2071-4e30-a3fc-12fa086b4b99_h1w5d6qs)

## Building a Deterministic AI Regulatory Classification System

### The case for reproducible, fact-based tier assignment

In this build, I created a deterministic AI system register that classifies use cases based on EU AI Act tiering logic. The register was designed to produce the same result each time the same facts were evaluated.

That mattered because regulatory classification cannot depend on a model’s tone, confidence, or interpretation style. The system needed a transparent audit trail that showed why each use case landed in a tier.

The result was a logic-based classification path. Stakeholders could validate outcomes numerically, compare them against sealed ground truth, and route ambiguous cases to human review instead of forcing the engine to guess.

## Designing the Architecture and Verifying the Toolchain

### Decision records, topology diagram, and workspace setup

In this step, I set up the workspace and documented the architecture for the EU AI Act classification register. The design records captured the classification approach, the policy-as-code boundary, and the evidence flow.

The topology diagram showed how OSCAL data, Rego rules, sealed ground truth, model-drafted rationales, and governance outputs connected. That gave the system a clear shape before classification logic was trusted.

This mattered because regulatory engineering needs a documented path from input facts to decision output. The workspace, records, and diagram made the register easier to review and maintain.

### End-to-end toolchain verification with OPA

opa eval returned {"tier": "unknown"} inside OPA’s result JSON. That was the default rule firing because props was empty and no other condition matched.

That result proved the toolchain was wired correctly. OPA executed the Rego policy, read the project structure, and returned a policy result.

It also confirmed that OPA, Rego, PATH, and the policy/ plus sealed/ wiring worked end to end inside the build.

## Authoring the OSCAL Register and Sealed Ground Truth

### 25 AI use cases as machine-readable component definitions

In this step, I built a machine-readable register of 25 AI systems using OSCAL component definitions. Each system carried structured properties about its purpose, context, and classification-relevant facts.

The engine used those properties as its input surface. That kept the tiering logic tied to structured data instead of prose descriptions alone.

This mattered because regulatory classification needs evidence that can be parsed and tested. OSCAL gave the register a machine-readable format that could support deterministic evaluation.

![Image](https://nextwork.ai/refreshed_maroon_timid_jujube/uploads/eaf5900d-2071-4e30-a3fc-12fa086b4b99_jm4fvyfn)

### Register structure and the ambiguous 25th system

The register contained 25 OSCAL components, from sys-01 through sys-25.

The sealed ground truth covered 24 of them, from sys-01 through sys-24.

sys-25-cv-dedup had no sealed entry by design. It was the ambiguous human-queue case, not a system that should receive an automated tier answer.

## Proving the Tiering Engine: 24/24 with Zero Disagreements

### Rego rules classifying every system deterministically

In this step, I built the deterministic tiering engine with Rego. The rules evaluated each AI system’s OSCAL properties and assigned the correct tier, conformity route, and regulatory deadline.

The engine proved 24 out of 24 classifications against the sealed ground truth with zero disagreements. That showed the policy logic matched the expected tiering decisions for the sealed cases.

The ambiguous case was handled separately. Instead of forcing a tier, the engine routed it to a human queue, which preserved the boundary between deterministic classification and governance judgment.

### Why the ambiguous case routes to the human queue

System 25 sat in Annex III employment, listed as 4_employment, with an Article 6(3) exception that was only arguable. Its properties included narrow_procedural_task and exception_arguable, but they did not make the exception definitive.

It was not profiling, and it had no sealed ground-truth answer. The rules therefore refused to choose high-risk or residual automatically.

The engine returned human_queue. That was a governance decision, not a deterministic tier assignment.

## Scoring Model-Drafted Rationales Through a Gated Harness

### The model beside the critical path, not on it

In this step, I built a scoring harness for model-drafted rationales. The model could help draft explanations, but it did not control tier assignment.

The harness scored rationale text against a defined rubric before any explanation could be accepted into the register. That kept the model beside the critical path instead of inside it.

This mattered because legal classification had to come from Rego and sealed ground truth. The model could support explanation, but it could not become the source of regulatory truth.

![Image](https://nextwork.ai/refreshed_maroon_timid_jujube/uploads/eaf5900d-2071-4e30-a3fc-12fa086b4b99_m8jaua0a)

### Graceful degradation when drafting stalls

If drafting failed or stalled, the register still held. Tiers came from Rego and sealed ground truth, not from model output.

The harness rejected a rationale run when it fell below 22 out of 24. Those texts stayed out of the register.

The estate classification remained correct because CI could still prove 24 out of 24 without any model-drafted rationale. The model path could fail without breaking the classification engine.

## Re-Tiering the Estate Under the July 2026 Amendment

### Encoding Regulation (EU) 2026/1744 and computing the diff

In this step, I encoded Regulation (EU) 2026/1744 into a new Rego policy file. The goal was to formalize the legislative update and compute the classification diff.

The re-tiering run checked which AI systems were affected by shifted deadlines and new Article 5 prohibitions. It also verified whether any current systems were hit by the new prohibition.

This mattered because regulatory registers cannot stay static. A useful register needs version-controlled policy changes and a clear diff that shows what changed, what did not, and what the board must decide.

![Image](https://nextwork.ai/refreshed_maroon_timid_jujube/uploads/eaf5900d-2071-4e30-a3fc-12fa086b4b99_nqkt75o5)

### 15 changed records and the board decision asked for

The re-tiering diff showed 15 high-risk systems gained more preparation time. Twelve Annex III systems moved to 2 Dec 2027, and three Annex I systems moved to 2 Aug 2028.

The update also added a CSAM and intimate-material prohibition for future intake. Zero current systems were hit, and no tiers or obligations were dropped.

The board ask was to approve the register as the Article 6 classification record, send System 25 to counsel, accept residual risk on the three deadline-blocked conformity controls, and set a quarterly or Official Journal-triggered review cadence.

## Delivering the Governance Package and Board Briefing

![Image](https://nextwork.ai/refreshed_maroon_timid_jujube/uploads/eaf5900d-2071-4e30-a3fc-12fa086b4b99_86lx3fv5)

### Control library, risk register, and the conformity gap plainly stated

The briefing asked the committee to approve the register as the Article 6 classification record, send System 25 to counsel, accept residual risk on the three deadline-blocked conformity controls, and set a quarterly or Official Journal-triggered review cadence.

It also stated the conformity gap plainly. As of the SNAPSHOT date, no AI Act harmonised standard had been cited in the Official Journal, so Article 40(1) did not apply.

A management-system certificate, such as ISO 42001, was not treated as a harmonised standard. It did not create a presumption of conformity.

## Reflections and Takeaways

### Tools and concepts from regulatory engineering to policy-as-code

The key tools I used included Open Policy Agent for deterministic Rego execution, compliance-trestle for OSCAL component definitions, and GitHub Actions for continuous evidence generation.

The main concepts I learned included building a reproducible regulatory classification engine, mapping legal obligations to control frameworks, routing ambiguous cases to governance review, and maintaining a compliance posture through version-controlled legislative diffs.

The larger lesson was that regulatory classification should be treated like an engineering system. Facts, rules, sealed expectations, and review decisions need clear boundaries so the result can be defended.

### Time and challenges

This build took me approximately 70 minutes. That time covered workspace setup, design records, OSCAL register authoring, sealed ground truth, Rego tiering, rationale scoring, legislative re-tiering, governance packaging, and the board briefing.

The hardest part was making the Rego logic handle EU AI Act nuance while still producing deterministic output. The rules had to classify clear cases cleanly and refuse to decide ambiguous cases that belonged in human review.

The amendment diff was also important because it proved the register could change with the law without losing its audit trail. It showed which records changed, which ones did not, and which board decisions remained open.

I completed this build to learn how to create deterministic regulatory-classification systems with Open Policy Agent and Rego for EU AI Act tiering. Next, I want to connect compliance-as-code workflows into CI/CD pipelines so audit readiness can run continuously.

---

*Built with [NextWork](https://nextwork.ai) - [View this project](https://nextwork.ai/projects/eaf5900d-2071-4e30-a3fc-12fa086b4b99)*
