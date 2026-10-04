# Balance & Design Notes

## Design Goals

1. **Make Maya Card & Maya Purple Card more accessible** without removing the satisfaction of farming Ant Hell.
2. **Reward players who already farm the dungeon** by giving them a meaningful sink for surplus rare drops (Mother’s Nightmare, Queen’s Hair Ornament, etc.).
3. **Create a fair conversion path** between cards of similar power / rarity.
4. **Give exclusive cosmetic + useful gear** (Maya Crown + smaller items) so completing the trades feels rewarding beyond just the card.

---

## Suggested Trade Ratios (Configurable)

### Maya Card (Shield – Magic Reflect)

| Requirement                                      | Cost (zeny) | Notes |
|--------------------------------------------------|-------------|-------|
| 1× comparable MVP card (Phreeoni, Drake, Eddga, Mistress, Moonlight Flower, etc.) | 5 000 000 | Core exchange |
| 1× Maya Purple Card + 1× Mother’s Nightmare      | 2 000 000 | Upgrade path |
| 3× high-tier mini-boss cards + Queen’s Hair Ornament | 3 000 000 | Alternative |
| 1× any other Earth/Insect MVP card + Armlet of Obedience | 4 000 000 | Thematic |

### Maya Purple Card (Headgear – Detect Hidden)

| Requirement                                      | Cost (zeny) | Notes |
|--------------------------------------------------|-------------|-------|
| 2–3× mid-tier cards + 1× Safety Ring or Tiara    | 1 500 000 | Entry-level |
| 1× Mother’s Nightmare + 500k zeny                | —           | Rare material path |
| 5× random cards (any) + Queen’s Hair Ornament    | 1 000 000 | Quantity path |

### Maya Crown (the “Maya Hat”) + Gear Pack

Requires:
- Maya Card **or** successful major trade
- Queen’s Hair Ornament
- Armlet of Obedience
- 10 000 000 zeny (or adjustable)

Rewards:
- **Maya Crown** (upper headgear)
- Ant Queen Brooch (accessory)
- Purple Antennae (middle/lower headgear or costume)
- Optional: +1 Safety Ring or Tiara

---

## Power Level Comparison (MVP Cards)

Cards considered roughly equal in power/rarity for trading:

**High-tier / desirable:**
- Maya Card
- Tao Gunka Card
- GTB (Golden Thief Bug) Card
- Dark Lord Card
- Baphomet Card
- Stormy Knight Card
- etc.

**Mid-high (good trade-ins for Maya):**
- Phreeoni Card
- Drake Card
- Eddga Card
- Mistress Card
- Moonlight Flower Card
- Dracula Card
- Amon Ra Card (depending on server rates)

**Mini-boss / utility:**
- Maya Purple Card (detect hidden – extremely useful)
- Angeling / Deviling
- Mastering, etc.

Adjust the script arrays to match your server’s economy and rates.

---

## Rate Recommendations

| Server Type       | Suggested Multiplier on zeny cost | Notes |
|-------------------|-----------------------------------|-------|
| Low rate (1x–5x)  | 1.0×                              | Keep as written |
| Mid rate (10x–50x)| 0.5–0.7×                          | Reduce zeny |
| High rate (100x+) | 0.2–0.4× or remove zeny           | Focus on card + material requirements |

Always keep at least one rare Ant Hell material required so the dungeon still feels relevant.

---

## Anti-Abuse Notes

- The script uses `countitem` + `delitem` safely.
- Consider adding a daily / weekly limit if your server is high-rate.
- Cards given must be unbound / tradeable (script checks can be added).
- The Maya Crown is intended to be **account-bound or character-bound** on most servers (set the appropriate item flag).

---

## Future Expansion Ideas

- Add a small daily quest that gives a “Maya Token” usable toward the trades.
- Create a set bonus when wearing Maya Crown + Ant Queen Brooch + Purple Antennae.
- Allow trading multiple Maya Purple Cards into a stronger “Queen’s Gaze” headgear.
