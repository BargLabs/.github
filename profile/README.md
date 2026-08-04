# Barg Labs Inc.

Vancouver, British Columbia · [barglabs.ai](https://barglabs.ai) · [cejel.dev](https://cejel.dev)

We build **Cejel** — a deterministic, offline trust certificate for source code.

Point it at a repository and it scores eleven criteria against a published rubric, binds every
criterion to a specific file, line and content hash, and issues a certificate. No network call,
no model call, no telemetry, and it never uploads source. When the recognised source is too thin
to support a verdict it returns `insufficient_source` and declines to score rather than guessing.

There is no AI in Cejel. Same repository, same revision, same release, same rubric — same result,
byte for byte. That is what makes the output evidence rather than opinion.

## Measured

Rubric `witan-rubric-v17-2026-07-24`, decision date 25 July 2026, on a preregistered 200-repository
holdout the scanner had never run against. Thresholds locked 22 July, before any result was visible.
Three independent blind reviews.

- Finding precision **96.43%** (95% lower bound 94.16%)
- Worst-case false-positive rate **0.66%** (95% upper bound 1.10%)
- Rubric-agreement recall **95.64%** (lower bound 92.23%)

Rubric-agreement recall measures agreement with blind reviewers on the same bounded evidence. It is
**not** detection recall — it does not mean Cejel finds 95.64% of real defects. No detection-recall
figure is published. This is finding-level calibration of one rule set on one population: not a
security guarantee, not vulnerability detection.

## We publish results that hurt us

The run before the passing one was a terminal no-go, published in full, failing on inappropriate
abstention at 12.70% against a 10% cap. A separate free LLM pack sits at 0.0 recall against a 0.65
floor — zero of thirty-four known defects found, three findings all false positives — published with
the root cause named as a detector-architecture failure.

Our public leaderboard scores 24 repositories including our own, which sits mid-table at 2.8/4.0.
We dogfood our own tools before we ask anyone else to run them.

## Install

npx @cejel/cejel .


Also available as signed binaries, a container image, a GitHub Action, a Homebrew tap, and on the
MCP Registry. AGPL-3.0.
