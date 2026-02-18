# Change log
This is a detailed changelog of Logistics Guidance.

## Version 1.01 (2026-02-17)
Bugfix update.
- Fixed range control settings being applied to all player-owned stations at once.
  - The technical reason is mistaking `.{$idcode}` (correct) with `.$idcode` (wrong).

## Version 1.00 (2026-02-17)
Initial release.
- Station operational range can be limited by the player (see README for more details)
  - Sector/Cluster range limiting
  - Separate controls for trading/mining/salvaging
  - This may improve logistics efficiency in some cases
