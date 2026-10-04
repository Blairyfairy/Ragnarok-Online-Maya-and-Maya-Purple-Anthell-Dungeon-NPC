# Installation Guide

This guide covers installing the Maya Anthell Card Trader NPC on **rAthena** (recommended) and **Hercules**.

---

## 1. Copy Files

```bash
# From the repo root
cp npc/maya_anthell_trader.txt  /path/to/your/server/npc/custom/
cp db/item_db_maya.yml          /path/to/your/server/db/re/   # or db/pre-re/
# OR for legacy txt format:
cp db/item_db_maya.txt          /path/to/your/server/db/
```

If you use a custom item info system, also copy:
```bash
cp items/item_info_maya.lua     /path/to/client/System/   # or your iteminfo path
```

---

## 2. Register the NPC

Edit your main script loader (usually `npc/scripts_custom.conf` or `npc/scripts_athena.conf`):

```conf
npc: npc/custom/maya_anthell_trader.txt
```

Or add it directly inside an existing custom script file.

---

## 3. Add Custom Items to Database

### rAthena YAML (modern)

Merge the contents of `db/item_db_maya.yml` into your `item_db_equip.yml` / `item_db_etc.yml` (or create a separate import file and include it).

Key new items:
- `Maya_Crown` (headgear – the “Maya Hat”)
- `Ant_Queen_Brooch`
- `Purple_Antennae`
- Optional cosmetic variants

### Legacy .txt format

Append the lines from `db/item_db_maya.txt` to your `item_db.txt`.

---

## 4. Place the NPC on the Map

Open `npc/maya_anthell_trader.txt` and adjust the coordinates at the top:

```
moc_fild20,210,250,4	script	Maya the Queen	4_F_KAFRA8,{
```

Recommended locations outside Ant Hell:

| Map          | Suggested X,Y   | Notes                          |
|--------------|-----------------|--------------------------------|
| moc_fild20   | 210, 250        | Classic desert near entrance   |
| moc_fild04   | 150, 300        | Alternative desert area        |
| moc_fild15   | near warp       | Modern Sanderman Fortress side |

After changing coordinates, `@reloadscript` or restart the map server.

---

## 5. Optional: Client-Side Item Info

If your server uses `itemInfo.lua` / `itemInfo_EN.lua`:

1. Add the descriptions from `items/item_info_maya.lua`.
2. Rebuild the GRF or place the file in the correct System folder.
3. Clients must download the updated item info (or use a diff patch).

---

## 6. Optional: Script Bonuses

If you want the Maya Crown to have special bonuses beyond the database entry, include:

```conf
npc: scripts/maya_hat_bonus.txt
```

(This file contains example OnEquip / OnUnequip scripts.)

---

## 7. Test

1. `@reloadscript`
2. Go to the coordinates.
3. Talk to the NPC.
4. Test a simple trade (e.g. give a test MVP card).
5. Check that the Maya Crown appears correctly in inventory and can be equipped.

---

## Troubleshooting

| Problem                        | Solution                                      |
|--------------------------------|-----------------------------------------------|
| NPC not appearing              | Check coordinates + `@reloadscript`           |
| Item not found                 | Verify item ID is unique and loaded           |
| Script errors on load          | Check for missing commas / syntax in YAML/txt |
| Client shows “Unknown Item”    | Update itemInfo.lua and patch client          |
| Trade accepts wrong cards      | Edit the arrays inside the script             |

---

## Uninstall

1. Remove the NPC line from `scripts_custom.conf`.
2. Delete the custom items from your item database (or comment them out).
3. `@reloadscript` / restart.

---

For balance tuning and quest flow details, see the other files in `/docs`.
