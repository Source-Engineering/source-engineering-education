# Source Engineering in 15 Minutes

> The adopter quickstart. By the end, you have a validated COTS on your machine and an Explorer page you can open in a browser. If you have 90 minutes instead, do `tutorial-90-minutes.md` after this.

## Prerequisites

- Node.js 20+.
- 15 minutes.

## Step 1 -- Get the tools (3 minutes)

```bash
git clone https://github.com/Source-Engineering/source-engineering-tools.git
cd source-engineering-tools
npm install
npm run build
```

## Step 2 -- Run the quickstart (2 minutes)

```bash
bash scripts/quickstart.sh
```

One command does four things: obtains a seed COTS (fetched from `source-engineering-reference-implementation`, falling back to the bundled `examples/legal-summarization.cots.json`), runs the quick conformance check (`validate` -> `PASS`), prints the `inspect` and `cite` summaries, and writes `seed.cots.explorer.html` in a fresh temp directory.

## Step 3 -- Open the Explorer page (2 minutes)

Open the printed `*.explorer.html` in a browser. You get four tabs: Reasoning Roadmap (sources -> claims -> decision), Context Graph (parameters, constraints, typed edges, RFC-0004), the text Summary, and the Audit Trail (RFC-0005). Click through them. That page is the discipline's demo-able surface: a response you can audit.

## Step 4 -- Validate with the full suite (3 minutes)

```bash
git clone https://github.com/Source-Engineering/source-engineering-conformance.git
cd source-engineering-conformance
npm install && npm run build
node dist/cli.js validate <path-to-seed.cots.json>
```

The full suite reports `PASS` with at most the two legacy warnings (TC-RC-05, TC-L4-05) on a pre-RFC-0002/0005 producer; the reference implementation's own examples carry the current fields.

## Step 5 -- Produce your own COTS (5 minutes)

```bash
git clone https://github.com/Source-Engineering/source-engineering-reference-implementation.git
cd source-engineering-reference-implementation
npm install && npm run build
npm run example:legal-summarization     # or: example:transaction-routing
node ../source-engineering-tools/dist/cli/se-trace.js explore examples/output/legal-summarization.cots.json -o ./out
```

You now have a COTS your own run produced, validated, and rendered.

## What you should take away

- A COTS is the response's auditable bundle: Inputs, Context, Decisions, Evidence, Validation.
- `se-trace` is the CLI surface: `validate`, `inspect`, `cite`, `visualize`, `context-graph`, `audit`, `recursive`, `explore`.
- The conformance suite is the gate: `se-conformance validate <cots>` must pass before a response ships.

## Next

- `tutorial-90-minutes.md` -- the full guided session.
- `curriculum.md` -- the six-plus-unit learning path.
- `Source-Engineering/source-engineering-foundations/docs/00-manifesto.md` -- the why.
