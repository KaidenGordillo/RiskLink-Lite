# FAQ

## Does RiskLink Lite guarantee alt detection?

No.

RiskLink Lite is not a guaranteed alt detector.  
It is an account risk intelligence framework that helps identify suspicious account patterns and moderation risk.

## Is RiskLink Lite only useful through Output logs?

No.

Output logs are mainly for:
- setup
- testing
- debugging
- demonstrations

RiskLink Lite also provides:
- player attributes
- public APIs
- moderation queue APIs
- moderation feed events
- review and high-risk queues
- moderation snapshots

This makes it useful in larger games and future admin systems.

## Can I safelist trusted users?

Yes.

You can add specific Roblox UserIds to the safelist in `Config.SafeList.UserIds`.

## Can I integrate RiskLink Lite into my own admin system?

Yes.

RiskLink Lite exposes:
- player attributes
- risk queries
- trust profile data
- recommendations
- event hooks
- moderation feed events
- queue APIs
- full risk records

These make admin integration straightforward.

## Is RiskLink Lite lightweight?

Yes.

RiskLink Lite is designed to remain lightweight and practical for most Roblox games.

## Is RiskLink Lite suitable for roleplay or moderation-heavy games?

Yes.

RiskLink Lite is especially useful for:
- roleplay games
- community games
- moderation-heavy games
- public experiences vulnerable to suspicious join waves

## Does RiskLink Lite use Roblox's Ban API?

Not by default.

The configuration contains future-facing moderation foundation settings, but Lite does not automatically use Ban API moderation.

## Why is Avatar scoring disabled?

Avatar scoring in Lite is currently conservative and disabled by default to avoid weak or misleading scoring behavior.

## Will there be a Pro version?

That is the planned direction.

RiskLink Lite is intended to serve as the free foundation for a broader moderation and account intelligence product line.

## Does RiskLink Lite auto-ban users?

No, not by default.

RiskLink Lite is intentionally conservative and does not auto-ban by default.  
It provides moderation intelligence, not automatic punishment by default.

