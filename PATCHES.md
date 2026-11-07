# SurrounSync patches (hugge01)

Base: **SYMPLYSCK/SurrounSync `v1.1.0`** (`351a1f2`).  
License: all rights reserved — Hugo has **written author OK to modify**. Keep attribution; do not republish as original work.

This branch holds **patch files + modified Lua mirrors only** (not a full upstream tree — clone SYMPLYSCK/SurrounSync @ v1.1.0 and apply `patches/0001-…` or copy the four `mod/.../mirror/*.lua` files over).

## 0001 — join FPS / vehicle absorb + soft autosave/weather

| Change | Why |
| --- | --- |
| `util.lua` absorb unknown group children | Avoid forever one-FindAllOf-per-class after game updates (join hitch; Humvee2 lesson) |
| `vehicles.lua` scan learned Vehicle_* | New car types sync instead of guest duplicate spawn |
| `config.lua` checkpoint_min_interval 90→150 | Soft lever for autosave/ghost hitch (Reddit) |
| `world.lua` JUMP_CONFIRM 1.5→2.5 | Soft lever for weather stall flicker (Reddit) |

**Not patched (need 1.1.0 smoke repro):** infestations residual, drop/loot edge cases beyond 1.1 claims, vehicle launch/enter, join FPS beyond group walks.

Apply on test copy only (`D:\\coop-test-surrounsync`). Never live Steam. Never mix with SDO Win64.
