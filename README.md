# scout-workflow

Prompts and sample data for turning Hudl breakdown exports into a scouting report, a game plan and a scout-team practice script with an LLM.

Guide, step by step: https://nastyfootball.com

## The pipeline

1. **Export**: one Excel file per game from Hudl breakdown data
2. **Master file**: merge games, normalize names, tag every snap with its source (`G2 #41`)
3. **Scouting report**: down & distance, formation, front, coverage, pressure
4. **Game plan**: tendency → call → evidence
5. **Practice script**: scout-team reps copied from real snaps
6. **Playlists**: one per script and per tendency
7. **Scout cards**: drawn from the script ([Football Designer](https://playmaker-demo.pages.dev))

## What is here

- `prompts/prompts.md`: the four prompts (master file, report, game plan, script)
- `sample/`: three fictional game exports (`wolves_g1..3.xlsx`) and the merged `master.json`
- `SCHEMA.md`: the columns and the JSON shape every step expects

## Three rules

- Every row keeps its film tag from the merge onward.
- The LLM counts and writes. It never guesses what the opponent runs.
- Every percentage prints with its snap count.

## Try it

Upload the three files in `sample/` to any LLM that can run code on uploads, paste prompt 1, then work down the list.

## More

The slide template, the script workbook and the longer skills are in the free kit: https://nastyfootball.com/kit

All sample data is fictional (Westfield Wolves). Not affiliated with or endorsed by Hudl.
