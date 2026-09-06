# Change log
This is a detailed changelog of Logistics Guidance.

## Version 1.04 (2026-09-06)
Feature update.
- Station trade direction can be limited by the player (see README for more details)
  - Import only; or Export only
  - This may improve logistics efficiency in some cases

## Version 1.03 (2026-02-20)
Bugfix update.
- Fixed range control settings not persisting at all.
  - The technical reason is that it is difficult to make use of dynamic string keys for the lookup tables.

## Version 1.02 (2026-02-18)
Bugfix update.
- Fixed salvage range control not distinguishing between sector/cluster ranges.
  - The technical reason is a bad patch path.

## Version 1.01 (2026-02-18)
Bugfix update.
- Fixed range control settings being applied to all player-owned stations at once.
  - The technical reason is mistaking `.{$idcode}` (correct) with `.$idcode` (wrong).

## Version 1.00 (2026-02-17)
Initial release.
- Station operational range can be limited by the player (see README for more details)
  - Sector/Cluster range limiting
  - Separate controls for trading/mining/salvaging
  - This may improve logistics efficiency in some cases
