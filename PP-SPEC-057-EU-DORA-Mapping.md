# PP-SPEC-057: Proof of Efficacy Mapping to the EU Digital Operational Resilience Act (DORA)

| Field | Value |
|---|---|
| Status | DRAFT v0.1 |
| Author | Craig Ellrod, Nebulonium, Inc. (dba HACKERverse®) |
| Date | October 8, 2026 |
| License | CC BY 4.0 |
| Maps to | Regulation (EU) 2022/2554 (DORA) and its delegated and implementing regulations |
| Series | Proof Protocol Framework Mapping Specifications |

---

## 1. Purpose

This specification defines how the ICT risk management, ICT-related incident, digital operational resilience testing, and ICT third-party risk obligations of the EU Digital Operational Resilience Act can be bound to Proof Protocol test cases, evidence, and efficacy results.

DORA is Regulation (EU) 2022/2554 of the European Parliament and of the Council of 14 December 2022 on digital operational resilience for the financial sector, published in the Official Journal of the European Union on 27 December 2022. It applies from 17 January 2025. It is supplemented by Commission delegated regulations (regulatory technical standards, RTS) and implementing regulations (implementing technical standards, ITS), including:

- Delegated Regulation (EU) 2024/1774 (ICT risk management tools, methods, processes and policies, and the simplified ICT risk management framework);
- Delegated Regulation (EU) 2024/1772 (classification of ICT-related incidents and cyber threats);
- Delegated Regulation (EU) 2025/301 and Implementing Regulation (EU) 2025/302 (content, time limits, and templates for major ICT-related incident reporting);
- Delegated Regulation (EU) 2025/1190 (threat-led penetration testing, TLPT);
- Delegated Regulation (EU) 2024/1773 (contractual arrangements for ICT services supporting critical or important functions);
- Delegated Regulation (EU) 2025/532 (subcontracting of ICT services supporting critical or important functions);
- Implementing Regulation (EU) 2024/2956 (templates for the register of information); and
- Delegated Regulations (EU) 2024/1502, 2024/1505 and 2025/295 (oversight of critical ICT third-party service providers).

The upstream source remains authoritative for its own requirements, identifiers, terminology, and guidance. This document defines a **Proof Protocol mapping** and does not supersede, reproduce, modify, or certify conformance to the upstream source.

## 2. Scope

DORA supplies external context that can identify what should be examined or tested by a financial entity, a competent authority, an ICT third-party service provider, or a tester. Proof Protocol supplies an independent evidence model for determining what happened during a test and whether a selected control performed as claimed.

DORA is public law. Many of its obligations are governance, documentation, contractual, reporting, and supervisory obligations. This mapping binds empirical tests only to obligations that describe an observable technical behavior or outcome and keeps all other obligations as non-empirical context.

Independent witnessing, proof validity, evidence capture, packaging, anchoring, and efficacy semantics are defined elsewhere in the Proof Protocol specification family.

## 3. Core Question

Proof of efficacy asks:

> **Was there a control, and did it work?**

A framework requirement, criterion, principle, or obligation may identify a condition of interest. A product, architecture, policy, process, or safeguard may claim to satisfy or mitigate that condition. Proof Protocol binds the external context, test, control, observed behavior, downstream outcome, and evidence into a result that can be independently examined.

A Proof Protocol result does **not** by itself establish legal, audit, regulatory, or standards conformance unless the applicable authority separately determines that the evidence is sufficient.

A Proof Protocol result is **not a legal or regulatory determination** and does **not** establish compliance with DORA or any delegated or implementing act. A Proof Protocol test is not a TLPT within the meaning of DORA unless it is separately conducted and attested in accordance with DORA, Delegated Regulation (EU) 2025/1190, and the requirements of the competent authority. Determinations of compliance rest with financial entities' management bodies, competent authorities, the Lead Overseers, and courts.

## 4. Metric Definitions

Against a defined corpus or test condition, each applicable empirical case is recorded as **blocked**, **detected**, **missed**, or **INVALID** where those verdicts are meaningful.

Relevant measurements can include containment rate, detection rate, miss rate, false-positive rate, robustness under bypass or failure conditions, version-level results, and **INVALID** when required evidence is incomplete or broken.

