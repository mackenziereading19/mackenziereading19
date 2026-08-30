# Kenzie Reading

Geographer working across spatial accessibility, public-transport data, open spatial data and reproducible data analysis.

I am particularly interested in the gap between **formal or modelled accessibility** and the access people can actually achieve in practice, and in building transparent analytical workflows that distinguish observed evidence from interpretation.

## Selected projects

### Scottish NaPTAN Readiness Baseline

A reproducible technical baseline examining selected structural characteristics of a Scottish NaPTAN extract.

The analysis processed 50,893 StopPoint records and investigated the 16,275 records without supplied WGS84 coordinates. It found that all of those records retained British National Grid coordinates and could be transformed in the tested OSTN15-backed environment.

**Repository:**  
https://github.com/mackenziereading19/Scottish_NaPTAN_Readiness_Baseline

### Ceredigion NaPTAN–OpenStreetMap Audit

An evidence-bounded comparison of NaPTAN public-transport records and relevant OpenStreetMap objects in Ceredigion.

The project combines deterministic identifier linkage, spatial candidate generation and manual/evidential validation. It also provides an automated current-data acquisition route for independently rerunning the computational methodology while keeping the frozen historical audit evidence separate. It deliberately avoids treating either dataset as ground truth or converting automated discrepancies directly into OpenStreetMap edits.

**Repository:**  
https://github.com/mackenziereading19/ceredigion-naptan-osm-audit

## Open-source contributions

### MobilityData GTFS Validator

**Conditional `min_transfer_time` validation — PR #2175**

Adds validation for the conditionally required `transfers.min_transfer_time` field when `transfer_type = 2`, with focused regression coverage and reuse of the validator's existing required-field notice.

https://github.com/MobilityData/gtfs-validator/pull/2175

### MobilityData Mobility Feed API

**GTFS-RT location inheritance — PR #1811**

Fixes locationless GTFS-Realtime feeds failing to inherit location metadata from referenced static GTFS feeds, including preservation and deduplication behaviour.

https://github.com/MobilityData/mobility-feed-api/pull/1811

### MobilityData GBFS Validator

**Cross-feed vehicle-type reference validation — PR #218**

Adds validation that `vehicle_type_id` references resolve to vehicle types defined elsewhere in a GBFS feed across supported specification versions.

https://github.com/MobilityData/gbfs-validator/pull/218

### Transport for the North `caf.viz`

**XY plot data-column validation — PR #48**

Adds consistent validation for requested plotting columns before dispatch to the plotting backend, with regression tests across supported XY plot types.

https://github.com/Transport-for-the-North/caf.viz/pull/48

## Approach

Across these projects I try to use the same principles:

- establish feasibility before implementation;
- preserve and identify source evidence;
- prefer reproducible diagnostics to manual assumptions;
- distinguish discrepancies from confirmed errors;
- record limitations and negative findings;
- test changes against the smallest defensible claim.
