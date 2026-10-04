# Maya Anthell Card Trader & Gear NPC

**Custom rAthena / Hercules NPC pack** for Ragnarok Online private servers.

An elegant ant-queen inspired NPC stationed **outside Ant Hell** (near the desert entrances).  
She trades **Maya Card**, **Maya Purple Card**, and other hard-to-obtain Ant Hell drops for equivalent-power MVP cards, rare materials, and exclusive gear rewards including the **Maya Crown / Maya Hat** and smaller insect-themed accessories.

Inspired by the Queen Maya (MVP) and her mate Maya Purple (mini-boss) from the Ant Hell dungeon (`anthell01` / `anthell02`).

---

## Features

- **Card Exchange Quests**  
  Trade other MVP / mini-boss cards of similar rarity/power for Maya Card or Maya Purple Card.
- **Material & Drop Trades**  
  Exchange hard-to-get Ant Hell items (Mother's Nightmare, Queen's Hair Ornament, Armlet of Obedience, Dea Staff, etc.) + zeny or other cards for the desired Maya cards.
- **Exclusive Rewards**  
  Completing major trades or a short quest chain rewards:
  - **Maya Crown** (custom headgear – “Maya Hat”)
  - Smaller gear: Ant Queen Brooch, Purple Antennae, Safety Ring variants, insect-themed accessories.
- **Balanced for mid-to-late game**  
  Designed so players who farm Ant Hell or other MVPs can convert surplus cards into the highly sought-after Maya / Maya Purple cards without pure RNG.
- **Fully documented**  
  Installation guides, item definitions, script explanations, and balance notes inside `/docs`.

---

## Quick Start

1. Copy the contents of `/npc` into your server’s `npc/custom/` folder.
2. Add the item definitions from `/db` (or `/items`) to your item database.
3. Add the mapflag / spawn line (see docs) so the NPC appears outside Ant Hell.
4. `@reloadscript` (or restart) and test.

Full step-by-step instructions → [docs/INSTALLATION.md](docs/INSTALLATION.md)

---

## Folder Structure

```
maya-anthell-npc/
├── README.md                 ← you are here
├── LICENSE
├── docs/
│   ├── INSTALLATION.md       ← how to implement on rAthena / Hercules
│   ├── BALANCE.md            ← design notes & suggested rates
│   ├── QUEST_FLOW.md         ← dialogue & trade logic overview
│   └── CUSTOM_ITEMS.md       ← Maya Hat + smaller gear details
├── npc/
│   └── maya_anthell_trader.txt   ← main NPC script
├── db/
│   ├── item_db_maya.yml      ← new custom items (YAML format)
│   └── item_db_maya.txt      ← legacy .txt format (pre-renewal style)
├── items/
│   └── item_info_maya.lua    ← client-side item info (optional)
└── scripts/
    └── maya_hat_bonus.txt    ← example script bonuses
```

---

## NPC Location (Recommended)

Place the NPC just outside the Ant Hell entrances in the Sograt Desert:

- Near `moc_fild20` (classic entrance area) or  
- Near the modern Sanderman Fortress entrance (post-Renewal).

Suggested coordinates (adjust to your map):  
`moc_fild20, 210, 250` or `moc_fild04, 150, 300`

Sprite suggestions:  
- `4_F_MAYA` (if available)  
- `4_F_KAFRA8` / custom ant-queen look  
- Or any elegant female insect-themed sprite.

---

## Core Trade Examples

| You give                                      | You receive                  |
|-----------------------------------------------|------------------------------|
| 1× comparable MVP card (e.g. Phreeoni, Drake, Eddga, Mistress…) + 5M zeny | Maya Card                   |
| 1× Maya Purple Card + materials               | Maya Card (upgrade path)    |
| 3–5 random high-tier cards + Mother’s Nightmare | Maya Purple Card            |
| Maya Card + Queen’s Hair Ornament + Armlet of Obedience | **Maya Crown** (hat) + smaller gear pack |
| Full quest completion                         | Maya Crown + Ant Queen Brooch + Purple Antennae |

Exact ratios are configurable in the script and documented in `/docs/BALANCE.md`.

---

## Hard-to-Get Ant Hell Items Used

- **Mother’s Nightmare** (very rare – used in Mysteltainn creation)
- **Queen’s Hair Ornament**
- **Armlet of Obedience**
- **Tiara / Safety Ring**
- **Dea Staff [1]**
- **Maya Card** (0.01–0.02%)
- **Maya Purple Card** (detect hidden – highly valued)

These items are intentionally required so the NPC feels like a natural extension of the dungeon economy.

---

## Requirements

- rAthena or Hercules emulator
- Item database editable (YAML or .txt)
- Basic knowledge of adding custom NPCs and items
- Optional: custom headgear sprites for the Maya Crown

---

## Credits & Inspiration

- Original monsters: Gravity / RO Maya & Maya Purple
- Design goal: Make rare Ant Hell cards more accessible through meaningful trades while rewarding dungeon farmers with unique gear.
- Inspired by classic card-trader NPCs and modern private-server quality-of-life features.

---

## Contributing

Feel free to open issues or PRs for:
- Additional trade combinations
- More custom gear
- Client sprite packs
- Renewal vs Pre-Renewal balance variants

---

**Enjoy your Ant Hell adventures, and may the Queen smile upon your card drops!**  
🐜👑