Not every upstream requirement is empirical. Governance, documentation, organizational, legal, and procedural requirements MUST NOT be converted into efficacy scores merely because they can be referenced by a proof record.

## 5. Evidence Produced

Mapped tests can produce:

- **Proof records** binding external context, test case, control, system/version, verdict, timestamp, and evidence references;
- **ProofStamp™** trusted timestamps bound to evidence/verdict objects;
- **ProofBundle™** packages containing proof records, metrics, corpus manifests, and environment/context;
- **ProofRegister™** records for issued proof artifacts; and
- corpus and environment manifests identifying the tested conditions.

## 6. Mapping to DORA

Exact upstream identifiers and titles SHOULD be taken from the authoritative version being mapped and recorded in the ProofBundle™ where licensing permits. This specification does not redefine upstream requirements.

DORA provisions SHOULD be cited by instrument, article, and paragraph (for example, "Regulation (EU) 2022/2554, Article 26(1)"), together with the consolidated version date used.

| DORA context | Proof Protocol treatment | Evidence |
|---|---|---|
| Instrument and version (Regulation (EU) 2022/2554, RTS/ITS, consolidated version date) | Bind the instrument, article, paragraph, and EUR-Lex version used to the proof record. | Requirement metadata |
| Entity type and proportionality (Chapter I; simplified ICT risk management framework) | Record the financial entity type and whether the simplified framework applies, as context only. | Requirement metadata |
| ICT risk management framework (Chapter II) | Record the asserted protection, prevention, detection, and response measures separately from observed behavior. Governance and policy elements remain non-empirical. | Control descriptor; non-empirical annotation |
| Protection and prevention, detection (Chapter II) | Exercise defined adversarial or failure conditions and capture whether the measure prevented or detected them at the protected asset. | Execution evidence; outcome evidence |
| Response and recovery, backup and restoration (Chapter II) | Exercise disruption or loss conditions and capture whether recovery actually achieved the stated recovery objective. | Outcome evidence |
| ICT-related incident classification and reporting (Chapter III; RTS/ITS on classification and reporting) | Treat classification and reporting as procedural context. Bind only observable elements, such as whether an exercised incident condition was detected and recorded. | Detection result; non-empirical annotation |
| Digital operational resilience testing programme (Chapter IV) | Bind Proof Protocol test cases to the tests listed in the entity's programme as context. A Proof Protocol test does not discharge the programme. | Corpus/test metadata |
| Threat-led penetration testing (Chapter IV; Delegated Regulation (EU) 2025/1190) | Record TLPT scope and threat intelligence as context where the tester and entity permit. Proof records MAY serve as supporting evidence; they are not a TLPT attestation. | Proof records; corpus manifest |
| ICT third-party risk and register of information (Chapter V; RTS/ITS on contracts, subcontracting, register) | Record the third-party service, contractual function, and version as context. Contractual and register obligations remain non-empirical. | Requirement metadata; environment descriptor |
| Third-party service behavior under test | Exercise conditions affecting a service supporting a critical or important function and capture outcome evidence from the provider and the protected function. | Target/outcome evidence |
| Exception/failure condition | Exercise negative, bypass, misuse, or failure cases where applicable. | Proof records; robustness evidence |
| Evidence export for supervisory or audit review | Package evidence and provenance for independent examination. | ProofBundle |

## 7. Interoperability Rules

1. The authoritative upstream source, edition/version, and applicable identifier SHOULD be recorded.
2. Upstream identifiers and terminology MUST NOT be silently redefined.
3. Proof Protocol verdicts are Proof Protocol results; they are not upstream certifications, audit opinions, legal determinations, or endorsements.
4. A control's presence, configuration, activation, detection, and efficacy are distinct facts.
5. A policy decision, alert, log entry, or control trigger does not by itself establish efficacy when the claim concerns a downstream protected outcome.
6. Target, application, tool, SIEM, vendor, service, resource, or equivalent evidence SHOULD complete the evidence round trip when required to establish the result.
7. Missing required evidence MUST yield **INVALID**, not PASS.
8. Material changes to the tested system, policy, control, environment, mapping, or corpus SHOULD trigger retesting where they can affect the result.
9. Non-empirical requirements MUST remain distinguishable from empirically tested efficacy assertions.

