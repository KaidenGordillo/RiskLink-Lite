# Installation Guide

This guide explains how to install RiskLink Lite into a Roblox game.

---

## Requirements

- Roblox Studio
- Basic understanding of Explorer and ServerScriptService
- RiskLink Lite folder structure

No external tools are required for the base Lite version.

---

## Folder Placement

RiskLink Lite should be placed inside:

```
ServerScriptService
```

---

Recommended structure:

```
ServerScriptService
  RiskLink
    init
    Main
    Config
    ProductInfo
    TestUtils
    Bootstrap
    Services
      PlayerProfileService
      JoinAnalysisService
      RiskScoringService
      LoggingService
      SessionStoreService
      ModerationQueueService
      ModerationAdapterService
    Modules
      RiskSignals
        AccountAgeSignal
        AvatarSignal
        JoinBurstSignal
        BehaviorSignal
        NamePatternSignal
```

---

## Installation Steps

1. Open your game in Roblox Studio
2. Open Explorer and Properties
3. Insert the `RiskLink` folder into `ServerScriptService`
4. Confirm all scripts and subfolders are present
5. Press Play
6. Check Output for startup logs

Expected startup output:

```
[RiskLink] RiskLink Lite v1.0.0 | Initialized successfully.
```

---

## First Test

When a player joins, RiskLink Lite should:

- evaluate account risk
- create a session record
- assign player attributes
- print a moderation summary
- update moderation queues
- push a moderation feed entry

Example:

```
[RiskLink] RiskLink Lite v1.0.0 | PlayerName scored 0 (Low Risk) | Trust=Trusted | Recommendation=No Action
```

---

## Safelist Test

To test safelist behavior:

1. Open `Config`
2. Find `Config.SafeList.UserIds`
3. Add your Roblox UserId
4. Press Play again

Expected behavior:

- score remains `0`
- trust profile becomes `Safe`
- recommendation becomes `Ignore`
- tag `SafeListed` appears
- feed and summary output reflect safelist state

---

## Notes

- RiskLink Lite is server-side by default
- Lite does not auto-ban by default
- Lite is intended to support moderation workflows, not replace moderation judgment
- Moderation queue and feed systems are intended to scale better than relying on console output alone
