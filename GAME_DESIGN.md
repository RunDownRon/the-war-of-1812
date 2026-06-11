# The War of 1812 — Game Design Document

## Overview
A turn-based strategy board game in the style of Axis & Allies, set during the War of 1812. 
Playable as single player (control both sides) with multiplayer planned for a later stage.
Built as a browser-based game, eventually packaged as a downloadable desktop app.

---

## Factions

### Americans
- Invading force pushing into Canada
- Suffer fear penalties when facing Indigenous warriors
- Must manage morale to avoid surrendering forts without a fight

### British / Canadians
- Defending Canada from American invasion
- Rely heavily on Indigenous alliances to hold the frontier
- Must balance war funding against fair treatment of Indigenous allies

### Indigenous Nations (Allied with British)
- Led by Tecumseh's Confederacy
- Not just a military unit — a full strategic partner
- Central to the economic fur trade in the northern territories
- Their effectiveness rises and falls based on how fairly they are treated

### France (Background Factor — not a playable faction)
- Not on the map — represented as a background modifier
- Reduces the size of British annual convoys in early years
- Napoleon's defeat in 1814 triggers larger British convoys to Canada

---

## Map

### North American Theater

**Land Territories:**
- Upper Canada (Ontario region)
- Lower Canada (Quebec region)
- Nova Scotia / New Brunswick
- Northern Territories (fur trade zone — economic, not military)
- American Northwest (Ohio, Indiana, Michigan)
- American Northeast (New York, Vermont, New England)
- Mid-Atlantic (Pennsylvania, Maryland, Virginia)
- The South (Georgia, Tennessee, Louisiana / New Orleans)
- Spanish Florida
- The Western Frontier

**Naval Zones:**
- Lake Ontario
- Lake Erie
- Lake Champlain
- Gulf of St. Lawrence
- Atlantic Coast (North)
- Atlantic Coast (South)
- North Atlantic (British annual convoy route)

**Victory Cities:**

*Canadian / British:*
- York (Toronto)
- Montreal
- Hull
- Quebec City
- Kingston (main British naval base on Lake Ontario)
- Niagara (key border crossing, heavily contested)
- Queenston Heights (where Isaac Brock fell — significant early British victory)
- Lundy's Lane (one of the bloodiest battles of the war, Niagara corridor)

*American:*
- Detroit
- Washington D.C.
- New Orleans
- Sackett's Harbour (main American naval base on Lake Ontario)
- Plattsburgh (key northern New York)
- Baltimore (famously attacked by British — Star Spangled Banner)

---

## Core Mechanics

### Combat System
Based on Axis & Allies dice rolling. Each unit has an attack value and a defense value.
Roll at or under your value to score a hit.

### Unit Types
- Infantry
- Artillery
- Cavalry
- Naval Vessels (Frigates, Gunboats)
- Forts (defensive structures, not mobile)
- Indigenous Warriors (special rules apply)

---

## Indigenous Nations Mechanics

### Alliance / Morale Track
A visible meter that shifts based on British player actions each turn.

**Raises morale:**
- Generous or very generous trade terms
- Honoring territorial agreements
- Winning battles that protect Indigenous lands
- Keeping promises

**Lowers morale:**
- Exploitative trade terms
- Taking Indigenous lands
- Breaking treaties
- Losing battles that expose their territories

### Combat Stats by Morale Level

| Morale Level | Attack Roll | Defense Roll | Available Units |
|---|---|---|---|
| High | hits on 1-3 | hits on 1-4 | Full strength |
| Medium | hits on 1-2 | hits on 1-3 | Reduced numbers |
| Low | hits on 1-1 | hits on 1-2 | Skeleton force |
| Broken | no attack | no defense | Withdraw completely |

### Terrain Bonus
Indigenous warriors always get combat bonuses in forests, wilderness, and northern territories 
regardless of morale level — they are naturally more effective in their home terrain.

### Fear Factor
When Indigenous warriors are present in battle, American units suffer penalties:
- -1 to American dice rolls
- Chance of automatic American retreat before battle begins
- Increased chance of fort/garrison surrender
- American morale track drops in affected territories

### The Trade Terms Mechanic
Each turn the British player sets trade terms with Indigenous nations:

| Trade Terms | British Income | Indigenous Morale Effect |
|---|---|---|
| Exploitative | High | Drops each turn |
| Fair | Medium | Stays stable |
| Generous | Low | Rises each turn |
| Very Generous | Minimal | Rises fast + loyalty bonus |

**Design philosophy:** The most ethical strategy is also the most effective one. 
Players who treat Indigenous nations fairly win more decisively.

### Northern Territories / Fur Trade
- The northern wilderness is an economic zone, not a combat zone
- Generates fur trade income each turn if controlled
- Indigenous nations have natural influence and bonus here
- British players need Indigenous allies to fully exploit it
- Income scales with morale — broken relations = no fur trade income

