---
address: c-000002
type: concept
title: Brain v2 Mission Control
status: evergreen
created: 2026-09-18
updated: 2026-09-18
tags:
  - brain-v2
  - mission-control
  - architecture
  - provenance
  - retrieval
---

# Brain v2 Mission Control

The shared Markdown vault is the canonical learning source. Mission Control consumes the governed Brain v2 graph rather than treating visual proximity, lexical suggestions, or decorative motion as knowledge.

## Governed graph

`GET /api/brain/v2/graph` exposes evidence-backed nodes and edges. Allowed relationships come from explicit wiki links, source-backed claims, completed transaction artifacts, recorded handoffs, retrieval records, task ownership, or explicit skill-use records. Suggestions remain outside the governed graph until reviewed and promoted.

## Mission Control surfaces

Mission Control v2 remains available at `/mission/` while v1 remains the default at `/`. Command, Flows, Brain, Projects, and Orchestration lenses share the existing runtime, vault, and APIs. Output review, incident handling, and reversible session hiding preserve original files and session history.

Sanitized session chat is operational evidence. It does not automatically become knowledge. Installed, enabled, loaded, authenticated, connected, invoked, and verified remain separate states.

## Retrieval-first task routing

Every dashboard-run Swarm task performs local BM25 retrieval before execution. The prompt receives at most three governed excerpts and instructs the agent to use that bounded packet first. Broader files or history are loaded only when the packet is insufficient.

Retrieval failure is explicit and fail-open. Provenance stores the task and query hashes, identifiers, and selected page paths, never raw task text, query text, credentials, or secret values.

## Live updates

Runtime telemetry and governed graph changes are published through the existing local polling and SSE channels. Brain updates do not introduce extra model polling.

## Write boundary

Inbox capture is create-only. Canonical capture and promotion require reviewed transactions and exact approval hashes. The legacy `/api/brain` read remains a compatibility source until a separately approved cutover.

## Obsidian

Obsidian is optional. Storage, wiki links, local retrieval, transactions, and dashboard visualization operate on ordinary local Markdown and Brain v2 APIs.

## Related

- [[Nexus]]
- [[NJ-Collision-Shop-Automation]]
