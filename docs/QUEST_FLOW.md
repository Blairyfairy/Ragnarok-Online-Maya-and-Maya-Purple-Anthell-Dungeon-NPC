# Quest & Dialogue Flow

## NPC Personality

**Name:** Maya the Queen (or “Queen’s Envoy”)  
**Tone:** Elegant, regal, slightly mysterious, proud of her ant colony.  
She speaks as if she is an extension of the true Maya MVP – a guardian of the nest who helps worthy adventurers.

---

## Main Menu Structure

```
1. Exchange for Maya Card
2. Exchange for Maya Purple Card
3. Claim Maya Crown & Gear (requires previous trades / materials)
4. Learn about Ant Hell rarities
5. Goodbye
```

---

## Flow 1 – Maya Card Exchange

1. Player selects “Exchange for Maya Card”.
2. NPC lists acceptable trade-in cards (configurable array).
3. Player chooses which card to offer.
4. Script checks:
   - Has the required card?
   - Has enough zeny?
   - Has optional materials (Mother’s Nightmare / Queen’s Hair Ornament)?
5. Confirmation dialogue.
6. Delete items → give Maya Card → success message + optional small reward.

Alternative paths (same menu):
- Maya Purple Card → Maya Card (upgrade)
- Multiple lower cards + rare material

---

## Flow 2 – Maya Purple Card Exchange

Similar structure but lower requirements.  
Focus on utility (detect hidden) rather than pure power.

---

## Flow 3 – Maya Crown & Gear Pack

**Requirements (all must be true):**
- Player has obtained at least one Maya Card through the NPC **or** already owns a Maya Card.
- Has Queen’s Hair Ornament
- Has Armlet of Obedience
- Has enough zeny (default 10M)

**Rewards:**
1. Maya Crown (upper headgear)
2. Ant Queen Brooch (accessory)
3. Purple Antennae (middle headgear / costume)
4. Optional: 1× Safety Ring or Tiara

After claiming, a flag is set so the player cannot claim again (or can claim once per character).

---

## Sample Dialogue Snippets

**Greeting:**
> “Welcome, traveler… You stand before the threshold of my nest.  
> I am the Queen’s voice. Do you seek the power of Maya’s reflection,  
> or the eyes that pierce the shadows?”

**Successful Maya Card trade:**
> “The magic of the Queen now rests in your shield.  
> Use it wisely – few are granted her reflection.”

**Maya Crown claim:**
> “You have proven yourself a true friend of the colony.  
> Wear this crown, and let the ants of Ant Hell recognize you as kin.”

---

## Variables Used (rAthena style)

- `MAYA_TRADE_DONE` – character variable, set after first major trade
- `MAYA_CROWN_CLAIMED` – prevents re-claiming the gear pack

These can be changed to account variables if desired.
