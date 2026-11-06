# Conceptual Product Architecture

Crystal Flip is a closed-source product. This page describes its public-facing components and data flow without disclosing implementation details, infrastructure locations, proprietary algorithms, or credentials.

## High-Level Flow

```text
Supported launch platforms ─┐
                            ├─> Continuous collection ─> Historical entity profiles ─┐
Public social activity ─────┘          │                                             │
                                       └─> Real-time normalization and filtering ────┼─> Desktop application
                                                                                     │    └─> Review / auto-open
User lists and thresholds ───────────────────────────────────────────────────────────┘

Historical profiles ───────────────────────────────────────────────────────────────> Crystal Extension
```

## Components

### 1. Market and Social Inputs

Crystal Flip processes publicly available information from supported token-launch venues, blockchain networks, and Twitter-related sources. The exact integrations and coverage can change as external services evolve.

### 2. Continuous Collection

Server-side collectors operate around the clock to associate launches with developers, tweet authors, and Community admins. Their results are accumulated into reusable historical profiles.

This architecture removes the need for every user to build an independent database of recurring participants.

### 3. Entity History and Caching

Recurring developers and social accounts are cached with relevant launch outcomes. When a new token appears, the platform can retrieve existing context instead of reconstructing the participant's history from scratch.

### 4. Detection and Filtering

Incoming launches are evaluated against user settings, including migration, wallet, follower, keyword, liquidity, trust, and score thresholds. Blacklists, whitelists, and duplicate suppression reduce unwanted or repeated results.

### 5. Scoring and Risk Signals

Supported signals are combined into analytical views such as Crystal AI Score, behavioral profiles, and risk warnings. Proprietary model details are not part of this documentation.

### 6. Desktop Workspace

The desktop application presents detections, history, notes, configuration, and automatic-opening controls. It is the primary control center for active monitoring.

### 7. Crystal Extension

The extension enriches supported web interfaces with cached historical context and user-defined visual highlighting. It complements rather than replaces the main analytics platform.

### 8. Telegram Control Panel

The official Telegram bot handles access, subscription management, application delivery or reinstallation, and customer support.

## Design Goals

- **Low-latency discovery:** surface launches while their context is still actionable.
- **Historical continuity:** compare recurring participants across launches.
- **Configurable relevance:** let users reduce noise using their own strategy.
- **Explainable context:** expose the underlying factors behind detections and scores.
- **Separation of concerns:** continuous collection, user workflow, and access management are distinct product components.

## Repository Boundary

This repository is a public product-documentation space. It intentionally excludes:

- application and server source code;
- private API credentials and access tokens;
- proprietary scoring weights and internal algorithms;
- customer lists, payment records, and private community content;
- unreleased security-sensitive operational details.
