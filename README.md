# v1024_logistics_guidance
Some QOL tools to manually adjust logistics efficiency in X4 Foundations.

- Our GitHub repo: https://github.com/Vectorial1024/v1024_logistics_guidance
  - Detailed changelog: https://github.com/Vectorial1024/v1024_logistics_guidance/blob/master/CHANGELOG.md
  - Advanced users may make use of commit tags
- Our EgoSoft Forums link: https://forum.egosoft.com/viewtopic.php?t=473891
- Our Steam Workshop link: (WIP)
- Our Nexus Mods link: (WIP)

> Improve your stations; improve your logistics!

(NPC stations not affected.)

------

## Quick Info
TL;DR: limit the operational range(s) of your stations. Mostly save-compatible because this will involve some player configs.

This mod modifies the vanilla trading, mining, and salvage scripts to let players manipulate their logistics, and so perhaps it's easier to set up and run logistics networks:
- Limit trading range: traders may only find trade offers within the same sector
- Limit mining range: miners may only mine minerals/gases within the same sector
- Limit salvage range: salvagers may only use scraps/wrecks within the same sector

These options are found in the Custom Actions section towards the bottom of the right-click menu of player-owned stations.

Currently, these range restrictions apply separately, so e.g. miners must stay at home while (export) traders can go outside.

## Motivation

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

## Use Cases
- Local "mining stations" that only collects minerals/gases
- Regional warehouses move the minerals/gases to refineries (located in population centres)
- Refineries sell products between each other, and also back to the warehouses
- Advanced factories all trade with the warehouse for resources
