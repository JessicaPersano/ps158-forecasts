# LLM county-level forecasts of the Nov 3, 2026 ballot measures: forecast values

Forecasts made **before the election** by Claude Opus 5.5 and Claude Haiku 5.5 for 142 statewide ballot measures in 38
states, for a pre-registered study (Stanford POLISCI 158, fall 2026). This repository publishes the forecast values only.
The full record (pre-registration and its amendments, data decisions, code, call logs and history) is in the
project's private working repository, which the course staff can access; `MANIFEST.sha256` ties the two together.

## Contents

- `forecasts/registered_forecasts.csv`: 12,780 forecasts (original sample 2,880; Tier 1 3,870; Tier 2
  6,030): model x information condition (no tools, web, curated data) x cue (neutral and four stated stakes) x 3
  repeats per measure. One row per forecast: identifiers and the statewide Yes share.
- `forecasts/registered_county_forecasts.csv`: the county (or county-equivalent) Yes shares for each forecast.
- `forecasts/agentic_forecasts.csv` and `agentic_county_forecasts.csv`: 426 forecasts by Opus 5.5 with a neutral cue,
  one per measure in three conditions where the model could write and run Python (no data; curated data; curated data
  plus web).
- **Not yet here: the models' text** (each forecast's key considerations and, for agentic forecasts, the model's
  description of its methodology). In the web conditions it may quote news articles, which can't be checked before the
  election without reading forecast content. The full files with the text are in the private repository
  (`forecast_text/`), and their SHA-256 hashes are in `MANIFEST.sha256`; the author checks the text for copied news
  content and publishes it after Nov 3, 2026.
- `baseline_b2/`: the B2 baseline forecasts, a mechanical rule fixed before the election.
- `MANIFEST.sha256`: the SHA-256 of every file here, of the full files with the text, and of each private forecast log
  the values were extracted from,
  plus the private repository's commit at build time (`d8be7dc9beb15ae9e6505cf6a9e98ad672934af7`).

Yes shares are percentages of Yes + No votes (0-100). Counties are identified by 5-digit FIPS codes. A forecast is
included exactly when the pre-registered analysis counts it (a valid, condition-true call made under the registered
settings). Call logs (prompts, tool calls, search results and page summaries) are not published; they are in the private
working repository (`forecast_logs/`, compressed), where course staff can check any value here against its log.

## Timeline

The forecasts were made at these times (start of the first and last counted call in each set, UTC):

- original sample: 2026-10-16 21:54 to 2026-10-18 21:38
- Tier 1 (extension): 2026-10-21 06:30 to 2026-10-23 02:14
- Tier 2: 2026-10-24 07:05 to 2026-10-25 12:43
- agentic: 2026-10-26 20:48 to 2026-10-27 03:57

This repository was built on Nov 1, 2026. The author emails its manifest
(`MANIFEST.sha256`) to the course TA before Nov 3, 2026, as the record of when it existed. After the election it will add the official results, the poll benchmark, the market
comparisons (aggregates only) and the analysis output.

## Use of AI

The forecasts are model outputs (the study's subject). The repository and its scripts were prepared with Claude Code
(Opus 5.5) under the author's direction.