---

## Fear Factor & Psychological Warfare

### Fort Surrender Mechanic
When attacking a fort with Indigenous warriors present, roll for psychological surrender 
BEFORE combat begins. Influenced by:
- Number of Indigenous warriors present
- Whether Tecumseh is present (major bonus)
- Current American morale level
- Size of the defending garrison

A successful roll = fort surrenders with no casualties. Entire garrison captured.
*Based on the real surrender of Fort Detroit in 1812.*

### American Counter-Fear Options
Americans can reduce fear penalties through:
- Building up fort defenses
- Experienced officers present in garrison
- Boosting troop morale through recent victories
- Maintaining a high American morale track

---

## Named Hero Units

One-of-a-kind powerful units. **Permanently lost if killed in battle** — just like history.

### Tecumseh (Indigenous / British)
- Multiplies fear factor dramatically
- Boosts Indigenous warrior morale and combat stats
- Presence alone can trigger fort surrender rolls
- His death is a catastrophic blow to Indigenous morale

### Isaac Brock (British / Canadian)
- Boosts British Canadian defensive stats
- Bonus to coordinated British/Indigenous attacks
- His death weakens Canadian defensive capability

### Andrew Jackson (American)
- Boosts American forces in the southern theater
- Reduces fear penalties for units under his command
- Key figure for the New Orleans campaign

---

## Victory Conditions

### Military Victory + High Indigenous Morale — Best Ending
Canada is defended, alliances are honored, Indigenous nations retain their territories.
A strong foundation built on fairness and mutual respect.

### Military Victory + Low Indigenous Morale — Hollow Victory
Canada is defended but relations are damaged. Northern territories weakened.

### Military Victory + Broken Relations — Pyrrhic Victory
The war is won but Indigenous nations have withdrawn. The country is weaker for it.
A cautionary outcome.

---

## Seasons & Weather

### Season Cycle
Every 2 turns the season changes. A full year = 8 turns. Full game = ~24 turns (1812-1815).

```
Turns 1-2  → Summer
Turns 3-4  → Autumn
Turns 5-6  → Winter
Turns 7-8  → Spring
Turns 9-10 → Summer
...and so on
```

### Season Effects

**Summer (turns 1-2)**
- Full movement for all units
- No supply penalties
- Best time to launch major offensives

**Autumn (turns 3-4)**
- Movement slightly reduced
- Build supply depots and prepare for winter
- Creates urgency — push now or wait until spring

**Winter (turns 5-6)**
- Movement heavily reduced
- Exposed American units take attrition damage every turn
- Supply drains faster
- Indigenous warriors and British/Canadians unaffected in home territory
- Long-marched armies arrive in terrible condition

**Spring (turns 7-8)**
- Recovery season
- Units slowly regain strength
- Supply lines reopen
- Both sides regroup and plan

### Regional Winter Severity Zones

Winter penalties scale by how far north the territory is:

| Zone | Region | Winter Effect |
|---|---|---|
| Zone 1 | Northern Territories, Upper Canada | Brutal — blizzards possible, units lose health every turn |
| Zone 2 | Great Lakes, Lower Canada | Harsh — significant penalties for unprepared armies |
| Zone 3 | Mid-Atlantic, American Northeast | Cold — moderate penalties, manageable with supply |
| Zone 4 | The South (Tennessee, Georgia, Louisiana) | Mild — minimal penalties |
| Zone 5 | Florida, Gulf Coast | None — essentially no winter penalties |

### Supply & Attrition
- Every army has a supply level
- Long marches drain supply
- Winter drains supply faster
- Units that run out of supply take attrition damage before combat
- British/Canadians have supply advantages in home territory
- Americans marching from Kentucky arrive weakened — worse in winter

---

## The Annual British Convoy

There is no European map. Once per year (every 8 turns) a British convoy arrives delivering troops, ships, and supplies. The size reflects how much Britain could spare while dealing with Napoleon.

### Convoy Schedule
| Year | Convoy Size | Reason |
|---|---|---|
| 1812 | Small | Napoleon at full strength — Britain barely spares anything |
| 1813 | Small | Still tied up in Europe |
| 1814 | Large | Napoleon defeated — Britain cuts loose |
| 1815 | Massive | Full British military now available |

### Contents of Each Convoy
- Infantry and artillery units
- Naval vessels
- Supply resources
- Occasionally a named hero or special unit

### Strategic Implications
- Canada largely defends itself in the early game — historically accurate
- Americans need to make serious gains before 1814 or the game tilts heavily toward Britain
- Late game shifts dramatically once the full British military becomes available

---

## Development Roadmap

1. **Single player mode** — build full game, all rules, map, units. Player controls both sides for testing.
2. **Polish** — visuals, balance, bug fixes
3. **Multiplayer** — connect two players over the internet
4. **Packaging** — wrap as downloadable desktop app (Electron)
