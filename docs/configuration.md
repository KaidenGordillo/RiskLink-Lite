# Configuration Guide

RiskLink Lite is configured through a single `Config` module.

This makes it easy to tune:

- score thresholds
- safelist behavior
- moderation feed behavior
- policies
- signal settings

---

## Logging

```
Config.Logging = {
	Enabled = true,
	Verbose = true,
	Prefix = "[RiskLink]",
}
```

---

## Risk Labels

```
Config.RiskLabels = {
	LowMax = 24,
	MediumMax = 49,
}
```

---

## Trust Profiles

```
Config.TrustProfiles = {
	Safe = "Safe",
	Trusted = "Trusted",
	LowTrust = "LowTrust",
	HighRisk = "HighRisk",
}
```

---

## Recommendations

```
Config.Recommendations = {
	Low = {
		Text = "No Action",
		ReviewSuggested = false,
		SuggestedAction = "None",
		SuggestedDurationHours = 0,
	},
	Medium = {
		Text = "Monitor",
		ReviewSuggested = true,
		SuggestedAction = "ManualReview",
		SuggestedDurationHours = 0,
	},
	High = {
		Text = "Manual Review Recommended",
		ReviewSuggested = true,
		SuggestedAction = "Escalate",
		SuggestedDurationHours = 0,
	},
	Safe = {
		Text = "Ignore",
		ReviewSuggested = false,
		SuggestedAction = "None",
		SuggestedDurationHours = 0,
	},
}
```

---

## Safelist

```
Config.SafeList = {
	Enabled = true,
	UserIds = {
		-- 123456789,
	},
}
```

---

## Moderation Feed

```
Config.ModerationFeed = {
	Enabled = true,
	StoreHistory = true,
	MaxHistoryEntries = 100,
}
```

---

## Webhooks

```
Config.Webhooks = {
	Enabled = false,
	Endpoint = "",
	LogHighRiskOnly = true,
}
```

---

## Policies

```
Config.Policies = {
	Enabled = true,

	OnMediumRisk = {
		Enabled = false,
		Action = "Notify",
	},

	OnHighRisk = {
		Enabled = false,
		Action = "Notify",
	},

	OnSafeListed = {
		Enabled = false,
		Action = "Ignore",
	},
}
```

---

## Signals

### AccountAge

```
Config.Signals.AccountAge = {
	Enabled = true,
	LessThan7Days = 30,
	LessThan30Days = 20,
	LessThan90Days = 10,
}
```

---

### JoinBurst

```
Config.Signals.JoinBurst = {
	Enabled = true,
	WindowSeconds = 120,
	BurstJoinCount = 5,
	BurstScore = 15,
}
```

---

### Behavior

```
Config.Signals.Behavior = {
	Enabled = true,
	QuickRejoinWindow = 180,
	QuickRejoinScore = 10,
}
```

---

### NamePattern

```
Config.Signals.NamePattern = {
	Enabled = true,
	RandomDigitSuffixLength = 4,
	RandomDigitSuffixScore = 8,
	GenericUsernameScore = 5,
}
```

---

### Avatar

```
Config.Signals.Avatar = {
	Enabled = false,
	DefaultLikeScore = 5,
	LowAccessoryScore = 5,
}
```

Avatar scoring is disabled by default in Lite.
