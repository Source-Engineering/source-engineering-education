# Source Engineering Curriculum

> The discipline's growth path. Five units, sequenced.

The curriculum is for the reader who has decided the discipline is worth their time and wants to learn it properly. The path is sequenced; the reader does not skip units. The path is not a race; the reader can spend a week or a quarter on each unit.

## Unit 1 -- Foundations (1 week)

**Question.** What is the discipline? What is the COTS? What is the hesitation factor? What is the judgment gap?

**Reading.**

- `Source-Engineering/source-engineering-foundations/docs/00-manifesto.md` -- the manifesto.
- `Source-Engineering/source-engineering-foundations/docs/05-positioning.md` -- the positioning matrix.
- `Source-Engineering/source-engineering-foundations/terminology.md` -- the working vocabulary.

**Assignment.** Write a one-page note that answers the four questions above in your own words. Submit the note for review.

**Exit criterion.** You can define COTS, source universe, evidence chain, decision record, hesitation factor, and judgment gap.

## Unit 2 -- Model (1 week)

**Question.** What does the discipline think about? What are the five stages? What are the integrity questions?

**Reading.**

- `Source-Engineering/source-engineering-model/model.md` -- the conceptual model.
- `Source-Engineering/source-engineering-model/entities.md` -- the data model.
- `Source-Engineering/source-engineering-model/integrity-questions.md` -- the integrity questions.

**Assignment.** Walk through the data model. For each entity, find the corresponding field in the COTS spec (`Source-Engineering/source-engineering-specifications/cots/README.md`). Submit the mapping.

**Exit criterion.** You can map every entity in the data model to a field in the COTS spec.

## Unit 3 -- Specifications (1 week)

**Question.** What does the discipline require? What is the COTS schema? What is the versioning policy? What are the decision-types?

**Reading.**

- `Source-Engineering/source-engineering-specifications/cots/README.md` -- the COTS spec.
- `Source-Engineering/source-engineering-specifications/versioning.md` -- the versioning policy.
- `Source-Engineering/source-engineering-specifications/compatibility.md` -- the compatibility guarantees.
- `Source-Engineering/source-engineering-specifications/decision-types/` -- the decision-types registry.

**Assignment.** Produce a COTS for a domain you know well. Validate the COTS against the conformance suite.

**Exit criterion.** You can produce a COTS that passes the conformance suite.

## Unit 4 -- Architecture (1 week)

**Question.** How does the discipline compose? What are the four layers? What is the pillar x layer matrix? What is a blueprint?

**Reading.**

- `Source-Engineering/source-engineering-architecture/four-layer-stack.md` -- the reference architecture.
- `Source-Engineering/source-engineering-architecture/pillar-x-layer-matrix.md` -- the 5x4 mapping.
- `Source-Engineering/source-engineering-architecture/layer-contracts/` -- the per-layer interface contracts.
- `Source-Engineering/source-engineering-architecture/blueprints/v0.1/README.md` -- the first blueprint.

**Assignment.** Read the conformance test cases in `Source-Engineering/source-engineering-conformance/`. For each test case, name the layer the test case exercises.

**Exit criterion.** You can map every conformance test case to a layer.

## Unit 5 -- Demonstrate (1 week)

**Question.** How does the discipline run? What is the reference implementation? What is the `se-trace` CLI? How do I produce, validate, and visualise a COTS end-to-end?

**Reading.**

- `Source-Engineering/source-engineering-reference-implementation/` -- the reference implementation.
- `Source-Engineering/source-engineering-conformance/` -- the conformance suite.
- `Source-Engineering/source-engineering-tools/` -- the `se-trace` CLI.
- `tutorial-90-minutes.md` -- the 90-minute tutorial.

**Assignment.** Follow the 90-minute tutorial. Produce a COTS, validate it, and visualise it. Submit the resulting HTML page.

**Exit criterion.** You have run the e2e demonstration.

## Unit 6 -- Recursive Evidence Chains (half week)

**Question.** What happens when the evidence is itself a model output? How does a COTS avoid citing itself? What are `source_type` and `chain_termination`, and how does a reviewer read them?

**Reading.**

- RFC-0002 (recursive evidence chains) in `Source-Engineering/source-engineering-governance/RFC/0002-recursive-evidence-chains.md`.
- `Source-Engineering/source-engineering-specifications/cots/README.md` -- Part 4, the RFC-0002 fields (COTS schema v1.2.0).
- `Source-Engineering/source-engineering-practice/handbook/10-recursive-evidence-chains.md` -- how a reviewer reads a COTS with recursive evidence.
- The 2026 legal-summarization case study's Q3.2 finding in `Source-Engineering/source-engineering-case-studies/2026-legal-summarization/` -- where the problem surfaced.

**Assignment.** Take a conformant COTS. Mark one evidence item `model-generated`, declare `bounded_recursion` with a bound of 1, and run the conformance suite: observe the `recursive-evidence` warning (TC-RC-01). Then declare `terminal` and observe the failure (TC-RC-04). Run `se-trace recursive` on both. Write a short note: under which policy would you accept each COTS, and why?

**Exit criterion.** You can explain why a structurally valid COTS can still cite itself, and how the RFC-0002 fields make that visible to a reviewer.

## Beyond the curriculum

The curriculum is the discipline's growth path. Beyond the curriculum, the reader joins the discipline's community: the case studies, the practice handbook, the open questions, the RFCs, and the ADRs. The community is where the discipline grows; the curriculum is where the reader joins it.

## Related documents

- `tutorial-90-minutes.md` -- the 90-minute tutorial. A single guided session.
- `learning-objectives.md` -- the discipline's learning objectives, by level.