# v1024_logistics_guidance
Some QOL tools to manually adjust logistics efficiency in X4 Foundations.

- Our GitHub repo: https://github.com/Vectorial1024/v1024_logistics_guidance
  - Detailed changelog: https://github.com/Vectorial1024/v1024_logistics_guidance/blob/master/CHANGELOG.md
  - Advanced users may make use of commit tags
- Our EgoSoft Forums link: https://forum.egosoft.com/viewtopic.php?t=473891
- Our Steam Workshop link: https://steamcommunity.com/sharedfiles/filedetails/?id=3668059212
- Our Nexus Mods link: https://www.nexusmods.com/x4foundations/mods/1982

> Improve your stations; improve your logistics!

(NPC stations not affected.)

------

## Quick Info
TL;DR: limit the operational range(s) of your stations. Mostly save-compatible because this will involve some player configs.

This mod modifies the vanilla trading, mining, and salvage scripts to let players manipulate their logistics, and so perhaps it's easier to set up and run logistics networks:
- Limit trading range: traders may only find trade offers within the same sector
- Limit mining range: miners may only mine minerals/gases within the same sector
- Limit salvage range: salvagers may only use scraps/wrecks within the same sector
- Limit trading direction: traders may only perform buy/sell deals for the station

These options are found in the Custom Actions section towards the bottom of the right-click menu of player-owned stations.

Currently, these range restrictions apply separately, so e.g. miners must stay at home while (export) traders can go outside.

There are two kinds of range limit:
- Sector range: limits activities to be within the hexagon that the station is at
- Cluster range: limits activities to be within the *large* hexagon that the station is at
  - Example of a multi-sector cluster: Grand Exchange
  - Option is hidden if cluster has only 1 sector

## Motivation

### Trade operational range

One big inspiration of this mod came from X: Rebirth. There, the trading operational range of stations can be switched between the Zone level, the Sector level, and (with Comms Relay upgrade) the System level. This allows the following hypothetical setup:
- Zone-level/Sector-level stations that always trade with each other
- System-level stations (especially warehouses) that act as ware balancers

This setup has the following benefits:
- Minimize local trading waiting time
- Minimize number of ships used, both locally (e.g. use S/M traders for fast action), and globally (e.g. use L/XL traders for bulk movement)
- Easy to scale up:
  - Easy to apply to new stations
  - Easy to increase logistics throughput (just use more ships!)
- Possible performance improvements due to limited ranges

... while also having the following drawbacks:
- Not suitable for early game
- Indirection: local traders must go through warehouses in case resources are available just next sector

### Trade direction

It is difficult to isolate a singular motivation for this concept, but we may easily find the following:
- Players overuse the "Repeat Orders" behavior to "push" wares to other places
- There are mods that provide custom trade behaviors to "push" wares to other places
- There are mods that literally has station trade rule presets to let players "push" wares to other places
- Players sometimes want to have a station to "interface" their trade with NPCs

Granted, the default trading script does not greatly prioritize buy/sell behaviors (except for shortages, added later), but we see the theme:
- We may want to let stations actively "push"/"pull" wares

This is perhaps "factory-like", and this can be easily achieved by slightly tweaking the vanilla AutoTrade script to skip entire behavior blocks.

This setup has the following benefits:
- Actual supply chain: wares can be definitely seen being pushed to other stations
- Optimize for ship usage
  - e.g., export-only fleet of S traders for a drug production station
- Greater general compatibility; this is still a variation on the vanilla AutoTrade script

... while also having the following drawbacks:
- Supply chain fragility: if some station can't send ships quick enough, then the entire system stalls

But perhaps this is what players want, to really control station import/export in X4 Foundations to really embrace the "galactic supply chain" dream.

## Use Cases
- Local "mining stations" that only collects minerals/gases
- Regional warehouses move the minerals/gases to refineries (located in population centres)
- Refineries sell products between each other, and also back to the warehouses
- Advanced factories all trade with the warehouse for resources
- Functioning intake/outflow warehouses to balance ware levels with NPC stations
- Active pushing of products (still checks prices; use auto-price!)
