# SB Strategy Chart — 6-max NL50/NL100 (100bb, rake-adjusted for GGPoker)

> **Core principle:** The SB is the single worst seat at the table. With GGPoker's
> uncapped-on-small-pots rake, you **cannot** play it like a chip-EV solver.
> Default = **FOLD**. When you play, play a **RAISE-FIRST-IN (no limping)** strategy.
> Target SB VPIP ~**30–36%** (you were at 52.7% — that is the leak).

---

## A. SB — FOLDED TO YOU (you open or fold; NO LIMPING)

Use a larger open (3bb) because you are OOP vs the BB and want fewer, bigger pots.
Open size: **3bb** (e.g. $3 at NL100). Vs a BB who 3-bets a ton, mix in some limps later — ignore for now.

### RAISE (open) — ~38–40% of hands
```
Pairs:      22+  (all pairs open)
Suited A:   A2s - AKs  (all suited aces)
Offsuit A:  A5o - AKo
Suited K:   K5s - AKs
Offsuit K:  K9o - KQo
Suited Q:   Q7s - QJs
Offsuit Q:  QTo - QJo
Suited J:   J8s - JTs
Offsuit J:  JTo
Suited T:   T8s - T9s
Suited:     98s, 87s, 76s, 65s, 54s
```

### FOLD everything else
Notably **FOLD**: K2o–K8o, Q2o–Q9o, J2o–J9o, all offsuit connectors below JTo,
weak suited gappers (J7s-, T7s-, 96s-, etc.).

> ⚠️ You were entering 53% of SB hands. This range is ~39%. The hands you must
> **STOP** playing: offsuit junk (K7o, Q8o, J9o, T8o), weak suited gappers, and
> any limp.

---

## B. SB vs a BTN/CO/MP OPEN (you are facing a raise)

You are OOP and squeezed. Be **tight**. Default = **FOLD**. Use a **3-bet-or-fold**
approach (very little flatting OOP — flatting invites the BB to squeeze and you
realize equity poorly out of position).

### 3-BET (for value + a few suited bluffs) — tighter vs EP, wider vs BTN/CO

**vs BTN or CO open:**
```
VALUE:   99+, AQs+, AKo, AJs, KQs
BLUFF:   A5s, A4s, A3s (suited-ace blockers), KJs, QJs, suited sometimes
```

**vs MP/UTG open (tighter):**
```
VALUE:   TT+, AQs+, AKo
BLUFF:   A5s, A4s only
```

### FLAT (call) — ONLY these, and only vs BTN/CO opens
```
88-JJ (set-mine / flop-play, be ready to fold to aggression)
AQs/AJs when not 3-betting
Occasionally KQs
```
> Everything else = **FOLD**. Do NOT flat offsuit broadways or small pairs OOP vs
> a raise — that was feeding your SB losses.

### HARD RULE (fixes your #1 punt)
**If you 3-bet and then face an all-in / big 4-bet, continue ONLY with QQ+/AK.**
Fold 55, AJ, KQ, A5s, etc. (Reference: hand #RC4860405039 — you called off 55 vs a jam.)
