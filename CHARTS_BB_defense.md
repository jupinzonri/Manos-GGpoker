# BB Strategy Chart — 6-max NL50/NL100 (100bb, rake-adjusted for GGPoker)

> **Core principle:** In the BB you already have 1bb invested and close the action,
> so you defend **wider** than any other seat — BUT you were defending TOO wide
> AND too passively (46.5% VPIP, only 9% PFR). The fix is twofold:
> (1) stop defending the junkiest offsuit hands, (2) add 3-bets so your range
> isn't a face-up, capped calling range.
> Target BB VPIP ~**40–45%**, but with PFR ~**13–16%** (not 9%).

---

## A. BB vs a SINGLE RAISE (you close the action)

Your defense width depends on the opener's position & size. Assume ~2.3–3bb opens.

### 3-BET (do this MORE — you were only PFR 9%)
Build a 3-bet range of value + bluffs so you're not purely calling.

```
VALUE:   TT+, AQs+, AKo, AJs, KQs
BLUFF:   A5s-A2s (wheel aces, blockers), K9s-KQs mix,
         suited connectors (76s-T9s) as occasional bluffs
```
Size: **vs BTN/CO open → 3.5x; vs EP open → 4x.** Larger OOP.

### CALL (flat) — wide, but NOT junk
**vs BTN/CO open (defend wide):**
```
Pairs:    22-99 (flat; TT+ mostly 3-bet)
Suited A: A2s-AJs (the ones not 3-betting)
Offsuit A: A8o-AJo
Suited K: K5s-KJs
Offsuit K: KTo-KQo
Suited Q: Q8s-QTs
Offsuit Q: QJo (QTo vs BTN only)
Suited J: J8s-JTs
Suited T: T8s-T9s
Suited:   54s-98s
Offsuit:  JTo, T9o (vs BTN only)
```

**vs MP/UTG open (tighter — fold the trash):**
```
Pairs:    22-99
Suited:   A2s-AJs, K8s-KJs, Q9s-QTs, J9s-JTs, T9s, 76s-98s, 54s-65s
Offsuit:  A9o-AJo, KTo-KQo, QJo, JTo
```

### FOLD (STOP defending these — this is your leak)
```
Offsuit junk: K2o-K8o, Q2o-Q9o, J2o-J8o, T2o-T8o, 92o-98o, all low offsuit
Weak suited gappers vs EP: J7s-, T6s-, 95s-, 84s-
```
> You were calling raises with hands like K7o, Q9o, J8o OOP, then check-folding
> flops (your 41.8% won-at-showdown reflects this). These are **folds.**

---

## B. BB POSTFLOP as the preflop CALLER (fix your passivity)

Because you flat a lot in the BB, how you play flops matters more than the chart.
- **Check-raise more** on boards that favor your calling range (low/middling,
  paired, connected) — e.g. 7-6-2, 9-8-5, 4-4-x. Target ~12–15% flop XR.
- **Donk-lead** small (~30%) on boards that smash BB range and miss the opener's
  (low connected: 6-5-4, 7-8-9 two-tone).
- **Give up** when you miss on A-high / K-high dry boards — don't float wide OOP
  with no equity (this fed your "float then fold" losses).

### HARD RULES
1. **Do not peel a flop with zero equity (no pair, no draw, no backdoors) vs a cbet.** Fold.
2. **Do not turn made bluff-catchers into bluffs** on later streets (your A6o/A-high barreling pattern — reference hand #RC4860694892).
3. Against the sticky NL50/NL100 population: **value-bet thinner, bluff less.** They call.
