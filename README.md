# RiskLink Lite

**RiskLink Lite** is a lightweight account risk intelligence framework for Roblox games.

It helps developers identify suspicious account patterns using configurable server-side signals, trust profiles, moderation recommendations, safelist support, event hooks, moderation feeds, in-memory review queues, and clean public APIs.

RiskLink Lite is built to be:

- **lightweight**
- **modular**
- **easy to configure**
- **easy to integrate**
- **moderation-friendly**
- **safe by default**
- **ready for future admin integration**

> RiskLink Lite does **not** claim guaranteed alt detection.  
> It is designed as a **moderation intelligence** and **account risk scoring** framework to help developers and staff make better decisions.

---

## Features

RiskLink Lite currently includes:

- **Account risk scoring**
- **Trust profile system**
- **Config-driven recommendations**
- **Safelist / protected user support**
- **Risk tags**
- **Display summary output**
- **Clear logs and signal breakdowns**
- **Player attributes**
- **Risk changed event hook**
- **Manual reevaluation API**
- **Dedicated moderation feed**
- **In-memory suspicious player queue**
- **Review queue and high-risk queue**
- **Moderation snapshots**
- **Policy foundation**
- **Webhook-ready placeholder support**
- **Lightweight server-side architecture**

---

## Included Lite Signals

The Lite version currently includes:

- **AccountAge**
- **JoinBurst**
- **Behavior** (Quick Rejoin)
- **NamePattern**
- **Avatar** *(disabled placeholder in Lite)*

---

## Why Use RiskLink Lite?

RiskLink Lite gives developers more than just a number.

Each evaluated player can provide:

- a **numeric risk score**
- a **risk label**
- a **trust profile**
- a **recommendation**
- a **review suggestion state**
- a set of **risk tags**
- a **display summary**
- a detailed **signal breakdown**
- **player attributes**
- **moderation queue presence**
- **feed event output**

This makes RiskLink Lite useful for:

- **roleplay games**
- **moderation-heavy communities**
- **public games vulnerable to suspicious account waves**
- **future staff panel integration**
- **future admin ecosystem integration**

---

## Moderation Intelligence Features

RiskLink Lite supports more than just Output logging.

It can maintain:

- a **flagged player queue**
- a **review queue**
- a **high-risk queue**
- **moderation feed history**
- **moderation snapshots** for dashboards or future staff tools

This makes it much more practical for larger games that cannot manually watch Output all the time.

---

## Example Output
```
[RiskLink] RiskLink Lite v1.0.0 | devfunk1e scored 0 (Low Risk) | Trust=Trusted | Recommendation=No Action
[RiskLink] RiskLink Lite v1.0.0 | - AccountAge: +0 (Account age normal)
[RiskLink] RiskLink Lite v1.0.0 | - Avatar: +0 (Disabled)
[RiskLink] RiskLink Lite v1.0.0 | - JoinBurst: +0 (No suspicious join burst)
[RiskLink] RiskLink Lite v1.0.0 | - Behavior: +0 (No suspicious session behavior)
[RiskLink] RiskLink Lite v1.0.0 | - NamePattern: +0 (No suspicious name pattern)
```
---

## Player Attributes

RiskLink Lite automatically sets these attributes on evaluated players:

- `RiskLinkScore`
- `RiskLinkLabel`
- `RiskLinkTrustProfile`
- `RiskLinkRecommendation`
- `RiskLinkReviewSuggested`
- `RiskLinkSafeListed`

These attributes make integration easier for developers who want quick access through scripts or directly in Studio.

---

## Core Use Cases

RiskLink Lite is useful for:

- flagging suspicious account joins
- highlighting players who need staff review
- separating trusted, low-trust, and high-risk users
- feeding data into moderation systems
- building future admin interfaces
- integrating into account-sensitive systems such as **trading**, **gifting**, or **staff review workflows**

---

## Documentation

Additional documentation can be found in the `/docs` folder:

- [Installation Guide](docs/installation.md)
- [API Reference](docs/api.md)
- [Configuration Guide](docs/configuration.md)
- [Roadmap](docs/roadmap.md)
- [FAQ](docs/faq.md)

---

## Product Philosophy

RiskLink Lite is intentionally conservative.

- It does **not** auto-ban by default
- It does **not** pretend to perfectly identify alternate accounts
- It is designed to provide **useful moderation intelligence**
- It is meant to support developer workflows, **not replace moderation judgment**

---

## Current Version

Current version: **v1.0.0**

See [CHANGELOG.md](CHANGELOG.md) for release history.

---

## Future Direction

RiskLink Lite is intended to become part of a broader Roblox moderation and security ecosystem.

Planned future expansions include:

- **RiskLink Pro**
- **admin integration**
- **stronger behavioral correlation**
- **moderation adapters**
- **staff tools**
- **webhook/logging extensions**
- **trust history systems**
- compatibility with future **anti-cheat** and **admin** frameworks

---

## License / Usage

**RiskLink Lite** is free to use in Roblox projects.

Developers are allowed to:
- use RiskLink Lite in their own games
- modify it for their own projects
- integrate it into their own moderation workflows

RiskLink Lite may not be re-sold, re-uploaded as a paid product, or falsely claimed as another developer’s work.

Any future **paid / premium** RiskLink products, including locked or expanded versions, are separate commercial products and are **not included** under the free RiskLink Lite release.
