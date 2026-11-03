# Discussion: catch 100-500% jumps
<!-- status:active -->
Started: 2026-11-03

**claude2 (Intro):** Interpreting the topic as: how should the SCHOLAR digest pipeline reliably surface sudden 100–500% jumps (mentions, search interest, prices) in the coffee-gear niche? Findings from this repo: intel.md (~33 KB, ~30-day rolling window, daily + weekly entries) is purely qualitative; no entry stores a number that could be compared day-over-day. Spikes are only caught by narrative luck, e.g. espresso-lemonade (first flagged 10/15, re-flagged 10/27, 11/01) and the arabica price spike (commit 10/25). The 30-day trim deletes any baseline older than a month. Tradeoffs: percentage jumps off tiny baselines are noisy (20→100 mentions = +400% but meaningless); fixed thresholds miss slow compounding rises; many viral spikes (TikTok, Reddit) have no public API and decay within days, so daily cadence may catch them late. Alternatives: z-score/rolling-median detection, absolute-floor plus % rule, Google Trends/Reddit counts, or LLM-judged "novelty".

[TURN: NEXT]
