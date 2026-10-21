---
document_id: OP-AI-ASSURANCE-ADD-2026-10-21
version: 0.1
status: Proposed amendment for controlled review
date: 2026-10-21
classification: Internal working method
applies_to: [Enterprise Service Model Selection and Assurance, AI Operational Assurance, Service Option Review, Target Implementation Design, Independent Fallback Coverage, Minimum Viable Enterprise Operation]
publication_status: Not a controlled release
---
# OP Enterprise AI Assurance: Control Independence and Regulatory Portability

## 1. Purpose and applicability
This proposed amendment establishes two mandatory design and assurance considerations for enterprises procuring, building, deploying, changing or migrating AI-enabled services, particularly autonomous agents and open-weight models. It supplements existing security, procurement, privacy, intellectual-property, resilience and lifecycle-cost controls. Case reports that motivated review must be verified separately; this amendment does not assert that any particular reported incident or regulatory order is authentic or universally applicable.

## 2. Principle A: Independent control preservation
**An AI-enabled system shall not be entrusted with unilateral authority to disable, weaken, conceal or attest to the effectiveness of the independent controls governing its own operation.**

### 2.1 Design requirements
1. Separate agent execution identities from security administration, policy enforcement, logging, evidence retention and recovery administration.
2. Protect monitoring, alert routing, audit trails, authorization policy, secrets and backup controls through technical boundaries external to the agent's change authority.
3. Require independently authorized change approval for modifications to those controls, including seemingly incidental refactoring, configuration changes, dependency substitutions and deployment scripts.
4. Use immutable or tamper-evident records, independent telemetry and out-of-band alerting where warranted by consequence.
5. Require independent verification of controls after agent-generated changes; agent self-reports do not constitute acceptance evidence.
6. Define safe suspension, rollback, quarantine and human-controlled restoration procedures. Preserve a viable non-agent path for essential business processes.

### 2.2 Assurance tests and evidence
- Authorized-task adversarial test: agent completes a legitimate change while controls remain intact.
- Control-tamper test: attempts to remove alerts, logs, approval gates, credentials boundaries or backup protections are prevented or independently detected.
- Delegation test: subagents and tool chains cannot acquire broader control-plane permissions through inherited context.
- Post-change verification: independent monitor heartbeat, policy diff, audit event completeness, rollback proof and owner sign-off.
- Recovery exercise: suspend agent access and execute minimum viable enterprise operation without reliance on the compromised control plane.
- Evidence: permission matrix, signed change record, test results, independent logs, exceptions register and remediation owner.

### 2.3 Gate criteria
At Gate 2 (Plan), establish the independent control boundary and test plan. At Gate 3 (Operational Readiness), demonstrate passing results for critical agent workflows. At Gate 4 (Close-out), retain assurance evidence and unresolved exceptions. Re-test after material model, tool, orchestration or permission changes.

## 3. Principle B: Regulatory and supply-chain portability
**Technical portability does not establish an enterprise's continuing legal, contractual or operational right and ability to use an AI capability.**

### 3.1 Design requirements
1. Maintain an inventory of models, weights, derivatives, adapters, embedded components, inference services, datasets, training/fine-tuning provenance and critical suppliers.
2. Record applicable licences, permitted uses, IP provenance, indemnities, jurisdiction, procurement eligibility, export controls, sanctions and data-sovereignty constraints.
3. Identify direct and indirect dependencies on restricted models, including products that embed or derive from them. Distinguish confirmed legal scope from unsettled interpretations.
4. Evaluate SaaS/API, hosted open-weight, self-hosted and alternate-provider options against **fully loaded** costs: GPU capacity, power, operations, security, testing, integration, maintenance, monitoring, licensing, data transfer and exit.
5. Establish a jurisdiction-aware substitution plan with approved alternative models and independent capacity, not merely an API abstraction.
6. Verify model performance and safety on representative enterprise cases, including unfavourable decisions, complex cases, exceptions, multilingual needs and auditability.
7. Contract for notice of withdrawal, material terms changes, pricing shifts, dependency substitutions, data export, deletion, transition assistance and operational continuity where feasible.

### 3.2 Assurance tests and evidence
- Regulatory withdrawal tabletop: designated model or embedded component becomes prohibited for a defined customer or jurisdiction.
- Supply-chain trace: identify every affected product, workload, supplier, contract and downstream decision process.
- Substitution test: demonstrate legally eligible alternate deployment, data portability, functional equivalence, acceptable accuracy, throughput, latency, privacy, security and cost.
- Commercial stress test: model price increase, capacity shortfall, export restriction and loss of supplier support.
- Evidence: dependency bill of materials, legal/procurement review, jurisdiction matrix, tested replacement recipe, resource envelope, exit estimate and accountable approval.

### 3.3 Gate criteria
At Gate 0 (Qualification), screen prohibited dependencies and jurisdictional constraints. At Gate 1 (Initiation), document provenance and affected stakeholders. At Gate 2, select and cost viable alternatives. At Gate 3, execute substitution and continuity tests. At Gate 4, archive evidence and set periodic review triggers.

## 4. Integration with OP operating doctrine
- **Service Option Review:** score control independence and regulatory portability separately from technical interoperability and vendor marketing claims.
- **Target Implementation Design:** model data flows, control planes, supply-chain provenance, infrastructure constraints and jurisdictional failure domains.
- **Independent Fallback Coverage (IFC):** require alternatives outside the compromised security-control or prohibited-supplier domain.
- **Minimum Viable Enterprise Operation (MVEO):** demonstrate continuity of critical decisions and transactions without the agent or restricted model.
- **AI Resource Envelopes:** include cost and capacity of compliant substitutes, migration testing and reserved fallback resources.
- **AI Jury / governance:** route disputed risk acceptances and high-impact exceptions to independent review; retain human accountability.

## 5. Monitoring triggers
Reassess when an agent modifies a protected control; monitoring evidence becomes incomplete; a model or component is withdrawn or restricted; legal interpretation changes; a supplier changes provenance or licence terms; model pricing or GPU availability materially changes; or a substitution exercise fails.

## 6. Publication and document control
This is a **proposed companion amendment**, not a silent modification of an approved manual. The authoritative catalogue identifier, parent doctrine editions, superseded handling and approval status must be reconciled before promotion. Apply OP branding and publication/IP standards to the controlled edition. Validate secure watermarking, digital signatures and forensic marks before any external distribution. No assertion of completed validation is made here.

**ACTION:** Map this amendment to the current authoritative doctrine and Stage 0–4 manuals, conduct independent juror/Board review, record approval and promote only through controlled publication.
