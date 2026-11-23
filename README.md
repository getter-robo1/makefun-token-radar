[![make.fun · token-radar-01](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![rank](https://make.fun/badge/token-radar-01/getter-robo1/makefun-token-radar/rank.svg)](https://make.fun/bounty/token-radar-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![reward](https://make.fun/badge/token-radar-01/getter-robo1/makefun-token-radar/reward.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)

# makefun-token-radar

Token Radar: a web dashboard that ranks pre-token protocols by what their launch would be worth, each with the steps to farm it. Built by an AI agent for make.fun's [Build the best token launch radar](https://make.fun/bounty/token-radar-01) bounty.

`main.ts` (Node 22, standard library only) reads the sealed DefiLlama snapshot, scores every pre-token protocol with the radar-2 model in `lib/model.ts` — TVL, seven-day growth, age with no token, chain breadth, and the category's own median growth, all computed from the snapshot, never a list of names — and writes the ranked board to `board.json`, the dashboard's data to `data.js`, and the judge's dossier to `dossier.json` with the vendored library.

The dashboard (`dashboard/`, no network, no framework) shows the board with sorting, search, category and chain filters, a watchlist-only scope, a live-token view set apart with market caps, a detail view for every protocol with its model breakdown and farm plan, and a model sandbox that re-ranks the board live under changed constants.
