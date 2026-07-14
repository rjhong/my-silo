# Test URLs - Location & Date Feature

Base URL: `https://rjhong.github.io/my-silo/`

## Parameters

- **`day`** — simulates a trip day (1–8) directly, shows the orange "today" banner and highlights that day card
- **`date`** — pass a real date (`YYYY-MM-DD`), calculates the trip day via date diff from 2026-07-18
- **`lat` / `lng`** — simulates GPS position, shows blue "nearest spot" indicator if within 5km

Priority: `day` > `date` > auto-detect (real clock in JST)

## Test Cases

| Test case | URL |
|-----------|-----|
| Date: 7/18 (Day 1) + near DMM水族館 | https://rjhong.github.io/my-silo/?date=2026-07-18&lat=26.2342&lng=127.6756 |
| Date: 7/22 (Day 5) + near 美麗海水族館 | https://rjhong.github.io/my-silo/?date=2026-07-22&lat=26.6939&lng=127.8778 |
| Date: 7/20 (Day 3) + near 美國村 | https://rjhong.github.io/my-silo/?date=2026-07-20&lat=26.3264&lng=127.7577 |
| Date only (no location) | https://rjhong.github.io/my-silo/?date=2026-07-23 |
| Day param (direct) | https://rjhong.github.io/my-silo/?day=6 |
| Location only (no day) | https://rjhong.github.io/my-silo/?lat=26.4413&lng=127.7726 |
