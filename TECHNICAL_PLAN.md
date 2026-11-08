# FabQuote - technical plan

**Planning document, not an implementation report.**

## Product objective

Explainable geometry and machine-time estimates, with no billing or customer account system.

## Intended system boundary

- **Input:** Fictional CAD drawings and invented standard rates.
- **Processing stages:** SVG/DXF geometry readers; Primitive normalizer and metrics layer; Parameter-based time/cost estimator; CLI output and example drawings.
- **Output:** A test drawing yields explainable dimensions and time estimates.
- **Runtime / build stack (tentative):** Python 3.12+, ezdxf, Shapely, Typer, pytest; optional static web UI
- **Explicitly excluded:** Invoicing, bookkeeping, processing real customer financial records, or executing manufacturing machines.

## Functional modules

- Read SVG/DXF geometry and flag unsupported primitives
- Calculate total cut length, pierce counts, and bounding dimensions
- Estimate machine effort using editable, generic process assumptions
- Compare sheet material utilization and operation time
- Export line-by-line assumptions and scenario-based cost estimates

## Demonstration and acceptance cases

**Test 1:** Estimate total cut length of a fictional bracket

**Test 2:** Show impact of changed machine feed rate

**Test 3:** Reject an unsupported geometry operation with a clear warning

## Safety, privacy, and provenance

1. Keep example datasets fictional, self-created, or appropriately licensed.
2. Run locally for the initial prototype; do not collect data on actual third parties.
3. Document origin and versions of external specifications and dependencies.
4. Exclude production credentials; put environment variable *names* only in `.env.example` if required later.
5. Do not make certification, legal compliance, professional safety, or performance guarantees without independent validation.

## Engineering unknowns and constraints

Estimated time is not a quote guarantee; fit for purpose depends on equipment calibration.

## Release definition

A first release requires a runnable prototype, verified README instructions, automated tests tied to the three demonstrations, the full LICENSE file, and an honest public GitHub development history. The roadmap estimates are hypotheses until reviewed during implementation.
