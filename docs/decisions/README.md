# Architecture Decision Records (ADRs)

This directory contains the Architecture Decision Records (ADRs) for the
Ontology Test-Driven Development (OTDD) methodology.

An ADR records a significant architectural or methodological decision,
the context in which it was made, the alternatives considered, and the
rationale for the decision.

The ADRs document the evolution of OTDD itself. They are intended to
capture engineering knowledge so that future OTDD projects can build
upon previous experience rather than rediscovering the same decisions.

## Scope

These ADRs describe the OTDD methodology.

Project-specific decisions belong in the ADR directory of the individual
OTDD project (for example, the UAD 3.6 Validation project).

## ADR Index

| ADR  | Title                                              | Status     |
|------|----------------------------------------------------|------------|
| 0001 | UAD 3.6 as the First OTDD Reference Implementation | Draft      |

## Principles

The OTDD methodology is developed according to its own principles:

- Derivation, not divination.
- Meaning before implementation.
- Traceability over ceremony.
- Architectural decisions should be documented when they affect future engineering work.
- The methodology evolves through experience gained from reference implementations.

## Relationship to Reference Implementations

Reference implementation projects validate and refine the OTDD methodology.

As engineering experience accumulates, improvements to the methodology
are captured in this repository through additional ADRs.

Conversely, once an OTDD architectural decision becomes established, new
reference implementations should adopt that decision unless there is a
clear engineering reason to do otherwise.