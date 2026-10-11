# Learning Objectives

> The discipline's learning objectives, by level. Novice, practitioner, expert.

The learning objectives are normative. A course that does not address the objectives is not a Source Engineering course; the objectives are the discipline's contract with the learner.

## Novice (after the 90-minute tutorial)

A novice can:

- **Define the discipline.** State the three principles, the COTS contract, and the hesitation factor.
- **Identify the five parts of a COTS.** Name the Inputs, Context, Decisions, Evidence, and Validation parts; explain the role of each.
- **Read a COTS in a high-stakes domain.** Walk through the five-part reading order; answer the four questions; escalate when the COTS is incomplete.
- **Run the e2e demonstration.** Clone the three repos, build them, produce a COTS, validate it, inspect it, cite it, and visualise it.

## Practitioner (after the curriculum)

A practitioner can additionally:

- **Map the data model to the COTS schema.** For every entity in `Source-Engineering/source-engineering-model/entities.md`, name the corresponding field in the COTS spec.
- **Produce a COTS for a domain.** Choose a domain; design a decision-type; produce a COTS; validate the COTS against the conformance suite.
- **Author a guardrail.** Identify a domain policy; write the guardrail in the discipline's DSL; test the guardrail against the conformance suite's fixtures.
- **Implement Layer 1.** Choose an implementation pattern (wrap an existing model API, build the model layer, or compose multiple model layers); implement Layer 1 in a new framework; pass the conformance test cases TC-L1-01..07.
- **Read a decision record as a regulator.** Walk the evidence chain; resolve the sources; inspect the audit history.

## Expert (after the case studies and the practice)

An expert can additionally:

- **Design a new decision-type.** Identify a domain with no existing decision-type; design the decision-type following the five-section template; submit the decision-type for review.
- **Author a blueprint.** Identify a layer composition that is not covered by an existing blueprint; design the blueprint following the v0.1 floor pattern; name the conformance test cases the blueprint introduces.
- **File a case study.** Run a protocol; collect the data; analyse the findings; file the case study following the template; record the implications for the discipline.
- **Roll out the discipline.** Run the four-stage adoption plan (Vocabulary, Reading, Authoring, Operating); measure the hesitation factor; record the case study.
- **Audit a decision record.** Walk the evidence chain; resolve the sources; inspect the audit history; file the audit record with the regulator.

## What this document is not

- **Not a curriculum.** The objectives are normative; the curriculum is the sequenced path. The objectives are the contract; the curriculum is the route.
- **Not a checklist.** The objectives are not "done" when the learner can check a box. The objectives are the learner's working knowledge; the learner can apply the knowledge to a new domain without the discipline's guidance.
- **Not a credential.** The objectives are not a certification. The discipline does not certify learners; the discipline's adoption is the credential.

## Related documents

- `curriculum.md` -- the curriculum (the path to the objectives).
- `tutorial-90-minutes.md` -- the 90-minute tutorial (the path to the novice level).