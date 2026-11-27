# Travel Buddy

Tell it what you want to do, and it finds where to go.

*"Castles and bike paths, quiet, within 2 hours of Kraków, no car, 2 days"* → a short list of towns that fit, and
day plans where every line links to the guide sentence it came from.

A plain chatbot guesses. Travel Buddy checks:
- **Grounded:** every claim cites its source ([Wikivoyage](https://www.wikivoyage.org/) travel guides).
- **Constraints checked by code:** distances, route lengths and surfaces are computed, not guessed
  (bike routes from [OpenStreetMap](https://www.openstreetmap.org/)).
- **Measured:** retrieval quality, faithfulness, cost and latency per plan are tracked with evals.

Status: early planning. Starts with Poland.

## Setup
```bash
cp .env.example .env   # add your keys here; .env is never committed
git config core.hooksPath .githooks   # enables the secret check before each commit
```

## Data and licences
- Code: MIT (see `LICENSE`).
- Wikivoyage content: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/), © Wikivoyage contributors.
- OpenStreetMap data: [ODbL](https://opendatacommons.org/licenses/odbl/), © OpenStreetMap contributors.
