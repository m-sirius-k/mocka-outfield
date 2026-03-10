# MoCKA Outfield

MoCKA Outfield is the public interface layer of the MoCKA system.

It exposes sanitized knowledge, public events, and collaboration
interfaces for external AI systems and researchers.

## Structure

ledger
Public event history derived from infield events.

knowledge
Public documentation, maps, and research artifacts.

governance
Rules and constitutional definitions of the outfield.

interfaces
Export endpoints for external services.

orchestra
Shared coordination context for multi-agent systems.

## Boundary

Infield contains internal reasoning and experiments.  
Outfield contains only sanitized and shareable artifacts.

Event history is the single source of truth.

