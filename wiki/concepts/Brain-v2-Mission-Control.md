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
---

# Brain v2 Mission Control

The shared Markdown vault is the canonical learning source. Mission Control consumes the governed Brain v2 graph rather than treating visual proximity, lexical suggestions, or decorative motion as knowledge.

## Governed graph

`GET /api/brain/v2/graph` exposes evidence-backed nodes and edges. Allowed relationships come from explicit wiki links, source-backed claims, completed transaction artifacts, recorded handoffs, retrieval records, task ownership, or explicit skill-use records. Suggestions remain outside the governed graph until reviewed and promoted.

## Provenance and skill use

Task routing and retrieval store hashes and identifiers, not task text, query text, credentials, or secret values. A recommended skill remains unverified until an agent records it as invoked, verified, failed, or skipped.

## Write boundary

Inbox capture is create-only. Canonical capture and promotion require reviewed transactions and exact approval hashes. The legacy `/api/brain` read remains a compatibility source until the new Mission Control consumes the governed v2 graph.

## Obsidian

Obsidian is optional. Storage, wiki links, local retrieval, transactions, and dashboard visualization operate on ordinary local Markdown and Brain v2 APIs. Obsidian can later serve as another editor for the same files without becoming the runtime dependency.

## Related

- [[Nexus]]
