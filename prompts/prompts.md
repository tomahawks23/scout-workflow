# Prompts

The same prompts shown on https://scout-workflow.nasty-football.workers.dev, in one file. Paste one with your files attached.

## 1. Master file
Attached are Hudl breakdown exports, one file per game, for the same opponent. Merge them into one table.
- Add "game" (from the file name) and "src" = game + " #" + PLAY #.
- Normalize OFF FORM, OFF PLAY, DEF FRONT, COVERAGE and BLITZ using the alias table below. If a value is not in the table, keep it as written and list it at the end. Do not guess.
- Do not change HASH, DN, DIST, YARD LN or PLAY #. Blank stays blank.
Return master.xlsx and master.json, then report row counts per game and per ODK so I can check them against the film.

## 2. Scouting report
Using master.json, write a scouting report on this opponent. Compute every number with code from the file. Do not estimate.
For each section give a table, then one sentence saying what it means for us.
Sections: at a glance / run-pass by down & distance / by formation / top runs and passes / 3rd down / red zone (defense: front / coverage / pressure by down & distance / coverage behind pressure).
Print the snap count next to every percentage. Mark anything under 10 snaps as "thin". Where a claim rests on specific plays, list their src tags.

## 3. Game plan
Here is the scouting report and master.json. Here is what we run: [your call sheet or playbook list].
Draft a game plan as a table: their tendency / our call / evidence.
- Use only tendencies with 10 or more snaps behind them.
- "Our call" must be something from our list. Do not add plays we do not have.
- Evidence = the number, the snap count, and up to five src tags.
Give me two options where the numbers support more than one answer, and say what each one risks.

## 4. Practice script
Build a Team D practice script from master.json (offense rows only). Menu: 24 plays, downs cycle 1-2-3, ball on our 30-40.
- Copy HASH, formation, motion and play name exactly from the source row. Never change or invent them.
- Choose plays in proportion to how often the opponent calls them; no row twice.
- For a 3rd-down slot, use a play they ran on 3rd down.
- Columns: # / situation / hash / formation / play / type / src.
After the table, report the run-pass split of the script next to the opponent's real split.
