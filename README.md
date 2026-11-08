# FabQuote

> Geometry-based manufacturing effort estimation for small shops.

**Current state:** Documentation starter / proposed product. The presence of this README does **not** mean the software has been implemented, deployed, used. Update this status to reflect real work.

## What it is

FabQuote is a proposed specialist software tool for Laser-cutting shops, local CNC subcontractors, and prototyping makerspaces. Estimating cutting effort from drawings is tedious and inconsistent when performed by hand. The intended differentiation is: Explainable geometry and machine-time estimates, with no billing or customer account system.

## Intended users and use cases

- Estimate total cut length of a fictional bracket
- Show impact of changed machine feed rate
- Reject an unsupported geometry operation with a clear warning

## Planned features

- Read SVG/DXF geometry and flag unsupported primitives
- Calculate total cut length, pierce counts, and bounding dimensions
- Estimate machine effort using editable, generic process assumptions
- Compare sheet material utilization and operation time
- Export line-by-line assumptions and scenario-based cost estimates

## Proposed technology

Python 3.12+, ezdxf, Shapely, Typer, pytest; optional static web UI

These technologies are *planned*, not a claim that dependencies have already been installed or code has been written. Revise this section when actual implementation decisions are made.

## Proposed architecture

- SVG/DXF geometry readers
- Primitive normalizer and metrics layer
- Parameter-based time/cost estimator
- CLI output and example drawings

See [TECHNICAL_PLAN.md](TECHNICAL_PLAN.md) for technical boundaries and acceptance tests.

## Running locally

**Not yet runnable.** This package contains documentation templates, not software. When a functioning implementation is available, replace this paragraph with tested prerequisites, install instructions, a verified executable command, and a reproducible example using `Fictional CAD drawings and invented standard rates.`

## Data boundaries and exclusions

Invoicing, bookkeeping, processing real customer financial records, or executing manufacturing machines. All public examples should use Fictional CAD drawings and invented standard rates.

## Known limitations / validation risks

Estimated time is not a quote guarantee; fit for purpose depends on equipment calibration.

## Development roadmap

Work is broken into estimated, not-yet-completed milestones in [ROADMAP.md](ROADMAP.md). They are *planning estimates*, not an assertion that development has begun or that work will definitely be performed.

## Business direction

Potential commercial extensions: Professional machine parameter libraries and CAD integrations. 
## Contributing and licensing

License: [Mozilla Public License 2.0](LICENSE) (`MPL-2.0`). The distribution contains the complete license text. Any future source files can include the SPDX identifier `MPL-2.0` and the Exhibit A notice where appropriate. Rights in contributions and project ownership must be verified before licensing.

