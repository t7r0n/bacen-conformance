# Bacen Conformance

An open conformance test suite + idempotency/replay harness for Brazil's Pix and Open Finance APIs - written in Elixir to match Cumbuca's stack, vendor neutral on the surface, Cumbuca flavoured under the hood.

## Why This Exists

Cumbuca's wedge is "no proprietary abstractions - code against the official Bacen and Open Finance specs." That is beautiful engineering taste but it has a cruel side effect: the official specs are vast, change frequently, and the failure modes (timeouts, idempotency, divergent participant behaviour at Itau vs. Bradesco vs. Nubank) are not in the spec at all.

## What It Builds

- Replays synthetic `cumbuca` and `wedge` cases against the project's evidence rules.
- Scores `cumbuca_coverage`, `wedge_risk`, and `proprietary_precision` so regressions are visible in CSV and JSON.
- Plants `cumbuca drift` and `wedge gap` failures as negative controls.
- Writes citation-locked decision claims; unsupported claims fail verification.
- Exports a review dashboard and demo pack for `bacen-conformance` without hosted services.

## Local Run

```bash
uv sync
uv run bacen-conformance all
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/analysis.json`
- `outputs/scenario_report.csv`
- `outputs/decision_report.md`
- `outputs/evidence_packet.md`
- `outputs/domain_rubric.json`
- `outputs/failure_matrix.md`
- `outputs/trace_graph.mmd`
- `outputs/dashboard.html`
- `outputs/demo_pack.zip`

## Sources

- https://www.businesswire.com/news/home/20251203797500/en/Cumbuca-Launches-Fast-Track-Payments-Initiation-Access-to-Brazils-Booming-Financial-Services-Market
- https://www.pymnts.com/news/international/latin-america/2025/global-fintechs-race-into-brazil-as-cumbuca-offers-a-new-back-door
- https://lsvp.com/company/cumbuca/
- https://pulse2.com/cumbuca-profile-daniel-ruhman-interview/amp/
- https://thefintechtimes.com/in-profile-cumbuca-ceo-daniel-ruhman/
- https://www.pismo.io/knowledge/cumbuca-business-case/
- https://github.com/appcumbuca
- https://github.com/appcumbuca/desafios
- https://www.ycombinator.com/launches/Oxa-cumbuca-the-first-proxy-for-the-brazilian-regulated-ecosystem

## Boundary

This repository uses synthetic fixtures only. It has no credentials, no customer data, no outreach data, and no dependency on a hosted API.
