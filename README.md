# The Rivalry Ledger

Andre's Madden head-to-head scoreboard: **https://gallatindev.github.io/rivalry-ledger/**

## Where the games live

Every game is one line in [`data/games.json`](data/games.json). The scoreboard reads that file, so saving a change to it updates the site within a few minutes. Wins and losses are worked out from the scores, so they can never disagree with them.

## Adding a game

Add a new line at the end of the `games` list. Put a comma after the line before it, and no comma after the new last line.

```json
{ "id": 16, "date": "2026-10-25", "opponent": "James", "myTeam": "Los Angeles Chargers", "myScore": 21, "oppTeam": "Seattle Seahawks", "oppScore": 7 }
```

| Field | What goes in it |
|---|---|
| `id` | The next number after the last game |
| `date` | The day it was played, as `YYYY-MM-DD` |
| `opponent` | `"James"`, `"Online"`, or another player's name (a new name gets its own tab) |
| `myTeam`, `oppTeam` | Full team names, city and nickname, such as `"Los Angeles Chargers"` |
| `myScore`, `oppScore` | Andre's score and the opponent's score |
| `notes` | Optional, such as `"James conceded."` |
| `passYds`, `rushYds`, `tds`, `turnovers` | Optional stats for Andre's team |

To edit on GitHub: open `data/games.json`, click the pencil icon, make the change, then click **Commit changes**.

If the file has a typo (a missing comma or quote), the scoreboard says the scores didn't load. Fix the line and commit again.
