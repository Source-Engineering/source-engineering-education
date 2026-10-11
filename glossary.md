# Student Glossary

> Student-friendly terms mapped to the discipline's canonical terms.

The discipline's canonical terms are in `Source-Engineering/source-engineering-foundations/terminology.md`. This glossary maps student-friendly terms to the canonical terms; the canonical terms are normative. The student-friendly terms are common English words that students may already know; the canonical terms are the discipline's vocabulary.

## A

**Answer** -> **DecisionRecord.** A COTS's persistent artefact that captures the decision.

**Audit** -> **Audit trail.** The persistent record of who saw what response, when, with what evidence, and what they did with it.

## B

**Backing** -> **Evidence.** The chain that supports a decision.

**Bookmark** -> **SourceArtifact id.** A COTS's reference to a specific source.

## C

**Chain** -> **Evidence chain.** The chain that links a decision back to its sources.

**Check** -> **Conformance test case.** A canonical test case in the discipline's conformance suite.

**Citation** -> **Provenance.** The chain that links an evidence item back to its source.

**Confession** -> **Audit history.** The append-only log of changes to a DecisionRecord.

## D

**Decision** -> **DecisionRecord.** The persistent artefact that captures a decision.

**Document** -> **SourceArtifact.** A discrete piece of content that can be cited as an input to a decision.

## E

**Evidence** -> **EvidenceItem + Provenance.** The chain that supports a decision.

**Explanation** -> **DecisionBasis + Evidence chain + Context.** The discipline's surface for explaining a decision.

## F

**File** -> **COTS file.** A JSON file that contains a COTS.

**Five-part structure** -> **The five parts of a COTS.** Inputs, Context, Decisions, Evidence, Validation.

## G

**Graph** -> **Reasoning Roadmap.** A Mermaid + HTML rendering of a COTS that shows the sources, the claims, and the decision.

## H

**Hesitation** -> **Hesitation factor.** The reluctance to act on a model's answer because the user cannot verify its reasoning in time.

## I

**Inspection** -> **The `se-trace inspect` command.** A CLI command that prints a human-readable summary of a COTS.

**Inputs** -> **The Inputs part of a COTS.** The source universe the model considered.

## J

**Judgment** -> **Judgment gap.** The gap between a structurally valid answer and the right answer.

## L

**Layer** -> **One of the four layers of the discipline's stack.** Typed Model, Runtime Validation, Business Guardrails, Audit Trail.

**Log** -> **Audit trail (operator-facing).** A COTS's audit trail is more than a log.

## M

**Manifesto** -> **The manifesto.** The discipline's canonical home, in `Source-Engineering/source-engineering-foundations/docs/00-manifesto.md`.

**Map** -> **Pillar x layer matrix.** The 5x4 mapping of the five pillars to the four layers.

**Model** -> **The conceptual model.** The five stages of every Source Engineering decision.

## P

**Pillar** -> **One of the five pillars.** Data Provenance, Contextual Signature Mapping, Chain of Evidence, Explainability Anchoring, Human Validation Points.

**Provenance** -> **Provenance.** The chain that links an evidence item back to its source.

## R

**Reasoning** -> **DecisionBasis.** The discipline's surface for explaining a decision.

**Reference** -> **SourceArtifact id.** A COTS's reference to a specific source.

**Review** -> **Audit.** A regulator's task. See `Source-Engineering/source-engineering-practice/handbook/07-auditing-a-decision-record.md`.

**Rule** -> **Guardrail rule.** A domain policy expressed in the discipline's guardrail DSL.

## S

**Schema** -> **JSON Schema.** The schema for the COTS, the decision-type, the question, the answer.

**Score** -> **Uncertainty.calibrated_score.** The model's stated uncertainty about an evidence item.

**Source** -> **SourceArtifact.** A discrete piece of content that can be cited.

**Spec** -> **Specification.** A normative technical requirement, in `Source-Engineering/source-engineering-specifications/`.

**Stack** -> **Four-layer stack.** The composition of the discipline into four named layers.

**Stamp** -> **SourceArtifact.version.content_hash.** A SHA-256 that uniquely identifies a specific state of a source.

## T

**Trace** -> **Audit trail (per-decision).** The append-only log of changes to a DecisionRecord.

**Type** -> **Decision-type.** A typed question with a declared answer shape.

## V

**Validation** -> **Validation.** The subset of a COTS that captures the feedback surfaces exposed back to the user.

**Version** -> **Version.** A specific state of a source artifact, addressed via content hash.

## W

**Wall** -> **The wall between the model and the user.** The COTS is the wall's window; the COTS is what the user can see.