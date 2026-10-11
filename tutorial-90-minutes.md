# Source Engineering in 90 Minutes

> A single guided session. By the end, you will have produced, validated, and visualised a COTS.

This tutorial is the discipline's elevator pitch. In 90 minutes, you go from "I have never heard of Source Engineering" to "I have a working COTS that the conformance suite accepts". The tutorial is hands-on; you follow the steps, you run the commands, you produce the artefact.

## Prerequisites

- A computer with Node.js 20+ and git installed.
- A GitHub account.
- 90 minutes.

## Step 1 -- Read the manifesto (10 minutes)

Open `Source-Engineering/source-engineering-foundations/docs/00-manifesto.md` in your browser. Read the manifesto. Skim the principles. Skim the COTS contract. Skim the open questions.

What you should take away: the discipline's three principles, the COTS contract, and the open questions.

## Step 2 -- Clone the three repos (5 minutes)

```bash
git clone https://github.com/Source-Engineering/source-engineering-conformance.git
git clone https://github.com/Source-Engineering/source-engineering-reference-implementation.git
git clone https://github.com/Source-Engineering/source-engineering-tools.git
```

You now have three repos on your machine.

## Step 3 -- Build the reference implementation (10 minutes)

```bash
cd source-engineering-reference-implementation
npm install
npm run build
```

This builds the reference implementation, including the two seeded decision-types and the mock model adapter.

## Step 4 -- Produce a COTS (10 minutes)

```bash
node dist/examples/legal-summarization.js
```

This produces a COTS at `examples/output/legal-summarization.cots.json`. The COTS is the discipline's headline artefact. Open the file; you will see the five parts (Inputs, Context, Decisions, Evidence, Validation).

## Step 5 -- Build the conformance suite (10 minutes)

```bash
cd ../source-engineering-conformance
npm install
npm run build
```

This builds the conformance suite.

## Step 6 -- Validate the COTS (5 minutes)

```bash
node dist/cli.js validate ../source-engineering-reference-implementation/examples/output/legal-summarization.cots.json
```

Expected output:

```
Status: PASS
Errors: 0
Warnings: 0
```

The COTS is conformant. The discipline's gate is open.

## Step 7 -- Build the tools (10 minutes)

```bash
cd ../source-engineering-tools
npm install
npm run build
```

This builds the `se-trace` CLI.

## Step 8 -- Inspect the COTS (5 minutes)

```bash
node dist/cli/se-trace.js inspect ../source-engineering-reference-implementation/examples/output/legal-summarization.cots.json
```

Expected output: a human-readable summary of the COTS. You see the source universe, the context, the decision, the evidence chain, and the feedback surfaces.

## Step 9 -- Cite the decision (5 minutes)

```bash
DECID=$(node -e "console.log(require('../source-engineering-reference-implementation/examples/output/legal-summarization.cots.json').decisions[0].id)")
node dist/cli/se-trace.js cite ../source-engineering-reference-implementation/examples/output/legal-summarization.cots.json "$DECID"
```

Expected output: the evidence chain for the specific decision. You see the supporting evidence, the contradicting evidence, and the uncertainty.

## Step 10 -- Visualise the COTS (5 minutes)

```bash
mkdir -p ./out
node dist/cli/se-trace.js visualize ../source-engineering-reference-implementation/examples/output/legal-summarization.cots.json -o ./out
```

Expected output: two files in `./out` -- a Mermaid source file and a self-contained HTML page. Open the HTML in a browser; you see the Reasoning Roadmap -- a graph that shows the sources, the claims, and the decision.

## What you have done

In 90 minutes, you have:

- Read the manifesto.
- Cloned three repos.
- Built the reference implementation, the conformance suite, and the tools.
- Produced a COTS.
- Validated the COTS against the conformance suite.
- Inspected the COTS.
- Cited the decision.
- Visualised the COTS as a Reasoning Roadmap.

You have run the discipline end to end. The COTS is real; the validation is real; the visual is real.

## What to do next

- **Read the curriculum.** `curriculum.md` is the discipline's growth path; the 90-minute tutorial is the first unit's first assignment.
- **Read the practice handbook.** `Source-Engineering/source-engineering-practice/handbook/` is the discipline's adoption surface.
- **Read the case study.** `Source-Engineering/source-engineering-case-studies/2026-legal-summarization/` is the discipline's first empirical artefact.

## Related documents

- `curriculum.md` -- the discipline's growth path.
- `learning-objectives.md` -- the discipline's learning objectives.