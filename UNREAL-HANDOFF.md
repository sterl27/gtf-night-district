# Grand Theft Family — Unreal handoff

Source of truth: the browser district in `grand-theft-family.html`. Do not rebuild fog, the analytic march, or the box Cadillac. Port the loop.

## What already plays

- Night avenue. Player is a black formal sedan. WASD, shift, brake.
- Job: three envelopes, gold door at Satriale’s, then Bing sit-down.
- F steals the nearest lane car and hides the Cadillac.
- E enters Satriale’s, the Bing, or Genco on foot. Eye camera. One line per room. E exits to the door.
- K saves cash, heat, loyalty, job flags, position.
- Fed heat rises with speed, crashes, and theft. Chase starts above 32. Job line changes above 70.

## Map

One district, not a city. Block span 3, block size 32 m, road 12 m.

| Place | World XY | Room |
| --- | --- | --- |
| Player start | 0, 18 | — |
| Satriale’s | -32, -24 | deli counter, case, gabagool line |
| The Bing | 32, 26 | bar, stools, envelope line |
| Genco | 64, -32 | crates, desk, olive-oil line |
| Envelope pins | 16,-12 / -22,22 / 44,-8 / 60,-28 | pickups |

Rooms in the page sit at x=400 so they do not intersect the avenue. In Unreal, use a sublevel or a streaming interior at the door.

## Cars

- Player: formal black sedan, clearcoat, chrome nose, vinyl roof, vertical tail lamps. No crest.
- Lane traffic: 14 sedans, four lanes, both directions.
- Feds: three dark cars, chase only when heat > 32.
- Steal: possess the traffic pawn. Do not teleport the Cadillac onto it.

Kenney CC0 trucks are in `vehicle-player.glb` and `vehicle-fed.glb`. Use them as parked props only.

## Missions

1. Collect 3 envelopes. +2500 ziti, +3 loyalty each.
2. Deliver at the Satriale gold door. +10000. Line: leave the gun, take the cannoli.
3. Enter the Bing. Choice: take the envelope (+8000, +15 loyalty) or walk.
4. Heat above 70 replaces the objective with “lose the avenue.”

Save keys: cash, fedsHeat, famHeat, loyalty, collected, delivered, sitdown, x, z.

## Unreal setup

- UE 5.4 or 5.5. World Partition on a small 512 m cell is enough. Do not enable a full city.
- Game mode: third-person vehicle, on-foot pawn swap at doors.
- Lighting: one directional moon, two cascades, night HDRI (`night.hdr` is Poly Haven moonlit golf, CC0). Street lamps are spot lights, every other one casts.
- Interiors: separate level instances. Eye-height camera. One dialogue node per room.
- Data: import `gtf-district.json` as a data table or read it from a blueprint function library.

## Do not port

- The fog ray march. Use exponential height fog and a light shaft on two lamps.
- Procedural plaster as final art. Satriale’s is the only hero interior.
- The box people. Use a MetaHuman or a Quaternius CC0 figure for the table only.

## First Unreal task

Empty map. Road spline on the avenue. One sedan pawn. One door that swaps to a 12x18 m room and back. Envelope pickup. Then the Bing line. Stop there.
