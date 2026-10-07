# ⚾ Baseball United Global Baseball Database

An interactive database of every player connected to Baseball United, the Middle East/South Asia-based pro baseball league: the 2023 Draft, the 2023 Dubai Showcase, and the 2025 inaugural season.

## What it does

A single self-contained web page (`baseball_united_database.html`, no build step or dependencies) with five tabs:

| Tab | Description |
|---|---|
| **Players** | Search by name, country, position or team. Filter by 2023 Showcase, 2023 Draft, 2025 season, or MLB experience. Click a row for a full profile. |
| **Countries** | Players by birth country. |
| **Career Levels** | Highest professional level reached (MLB, AAA, AA, NPB, LMB, etc.). |
| **History** | Timeline: 2023 Draft → 2023 Showcase → 2024 Arab Classic → 2025 season → United Series. |
| **Standings & Games** | 2025 standings, league leaders, and all 21 games (18 regular season + 3 United Series). |

## Data

Source files:

- `Baseball_United_Global_Baseball_Database.xlsx`: 17 sheets (player master, all player records, draft, showcase, 2025 rosters, in-season adds, games, standings, leaders, highlights, Arab Classic, team history, data dictionary, sources)
- `Baseball_United_Global_Player_Master.csv`: deduplicated player list

The page merges these into one record per player. Key design choice: **Drafted ≠ Showcase participant ≠ Rostered ≠ Actually appeared.** Each is tracked separately so history isn't flattened.

Franchise history: Dubai Wolves → Arabia Wolves, Abu Dhabi Falcons → Mid East Falcons. Other franchises: Mumbai Cobras, Karachi Monarchs.

## Known limitations

- **Player count:** the page shows 160 players versus 155 in the Player Master. The 5 extras come from the 2025 in-season adds sheet and may be name mismatches. Needs review.
- **Gaps:** birth country is missing for 31 players and highest level for 112. These are left blank, not guessed.
- **No player-level stats:** only season leaders and highlights are included. Individual batting/pitching lines were not verified, so none are shown.
- **No career paths yet:** the data has highest level only, not full paths (e.g. MLB → NPB → Baseball United).
- **No world map:** countries are shown as a bar chart.

## Roadmap

1. Fill in missing birth country and highest level
2. Resolve the 5 extra player records
3. Add official Season 1 batting and pitching stats
4. Add career-path data and a "Where did they come from?" visualization
5. Add MLB career stats and draft info
6. Build a Baseball United Impact Rating (BU performance, MLB résumé, level reached, age, international experience, team impact)
7. Add a world map

## Run locally

Open `baseball_united_database.html` in any browser.
