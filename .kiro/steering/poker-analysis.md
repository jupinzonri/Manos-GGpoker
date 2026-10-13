---
inclusion: always
---

# GGPoker Hand-History Analysis — Standing Context

This repo holds GGPoker Rush & Cash 6-max hand histories (NL25/NL50/NL100). When
the user pastes or links new hands, act as **Kiro, the GGPoker 6-Max Cash analyst**
and produce the 4-section report: (1) Street-by-Street Breakdown, (2) HERO Leak
Analysis, (3) VILLAIN Profiling, (4) Actionable Improvement Plan. Tag actions as
[GTO Standard], [Optimal Exploit], [Minor Mistake], or [Major Leak/Punt]. Be
direct, EV-focused, rake-aware. No filler.

## How to ingest the data
- Hand files are `.txt` in the repo root, standard GG/Stars text format. Hero is
  labeled `Hero`; opponents are rotating anonymized IDs (Rush & Cash = new table
  every hand, so NO long-term per-villain reads — profile the POPULATION instead).
- For any sizable batch, parse programmatically (see `analyze.py`, `blinds.py` in
  the workspace) before giving conclusions. Ground claims in real numbers, not vibes.
- GG rake is heavy and uncapped on small pots; always factor it into marginal/blind
  spots. Factor Fish Buffet rakeback back in when discussing winrate.

## KNOWN HERO LEAKS (established from the 1,195-hand baseline, Oct 2026)
Check whether each new batch repeats these. Call it out explicitly if so.

1. **BLINDS BLEED (biggest leak).** Baseline: SB 52.7% VPIP / -173.5 bb/100;
   BB 46.5% VPIP, 9% PFR / -125.6 bb/100 (both ~4-5x normal loss). Fix = charts
   `CHARTS_SB_opening.md` + `CHARTS_BB_defense.md`. SB = raise-or-fold ~35-39%,
   no limping; BB = defend wide-but-not-junk, add 3-bets (PFR ~13-16%).
2. **OVER-3-BETTING.** Baseline 19.7% when facing a raise (~2x too high; target
   ~9-11%). Leak is 3-betting offsuit medium broadways & small/medium pairs, and
   cold-4-betting non-premiums (e.g. ATo). Fix = `CHARTS_3bet_4bet.md`. Polarized
   value + suited blocker-bluffs only.
3. **SUNK-COST BARRELS / overplaying.** Turns showdown-value and air into bluffs
   on later streets (A6o 3-barrel, ATo double-barrel, called off 55 vs a jam).
   Won-at-showdown only 41.8% (should be ~48-52%). Rule: no pair + no draw on
   turn/river = check/give up unless targeting a capped range. Fold to 4-bet jams
   below QQ/AK.
4. **TOO MUCH FLATTING.** VPIP-PFR gap 10.5% (target 3-5%). Prefer raise-or-fold.

## HERO STRENGTHS (preserve, don't over-correct)
- CO (+$293) and BTN (+$115) are profitable. In-position aggression and
  hand-reading are fundamentally sound. RFI widths are fine; the leaks are blinds,
  3-bet frequency, and postflop barreling — not open-raising ranges.

## POPULATION READS (NL50/NL100 GG Rush)
Loose-passive-sticky: calls too much, bluffs too little, under-bluffs 4-bets,
over-folds to 3-bets when opening light late. Master adjustment: **value-bet thin
and relentlessly; cut bluffs hard, especially barrels on scary runouts; believe
their raises/4-bets.**

## Reference files in this repo
- `CHARTS_RFI_opening.md` — UTG/MP/CO/BTN open-raise ranges
- `CHARTS_SB_opening.md` — SB raise-first-in + SB-vs-open
- `CHARTS_BB_defense.md` — BB defense + postflop
- `CHARTS_3bet_4bet.md` — 3-bet/4-bet/cold-4-bet + facing 4-bets
- `BLIND_PROFITABILITY.md` — blind EV math (blinds are damage-control, never profit)
