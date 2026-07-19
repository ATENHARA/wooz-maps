# Wooz Maps

A custom, high-contrast map pack for **[EverQuest Legends](https://www.everquestlegends.com/home)**, built for use with the game's built-in map viewer.

This started as a recolor of **Brewall's Dark Maps** toward an even darker, higher-contrast aesthetic, but grew into something more involved: many EverQuest Legends zones exist under two different internal names — a modern redesigned version and an older "classic" version — and the game frequently loads the classic one even when it sounds like the outdated option. In several zones that classic version was missing or incomplete in every available map pack, which showed up in-game as black, unreadable text and sparse/missing NPC data. Wooz Maps fixes that: correct, complete zone layouts combined with a consistent, high-contrast color scheme, and NPC/POI data cross-referenced and merged in from multiple sources where the primary source was incomplete.

> **This pack is built specifically for [EverQuest Legends](https://www.everquestlegends.com/home).** It is not intended for and has not been tested against standard EverQuest live servers or emulators — several zones here have EQ Legends-specific layouts, NPCs, and content that don't exist in classic EverQuest. See also the [EQL Wiki](https://eqlwiki.com/) for general game info.

## Download

**[⬇ Download ZIP](https://github.com/ATENHARA/wooz-maps/archive/refs/heads/master.zip)**

Or clone it:
```
git clone https://github.com/ATENHARA/wooz-maps.git
```

Either way, what you get is a folder (`wooz-maps` or `wooz-maps-master`) containing all the zone `.txt` files directly — that folder *is* the map pack.

## Installation

1. Drop the downloaded/cloned folder into your EverQuest Legends `maps` directory, as-is — no need to rename it:
   `<your EQ Legends install>\maps\<folder>\`
2. In-game, open your map settings and select it from the list of available map skins (it'll show up under whatever the folder is named).
3. Recommended map display settings, for the best experience with this pack's dark, high-contrast theme:
   - **Display type:** Minimal Map
   - **Background:** Dark

<sub>Advanced: the skin selection is also stored as `MapSkin=<folder name>` in your `UI_<layout>.ini` files, if you'd rather set it there directly. Note the game rewrites this file when you change skins in-game, so it's not a "set once" file — the in-game menu is the reliable way to do this.</sub>

## Credits

Built on and informed by:
- **[Brewall's Dark Maps](https://www.eqmaps.info/)** — this pack is directly modified from Brewall's Dark Maps; the vast majority of the base geometry, labeling conventions, and dark-theme color palette this project builds on originates there. All credit to Brewall for the original cartography.
- **Dark Good's Maps** — a second community reference pack used for cross-checking colors and geometry.
- EverQuest Legends' own default/legacy map exports — often the most geometrically accurate source for zone layouts, even when their coloring wasn't usable as-is.

## Color legend

Each zone file is plain text, made of two line types:
- **`L` lines** draw geometry — walls, water, terrain features.
- **`P` lines** place point markers — NPCs, zonelines, landmarks, ground spawns.

Both end in an `r, g, b` color. The tables below are a lookup key for reading the map at a glance, and a reference if you want to edit the files yourself — reuse these values rather than inventing new ones, so the pack stays visually consistent.

### Walls & terrain (`L` lines)

| | Color | Meaning |
|---|---|---|
| ![#AFAFAF](https://placehold.co/15x15/AFAFAF/AFAFAF.png) | `175,175,175` | Main walls |
| ![#4B4B4B](https://placehold.co/15x15/4B4B4B/4B4B4B.png) | `75,75,75` | Secondary walls |
| ![#0000FF](https://placehold.co/15x15/0000FF/0000FF.png) | `0,0,255` | Water |
| ![#7F4000](https://placehold.co/15x15/7F4000/7F4000.png) | `127,64,0` | Elevation / ramps |
| ![#007F00](https://placehold.co/15x15/007F00/007F00.png) | `0,127,0` | Foliage / vegetation |
| ![#CD853F](https://placehold.co/15x15/CD853F/CD853F.png) | `205,133,63` | Terrain detail |
| ![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png) | `0,255,0` | Zoneline walls |

### Point markers (`P` lines)

| | Color | Meaning | Example label |
|---|---|---|---|
| ![#FF0000](https://placehold.co/15x15/FF0000/FF0000.png) | `255,0,0` | Zonelines ("to_X" exits) | `to_North_Ro` |
| ![#008000](https://placehold.co/15x15/008000/008000.png) | `0,127,0` / `0,128,0` | Merchants / vendors | `Innkeep_Rille_(General)` |
| ![#FFFFFF](https://placehold.co/15x15/FFFFFF/FFFFFF.png) | `255,255,255` | Landmark buildings | `Freeport_City_Hall` |
| ![#007F7F](https://placehold.co/15x15/007F7F/007F7F.png) | `0,127,127` | Missions / Tasks | `Almon_Juliao_(Task_Master)` |
| ![#00F0F0](https://placehold.co/15x15/00F0F0/00F0F0.png) | `0,240,240` | Raids | `Uzmanya_Zsik_(Raid)` |
| ![#C71585](https://placehold.co/15x15/C71585/C71585.png) | `199,21,133` | Special / notable POI | — |
| ![#BA55D3](https://placehold.co/15x15/BA55D3/BA55D3.png) | `186,85,211` | Craft stations | `Forge`, `Kiln`, `Oven`, `Loom`, `Brew_Barrel` |
| ![#FFE68C](https://placehold.co/15x15/FFE68C/FFE68C.png) | `255,230,140` | GM class trainers | `Trushandra_(GM_Cleric)` |
| ![#FF8C00](https://placehold.co/15x15/FF8C00/FF8C00.png) | `255,140,0` | Named / Hunter-tagged mobs | `Dreadfang_(Hunter,Roam,HS)` |
| ![#8CC8FF](https://placehold.co/15x15/8CC8FF/8CC8FF.png) | `140,200,255` | Generic NPC / mob markers | plain named NPCs, roam mobs, bosses |
| ![#1E90FF](https://placehold.co/15x15/1E90FF/1E90FF.png) | `30,144,255` | `GS:` ground spawns (loot pickups) | `GS:_Old_Silver_Coin` |
| ![#AFAFAF](https://placehold.co/15x15/AFAFAF/AFAFAF.png) | `175,175,175` | Map credit / legend text (not an NPC) | `Revised_Map:_Brewall_Rainsinger...` |

## Zones with full manual rework

Beyond the pack-wide color conventions above, these zones got a full rebuild — correct layout sourced from the most complete/accurate map data available, cross-referenced NPC/POI data merged in from multiple sources, and the full color treatment applied by hand:

Arena, Lavastorm, Innothule (+ Innothuleb), West Commons, Nektulos Forest, East Commons, West Freeport, North Freeport, East Freeport, Northern Desert of Ro, Oasis of Marr, Southern Desert of Ro, Temple of Cazic Thule (partial — mob color fix).

The rest of the pack is Brewall's Dark Maps as a base, with the pack-wide color conventions above applied on top.

## Known limitations

- Not every zone has been individually verified for layout accuracy — the zones listed above got full manual review, the rest inherit Brewall's original geometry.
- A handful of zones have two internal shortnames (a modern redesign and an older "classic" version); if you notice a zone with black or missing text, it may be the classic-named file that hasn't been reworked yet.
- This is a personal project without an issue tracker or PR process — if you find something worth fixing, feel free to fork it (see License).

## License

Public domain — see [LICENSE](LICENSE). Use it however you'd like.
