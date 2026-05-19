# Decision Report: Bacen Conformance

An open conformance test suite + idempotency/replay harness for Brazil's Pix and Open Finance APIs - written in Elixir to match Cumbuca's stack, vendor neutral on the surface, Cumbuca flavoured under the hood.

## Evidence-Grounded Findings

CLAIM: abstractions policy boundary should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=1.708. [EVID: ev_0033]
CLAIM: cumbuca drift should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=2.5. [EVID: ev_0088]
CLAIM: cumbuca evidence recall should `block release until replay is understood` because blocks=3 reviews=3 mean_severity=1.875. [EVID: ev_0132]
CLAIM: proprietary failure replay should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=3.333. [EVID: ev_0044]
CLAIM: wedge gap should `block release until replay is understood` because blocks=3 reviews=2 mean_severity=3.333. [EVID: ev_0077]
CLAIM: wedge reviewer handoff should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=2.583. [EVID: ev_0121]
