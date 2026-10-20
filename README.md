# Grand Theft Family

Night mob district. Sopranos / Godfather tone. GTA loop.  
One avenue, not a city.

## Current status

- Browser prototype complete (`grand-theft-family.html`) and temporarily deployed.
- Unreal handoff package ready.
- Short Unreal milestone defined and stepped out.
- MetaHuman capture pack for Ritch (Night Drive Driver) also prepared (separate track).

## What already plays (browser)

- Night avenue, formal black sedan, WASD / Shift / Space.
- Three envelopes → gold door at Satriale’s → Bing sit-down.
- E enters interiors on foot (eye-height camera).
- F steals nearest lane car.
- K saves cash, heat, loyalty, job flags, position.
- Volumetric fog, cascaded shadows, HDRI, minimap, radio, horn.

## Unreal short milestone

Ends when you can:
- Drive the avenue
- Pick up one envelope
- Enter Satriale’s on foot
- Hear the gabagool line
- Exit back to the same car
- Save and load restore position and ziti
- Bing door also swaps

Nothing else is required for the milestone.

### Setup order
1. Empty World Partition map + night lighting + avenue spline  
2. Chaos vehicle sedan  
3. Satriale’s door-swap (hide car → eye-height pawn → 12×18 m room → back)  
4. Envelopes + job progression + HUD + K save/load  
5. Bing door (same pattern)

### Key numbers (from `gtf-district.json`)
- Block size: 32 m
- Road width: 12 m
- Span: 3 blocks each way
- Player start: (0, 18)
- Satriale’s: (-32, -24)
- The Bing: (32, 26)
- Envelopes: (16,-12), (-22,22), (44,-8), (60,-28)
- Payouts: envelope 2500, gold door 10000, Bing sit-down 8000
- Heat: chase starts > 32, panic > 70 (store only for now)

### Controls (target)
- WASD drive
- Shift boost
- Space brake
- E enter / exit
- F steal
- K save
- Q radio
- H horn

## Do not port
- Browser fog ray-march (use Exponential Height Fog)
- Procedural box Cadillac as final art
- Full city / World Partition city
- Fed chase (this milestone)
- Genco interior (this milestone)
- Crests, logos, or show-accurate likenesses

## Files
- `UNREAL-HANDOFF.md` — loop and do-not-port rules
- `UNREAL-NEXT-PROMPT.md` — first milestone scene + instructions
- `gtf-district.json` — places, envelopes, payouts
- `gtf-unreal-handoff.zip` — packaged handoff
- `night.hdr` — Poly Haven moonlit golf (CC0)
- `vehicle-player.glb` / `vehicle-fed.glb` — Kenney CC0 parked props only

## Next after the milestone
- Expand avenue to full district blocks
- Proper Chaos vehicle polish
- Streamed interiors
- Heat actually rising + Fed chase
- MetaHuman or Quaternius figure at the table
- Later: photogrammetry room, EmpireRPG chapter

## Tone
North Jersey night. Sodium lamps. The job is already known.  
No crest. No likenesses. Night stays night.
