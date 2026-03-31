# API Reference

This document describes the public API exposed by RiskLink Lite.

---

## Accessing the System

```
local RiskLink = require(game.ServerScriptService.RiskLink.init)
local system = RiskLink.Get()
```

---

## Startup

### `RiskLink.Start()`
Starts the RiskLink singleton if it is not already running.

### `RiskLink.Get()`
Returns the running RiskLink system instance.

### `RiskLink.ReevaluatePlayer(player)`
Convenience function for forcing a player reevaluation.

---

## Risk Queries

### `system:GetPlayerRisk(player)`
Returns the numeric risk score.

### `system:GetRiskLabel(player)`
Returns the risk label:
- `Low`
- `Medium`
- `High`

### `system:GetRiskBreakdown(player)`
Returns the full signal breakdown table.

### `system:GetFullRecord(player)`
Returns the full stored risk record.

### `system:GetDisplaySummary(player)`
Returns a formatted summary string.

Example:

```
Score: 35 | Label: Medium | Trust: LowTrust | Recommendation: Monitor
```

### `system:GetRecommendation(player)`
Returns the recommendation string.

### `system:GetTrustProfile(player)`
Returns the trust profile string.

### `system:GetTags(player)`
Returns the player’s current tags.

---

## State Helpers

### `system:IsLowRisk(player)`
### `system:IsMediumRisk(player)`
### `system:IsHighRisk(player)`
### `system:IsReviewRecommended(player)`
### `system:IsSafeListed(player)`

These return boolean values describing the player’s current state.

---

## Reevaluation

### `system:ReevaluatePlayer(player)`
Forces a reevaluation of the player’s account risk state.

---

## Moderation Queue APIs

### `system:GetFlaggedPlayers()`
Returns all currently flagged players.

### `system:GetPlayersNeedingReview()`
Returns players currently marked as needing review.

### `system:GetHighRiskPlayers()`
Returns players currently marked as high risk.

### `system:GetModerationFeed()`
Returns in-memory moderation feed history entries.

### `system:GetModerationSnapshot()`
Returns a table describing current moderation queue state.

Example moderation snapshot:

```
{
	FlaggedCount = 3,
	ReviewCount = 2,
	HighRiskCount = 1,
	FeedEntries = 12,
}
```

---

## Event Hooks

### `system.RiskChanged.Event`
BindableEvent fired when a player's risk state changes.

Arguments:
- `player`
- `newRecord`
- `oldRecord`

---

## Moderation Feed Events

### `system.ModerationAdapterService.FeedEvent.Event`
Fires whenever a moderation feed entry is pushed.

### `system.ModerationAdapterService.ReviewSuggestedEvent.Event`
Fires whenever a player record indicates review is suggested.

### `system.ModerationAdapterService.HighRiskEvent.Event`
Fires whenever a player is classified as high risk.

---

## Player Attributes

RiskLink Lite sets these player attributes:

- `RiskLinkScore`
- `RiskLinkLabel`
- `RiskLinkTrustProfile`
- `RiskLinkRecommendation`
- `RiskLinkReviewSuggested`
- `RiskLinkSafeListed`

---

## Test Utilities

RiskLink Lite can be paired with the included `TestUtils` module for debugging.

Example:

```
local TestUtils = require(game.ServerScriptService.RiskLink.TestUtils)
local tester = TestUtils.new(system)

tester:PrintPlayerRisk(player)
tester:ReevaluateAndPrint(player)
tester:PrintAllPlayers()
tester:PrintModerationSnapshot()
```