## 8. Framework-Agnostic Architecture

> **Threat, control, audit, and regulatory frameworks are pluggable inputs to Proof Protocol. Proof Protocol is framework-agnostic.**

External frameworks can identify **what to test or examine**. Proof Protocol independently establishes **whether the control worked and what evidence proves that result**.

No external framework is required for Proof Protocol to operate. An implementation MAY use DORA, another recognized framework, a proprietary threat model, several frameworks simultaneously, or no external framework when the test condition is otherwise sufficiently defined.

Adding, replacing, muting, or removing a framework mapping does not alter the Proof Protocol architecture, evidence model, Proof of Efficacy determination, ProofBundle™, ProofStamp™, ProofRegister™, or independent corroboration requirements.

A framework mapping therefore establishes **interoperability**, not architectural dependency.

## 9. Relationship to Proof Protocol

This mapping is part of the Proof Protocol specification family maintained by Nebulonium, Inc.

The relationship is intentionally asymmetric:

> **DORA supplies legal obligations for the digital operational resilience of financial entities. Proof Protocol supplies the evidence model for independently examining whether a selected ICT control or resilience measure performed as claimed.**

No affiliation, endorsement, certification, or sponsorship by the European Union, the European Commission, the European Supervisory Authorities, or any competent authority is implied.

## 10. Source Framework, Attribution, and License

DORA and its delegated and implementing regulations are public law of the European Union. The authoritative source is EUR-Lex, the official website of EU law:

- Regulation (EU) 2022/2554: https://eur-lex.europa.eu/eli/reg/2022/2554/oj/eng
- Delegated and implementing acts: https://eur-lex.europa.eu (search by instrument number)

Only the versions published in the Official Journal of the European Union are authentic and legally binding. Consolidated texts on EUR-Lex are documentation tools. Implementation status: DORA applies from 17 January 2025 (Article 64). Amendments to DORA have been proposed by the European Commission as part of its digital simplification initiatives; their adoption status as of October 8, 2026 was not confirmed for this draft and SHOULD be checked on EUR-Lex before use.

EU reuse policy: the European Commission's reuse policy is implemented by Commission Decision 2011/833/EU of 12 December 2011 on the reuse of Commission documents. The Commission states that, unless otherwise indicated, content owned by the EU on its website is licensed under CC BY 4.0, which means "reuse is allowed, provided appropriate credit is given and changes are indicated" (https://commission.europa.eu/legal-notice_en). Trade marks, logos, and emblems are excluded from that reuse policy. The specific notice for EUR-Lex content is at https://eur-lex.europa.eu/content/legal-notice/legal-notice.html and SHOULD be checked before any reproduction of EUR-Lex text.

This Proof Protocol mapping is independently authored and licensed under **CC BY 4.0**. That license applies only to original Proof Protocol material in this repository. It does not relicense external standards, regulations, criteria, frameworks, or trademarks.

Where upstream material is copyrighted or access-controlled, contributors MUST NOT copy protected normative text into this repository merely to make the mapping self-contained. Reference identifiers and independently authored descriptions should be used where legally appropriate.

### Required attribution

EU legislation does not impose a specific notice for citation by instrument number and article. Reuse of EU-owned content requires appropriate credit and indication of changes. The recommended attribution line used in this repository is:

> Source: EUR-Lex, https://eur-lex.europa.eu, © European Union. Regulation (EU) 2022/2554 (Digital Operational Resilience Act), OJ of 27 December 2022, and related Commission delegated and implementing regulations. Reused under Commission Decision 2011/833/EU. Only the Official Journal versions are authentic.

What this specification reproduces: instrument titles and numbers, chapter-level structural terms, dates, and short factual statements. It does not reproduce article text, recitals, or annex content. Any future inclusion of EUR-Lex text MUST credit the source and indicate changes.

## 11. Versioning

This mapping is versioned independently of DORA. Material upstream changes SHOULD trigger a mapping review and, where necessary, a new version identifying the upstream revision mapped. This version maps Regulation (EU) 2022/2554 as applicable from 17 January 2025 and the delegated and implementing regulations listed in section 1.

---

*Proof Protocol · proofprotocol.io · CC BY 4.0*
