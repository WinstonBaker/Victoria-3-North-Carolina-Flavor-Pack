# North Carolina Flavor Pack

North Carolina flavor for Victoria 3 (`1.13.*`): journal chains, decisions, unique buildings, companies, characters, and state traits centered on North Carolina — without a full USA overhaul.

## Install

1. Place this folder in your Victoria 3 `mod/` directory (Paradox Interactive path), or subscribe via the Paradox Mods / Steam Workshop page when published.
2. Enable **North Carolina Flavor Pack** in the launcher.
3. Compatible with vanilla USA; no hard dependencies on other flavor mods. Company **prestige goods** require the Charters of Commerce DLC (`mp1_content`).

## Content (overview)

| Pillar | Highlights |
|--------|------------|
| **Universities** | Full UNC System (Chapel Hill + NCSU/Duke Triangle + 14 regional charters incl. ECSU & WSSU), Wake Forest relocation, education prestige |
| **Outer Banks** | Lighthouse program, Board funding, fuel PMs, ongoing storm/wreck pulse + coastal reconstruction |
| **Rail** | Wilmington & Weldon → Atlantic & NC → Western NC → Carolina Rail Network |
| **Piedmont industry** | Textiles, Duke Power, High Point furniture, mill village, Carolina brands, naval stores |
| **Tobacco Belt** | Brightleaf corridor; Duke / Reynolds / Liggett story |
| **Coast & century** | Cape Fear / Morehead ports, Wright brothers, Reconstruction → New South |
| **Characters** | Historical industrialists & educators (Duke, Reynolds, Bradham, Vanderbilt, Wrights, …) |
| **Landmarks** | State Capitol, Biltmore, state traits, gold belt |

All journal entries use the **North Carolina** JE group (`je_group_nc_flavor`). Unique buildings use building group `bg_nc_flavor`.

## Version

Current release: **1.3.0** (see `.metadata/metadata.json`). Supported game version: `1.13.*`.

## Known issues / notes

- Event IDs `.3` and `.25`–`.30` in `events/nc_events.txt` are **reserved** — do not reuse them without checking save/history compatibility. IDs `.35`–`.37` are **retired** (former NCSU Centennial expansion); `.72`–`.75` are **retired** (former Valdese / migrant hooks); next free IDs start at `.78+`.
- Play as the USA (or any country that owns incorporated North Carolina) to see the full JE tab.
- New content prefers timed modifiers and decisions over new laws or country tags.
- Character portraits are placeholders (no custom DNA yet).
- Davidson, Shaw, Elon, and Johnson C. Smith remain as **legacy-only** campus buildings (old saves / prestige count); they are not charterable in 1.3.
- Deferred backlog (not in 1.3): Jewish merchant towns, Valdese-scale migrant colonies (too small for Vic3 state impact), late-game pulse events, custom portraits, Oak Island, languages / 3D assets.
- Workshop packaging: keep `gfx/interface/icons/building_icons/_preview/` out of published zips (gitignored source PNGs only).

## Contributing / smoke test

After changes, in-game check:

1. Start buildings: UNC, Wake Forest, starting lighthouses, gold mines; NC state traits present
2. Mid-game: university / lighthouse charter recovery still works (cancel mid-build frees the slot without soft-lock); finished lights also credit if the build JE missed them
3. Industry JEs: Carolina Brands, naval stores, mill village, Tobacco Belt — decisions appear and company unlocks remain attainable (NCR after Piedmont trunk; sponsors note remaining building levels)
4. History arcs (1.2): Cape Fear ports, Wright brothers (from 1896 / flight 1903), Reconstruction→New South (from 1866)
5. Systems (1.3): company founding / Triangle / Biltmore / Wright spawn characters; education prestige scales with campuses (innovation + migration pull); after lights complete, Outer Banks storm JE pulses and Coastal Reconstruction decision clears damage
6. With Charters of Commerce: flavored company prestige goods appear; without CoC, no script errors
7. Error log clean on load (no missing loc / icons)
