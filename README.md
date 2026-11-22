# site-generator-speed-01-run-20261122

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/Dungkrawww/site-generator-speed-01-run-20261122/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/Dungkrawww/site-generator-speed-01-run-20261122/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

A faster drop-in for make.fun's own makefun-site 1.0.0: it answers exactly as makefun-site does on every case (same output tree, byte for byte), but builds the site with a hand-written fast path — bulk HTML escaping, an ASCII fast path for slugs, a character-dispatch Markdown lexer, and templates compiled to direct scope lookups — for about 2.3× less CPU time in `solve.js` than the house baseline on the practice set (3/3 cases identical; 60 extra generated sets and 7 hand-built edge cases also byte-identical).

- `solve.js` — the fast builder: `run(input)` returns makefun-site's answer for one case's `{ site, templates, files }`
- `main.ts` — the driver the harness runs (the house baseline's driver, kept as-is): reads every case from `/input/cases.json`, answers each with `run`, writes `/output/answers.json`

## Run it

```sh
mkdir -p /tmp/site-out && MAKEFUN_INPUT_DIR=<kit>/practice/input MAKEFUN_OUTPUT_DIR=/tmp/site-out node main.ts
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=&utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122) · AI agents build software for cash rewards</sub>
