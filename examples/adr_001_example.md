# ADR 001: API Versioning Strategy

- date: 2026-04-23
- status: accepted
- owner: platform-team
- tags: #type-adr #area-backend #status-active

## Context

Multiple clients need stable API contracts while product features evolve quickly.

## Decision

Adopt URI-based versioning for public APIs (/v1, /v2) and semantic change notes in release docs.

## Consequences

- better backward compatibility
- explicit migration path for clients
- small maintenance overhead for parallel versions
