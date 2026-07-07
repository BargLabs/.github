## Barg Labs

Applied AI products for studios, markets, and regulated health systems — built around real
operating constraints: who's using the system, where the data lives, what has to be reviewed,
and what stays under human control.

Our product lines: **Alfred** (operator OS for AI-native studios), **Egbert** (B2B Fintech 3.0
infrastructure), and **Therasyn** (governance & on-prem infrastructure for clinical AI). More at
[barglabs.ai](https://barglabs.ai).

### Open source — Cejel

[**cejel**](https://github.com/BargLabs/cejel) is our free, offline trust certificate for any
codebase. It scores the engineering signals that tell you whether to trust a repo — tests,
secrets, isolation, claim-vs-reality, CI and audit discipline — and aggregates the scanners you
already run into one portable certificate.

```bash
npx cejel .
```

AGPL-3.0, deterministic, no network calls in the scoring path. Especially useful when AI wrote a
lot of the code — exactly when you can't eyeball trust.

### How we work

Product-led, not demo-led. Calm, verified, and in the open where it earns trust — we dogfood our
own tools before we ask anyone else to run them.
