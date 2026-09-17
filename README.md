# Kenzie Reading

Incoming WGSSS-funded PhD researcher in Human Geography, working across spatial accessibility, public-transport data, open spatial data and reproducible spatial analysis.

I am particularly interested in the gap between **formal or modelled accessibility** and the access people can actually achieve in practice, and in building transparent analytical workflows that distinguish observed evidence, uncertainty and interpretation.

## Selected projects

### TfL Cycleway 6 Counterfactual Evaluation

A reproducible observational evaluation of cycling-volume changes associated with TfL Cycleway 6 section B.

The project tests how robust site-level estimates are to alternative counterfactual construction, pre-treatment fit, donor selection, spatial contamination and placebo diagnostics. It deliberately avoids collapsing heterogeneous site results into a single route-wide causal effect.

**Release:** `v1.0.0`

https://github.com/mackenziereading19/TfL-C6-Counterfactual-Evaluation

### NPT Active Travel Prioritisation Robustness Audit

A reproducible decision-support audit of public active-travel prioritisation evidence in Neath Port Talbot.

The project examines how far priority conclusions depend on policy-value weights, equity emphasis, public-transport deficit, road-safety evidence and normalisation choices, while keeping synthetic stress tests distinct from official policy methodology.

**Release:** `v1.0.0`

https://github.com/mackenziereading19/NPT-Active-Travel-Prioritisation-Robustness-Audit

### Environmental EO Evidence Reliability Audit

A bounded spatial-evidence audit testing whether a transparent Sentinel-2 vegetation signal is decision-ready for woodland screening, and what disagreement with mapped woodland evidence actually represents.

The project rejects weak classifier expansion where the limiting problem is semantic mismatch rather than model complexity, and explicitly separates evidence convergence from ecological ground truth.

**Release:** `v1.0.0`

https://github.com/mackenziereading19/Environmental-EO-Evidence-Reliability-Audit

### Ceredigion NaPTAN–OpenStreetMap Audit

An evidence-bounded comparison of NaPTAN public-transport records and relevant OpenStreetMap objects in Ceredigion.

The project combines deterministic identifier linkage, spatial candidate generation and evidential validation. It deliberately avoids treating either dataset as ground truth or converting automated discrepancies directly into OpenStreetMap edits.

https://github.com/mackenziereading19/ceredigion-naptan-osm-audit

## Open-source contributions

### MobilityData Mobility Feed API

**GTFS-RT location inheritance — PR #1811 — merged**

Fixes locationless GTFS-Realtime feeds failing to inherit location metadata from referenced static GTFS feeds, including preservation and deduplication behaviour.

https://github.com/MobilityData/mobility-feed-api/pull/1811

**GTFS-RT entity-type replacement semantics — PR #1822 — merged**

Fixes stale GTFS-RT entity types being retained when a later catalogue row narrows the advertised entity-type set, with bounded regression coverage that preserves existing blank-cell semantics.

https://github.com/MobilityData/mobility-feed-api/pull/1822

### MobilityData GTFS Validator

**Conditional `min_transfer_time` validation — PR #2175 — merged**

Adds validation for the conditionally required `transfers.min_transfer_time` field when `transfer_type = 2`, with focused regression coverage and reuse of the validator's existing required-field notice.

https://github.com/MobilityData/gtfs-validator/pull/2175

**Recommended `trip_headsign` validation — PR #2192 — merged**

Marks `trip_headsign` as a recommended GTFS field so feeds with the field present but empty emit the validator's existing missing-recommended-field notice, with focused regression coverage and real-feed acceptance testing.

https://github.com/MobilityData/gtfs-validator/pull/2192

### Transport for the North `caf.viz`

**XY plot data-column validation — PR #48 — merged**

Adds consistent validation for requested plotting columns before dispatch to the plotting backend, with regression tests across supported XY plot types.

https://github.com/Transport-for-the-North/caf.viz/pull/48

## Approach

Across these projects I try to use the same principles:

- establish feasibility before implementation;
- preserve and identify source evidence;
- prefer reproducible diagnostics to manual assumptions;
- distinguish discrepancies from confirmed errors;
- record uncertainty, limitations and negative findings;
- test changes against the smallest defensible claim;
- stop when additional complexity is not justified by the decision need.
