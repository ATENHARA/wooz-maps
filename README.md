# Wooz Maps

A custom, high-contrast map pack for **EverQuest Legends**, built for use with the game's built-in map viewer.

This started as a recolor of [Brewall's Map Pack](https://alla.clumsysworld.com/brewalls_maps.php) toward a darker, higher-contrast aesthetic, but grew into something more involved: many EverQuest Legends zones exist under two different internal names — a modern redesigned version and an older "classic" version — and the game frequently loads the classic one even when it sounds like the outdated option. In several zones that classic version was missing or incomplete in every available map pack, which showed up in-game as black, unreadable text and sparse/missing NPC data. Wooz Maps fixes that: correct, complete zone layouts combined with a consistent, high-contrast color scheme, and NPC/POI data cross-referenced and merged in from multiple sources where the primary source was incomplete.

## Installation

1. Copy the `Wooz Maps` folder into your EverQuest Legends `maps` directory:
   `<your EQ Legends install>\maps\Wooz Maps\`
2. In your UI config (`UI_<layout>.ini`), set:
   ```
   MapSkin=Wooz Maps
   ```

## Credits

Built on and informed by:
- [**Brewall's Map Pack**](https://alla.clumsysworld.com/brewalls_maps.php) — the original community EverQuest cartography this pack is derived from.
- **Dark Good's Maps** — a second community reference pack used for cross-checking colors and geometry.
- EverQuest Legends' own default/legacy map exports — often the most geometrically accurate source for zone layouts, even when their coloring wasn't usable as-is.

## Color conventions

| Element | Color |
|---|---|
| Main walls | `175,175,175` |
| Secondary walls | `75,75,75` |
| Water | `0,0,255` |
| Elevation / ramps | `127,64,0` |
| Foliage / vegetation | `0,127,0` |
| Terrain detail | `205,133,63` |
| Zoneline walls | `0,255,0` |
| Zoneline points ("to_X") | `255,0,0` |
| Special / POI marker | `199,21,133` |
| Merchants / vendors | `0,127,0` / `0,128,0` |
| Landmark buildings | `255,255,255` |
| Missions / Tasks | `0,127,127` |
| Raids | `0,240,240` |
| Craft stations (Forge, Kiln, Oven, Loom, Brew Barrel, etc.) | `186,85,211` |
| GM class trainers | `255,230,140` |
| Generic NPC / mob markers | `140,200,255` |
| Map credit / legend text | `175,175,175` |

## License

Public domain — see [LICENSE](LICENSE). Use it however you'd like.
