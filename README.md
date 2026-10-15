# Digital Characterisation and Reuse Screening of Mining Waste in Niger State

Pan-African MineTech Exploration Technology Pre-Incubation Programme 2026
Nasarawa State University Keffi Mine-Tech UniPod

Team: [Team name] Â· Materials and Metallurgical Engineering (3), Computer Engineering (1), Petroleum and Gas Engineering (1)
Contact: [name / email]

## The problem

Mining waste and tailings in Nigeria are rarely sampled, characterised or recorded. Without that data nobody can tell whether a waste dump is a contamination risk, a source of recoverable minerals, or a material that could be safely reused. Published research on chromium contamination in the Gutu mine spoil, Minna, Niger State shows the concern is real locally. Nigeria's critical minerals agenda treats legacy tailings as an untapped secondary resource, but that value cannot be assessed without reliable characterisation data.

## Our solution: a sample-to-decision workflow

1. Characterise. Sample waste from one accessible, authorised source in Niger State (for example the Gutu mine spoil area, Minna). Screen it with handheld XRF where available and confirm with laboratory testing, including leach testing for contaminants.
2. Register and flag. Every sample goes into a searchable registry (source, location, material, authorisation, results). Each sample gets screening flags: hazard, recovery potential, reuse candidate or insufficient data.
3. Prove one pathway. If a sample passes screening, cast small sample blocks and compare them with conventional control blocks for strength, durability and water absorption where facilities permit.

Safety principle: no material is assumed safe until tested.** A "reuse candidate" flag only means no screening exceedance was found. It is never a safety clearance.

## How this maps to the programme brief

| Brief bottleneck / theme | Our response |

| Secondary and non-conventional sources: characterise legacy mine tailings | Sampling and characterisation of legacy spoil / tailings |
| Fragmented legacy data | Searchable, standardised sample registry |
| Delayed field assaying | Handheld XRF screening with lab confirmation |
| Security and access constraints | One accessible, authorised site, engaged through the owner and local authorities |

## What exists today vs. what we will build

Working now (this repo): the sample registry prototype: sample registration, result entry (manual or CSV), screening-flag logic, search, CSV export, map view, and unit tests. A synthetic demo dataset is included so the workflow can be seen end to end.

To be done in the 10-week programme: site access and authorisation, field sampling, XRF and laboratory characterisation, replacing the placeholder flag thresholds with values from applicable guidance and our lab data, casting and testing sample blocks, and user feedback from small-scale miners, operators and regulators.

## Repository layout

```
app.py                   Streamlit interface
registry.py              Storage (SQLite) and screening-flag logic
config/flag_rules.json   Flag thresholds (PLACEHOLDERS, see warning inside)
data/demo/               Synthetic demo data
docs/data_schema.md      Tables, fields and flag logic
docs/workplan.md         Proposed 10-week plan
tests/                   Unit tests
```

## Limitations

- The shipped thresholds are placeholders, not regulatory limits.
- Handheld XRF gives total elemental content. It does not show leachability and cannot measure lithium or other light elements, so laboratory confirmation is part of the plan.
- The registry is a single-user prototype with no authentication.
- Nothing here has been field-tested yet.

## Research basis

Environmental Risk Assessment of Chromium Contamination in Gutu Mine Spoil, Minna, Niger State, Nigeria, UMYU Journal of Pure and Industrial Chemical Research. This gives a local research lead. It does not establish that any material we select is suitable for reuse.

