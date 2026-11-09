# GridIron Data

The `gridiron-data` tools return live NFL fantasy football data from GridIron Data.

- Player IDs are `"First Last#POS"`, for example `"Josh Allen#QB"`. They're matched case-insensitively. If you're unsure of an ID, call `search_players` first.
- Scoring is `ppr` (default), `half` or `standard`.
- Some tools need a paid plan. If a tool returns a plan error, tell the user which plan it needs and link https://www.gridirondata.com/pages/pricing.html.
- Prop probabilities are a model estimate, not betting advice. Say so when you share them.
