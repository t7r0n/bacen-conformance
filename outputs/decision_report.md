# Decision Report: Bacen Conformance

An open conformance test suite + idempotency/replay harness for Brazil's Pix and Open Finance APIs — written in Elixir to match Cumbuca's stack, vendor neutral on the surface, Cumbuca flavoured under the hood.

## Evidence-Grounded Findings

CLAIM: abstractions operator packet should `accept only if decision claims cite fixture evidence` because blocks=4 reviews=5 mean_severity=2.556. [EVID: ev_0011]
CLAIM: cumbuca evidence replay should `block release until cited evidence is regenerated` because blocks=4 reviews=5 mean_severity=2.611. [EVID: ev_0044]
CLAIM: proprietary regression harness should `open a regression issue with trace and benchmark delta` because blocks=3 reviews=5 mean_severity=2.528. [EVID: ev_0022]
CLAIM: wedge boundary probe should `route to reviewer with evidence packet` because blocks=3 reviews=4 mean_severity=2.528. [EVID: ev_0077]
