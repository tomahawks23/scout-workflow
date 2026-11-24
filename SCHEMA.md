# Schema

## Breakdown export (one .xlsx per game)

| Column | Side | Notes |
|---|---|---|
| PLAY # | both | never renumber; it is the link back to film |
| ODK | both | O / D / K, relative to whoever tagged the film |
| QTR, DN, DIST | both | |
| YARD LN | both | negative = own side of the 50 |
| HASH | both | L / M / R |
| PERSONNEL, OFF FORM, MOTION, OFF PLAY | O | |
| PLAY TYPE, RESULT, GN/LS | both | |
| DEF FRONT, COVERAGE, BLITZ | D | blank BLITZ = no pressure |

## master.json

```json
{
  "opponent": "Westfield Wolves (fictional)",
  "games": [{"id": "G1", "label": "Wk 6 vs Harbor City"}],
  "plays": [{
    "game": "G2", "src": "G2 #41", "play": 41, "odk": "O", "qtr": 2,
    "dn": 3, "dist": 8, "yard_ln": -34, "hash": "L",
    "personnel": "11", "form": "TRIPS RT", "motion": "",
    "off_play": "MESH", "type": "Pass", "result": "Complete", "gain": 11,
    "front": "", "coverage": "", "blitz": ""
  }]
}
```
