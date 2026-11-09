# GridIron Data MCP server

NFL fantasy football data for AI assistants: players, weekly and rest-of-season projections, stats, snap shares, matchups, news, injury changes and player-prop probabilities.

This is the official [GridIron Data](https://www.gridirondata.com) remote MCP server. There's nothing to install: connect to

```
https://api.gridirondata.com/mcp
```

It uses Streamable HTTP. You sign in with a GridIron Data account through OAuth; [free accounts](https://www.gridirondata.com/pages/signup.html) are available. You can also send an API key as `Authorization: Bearer <key>`.

<!-- mcp-name: io.github.avansledright/gridiron-data -->

## Connect

**Gemini CLI**

```bash
gemini extensions install https://github.com/avansledright/gridiron-data-mcp
```

**Claude Code**

```bash
claude mcp add --transport http gridiron-data -s user https://api.gridirondata.com/mcp
```

**Claude, ChatGPT and other apps with custom connectors:** add `https://api.gridirondata.com/mcp` as a custom connector, then sign in.

**Cursor and any `mcpServers` JSON client**

```json
{ "mcpServers": { "gridiron-data": { "url": "https://api.gridirondata.com/mcp" } } }
```

Full setup guide: https://www.gridirondata.com/pages/guide-mcp.html

## Tools

| Tool | What it does | Lowest plan |
|---|---|---|
| `list_players` | List players, optionally by position, paginated | Free |
| `search_players` | Find players by name (optional position) | Free |
| `get_player` | Player profile: team, position, injury status | Free |
| `get_player_by_espn_id` | Look up a player by ESPN id | Free |
| `get_player_by_gsis_id` | Look up a player by NFL GSIS id | Free |
| `get_projections` | Weekly projections, PPR / half / standard | Free (current week) |
| `get_ros_projections` | Rest-of-season projections | Basic |
| `get_schedule` | Regular-season schedule with scores | Basic |
| `get_byes` | Bye weeks by team | Basic |
| `get_player_stats` | Weekly and season stats, 2020 to the current season | Basic |
| `get_deviations` | Boom/bust: actual vs projected | Basic |
| `get_snap_share` | Weekly snap share and role trend | Basic |
| `get_matchups` | A player's history against an opponent | Basic |
| `get_player_news` | Impact-tagged news for a player | Basic |
| `request_news_scrape` | Ask for a fresh news pull for a player | Basic |
| `get_latest_news` | League-wide latest news feed | Basic |
| `get_injury_changes` | Feed of injury-status changes | Pro |
| `get_prop_probability` | P(over/under) and fair no-vig odds for a player stat line | Pro |
| `get_defense_vs_position` | What each defense allows to QB / RB / WR / TE | Pro |
| `get_depth_chart` | Depth charts and starters | Pro |
| `get_inactives` | Official game-day inactives | Pro |

Plans and prices: https://www.gridirondata.com/pages/pricing.html

Player IDs are `"First Last#POS"` (for example `"Josh Allen#QB"`), matched case-insensitively. Scoring is `ppr` (default), `half` or `standard`. Prop numbers are a model estimate, not betting advice.

## Links

- Website: https://www.gridirondata.com
- REST API docs: https://www.gridirondata.com/pages/docs.html
- Privacy: https://www.gridirondata.com/pages/privacy.html · Terms: https://www.gridirondata.com/pages/terms.html
- MCP Registry: `io.github.avansledright/gridiron-data`

## License

The files in this repository are MIT licensed. Use of the GridIron Data service is governed by its [terms](https://www.gridirondata.com/pages/terms.html).
