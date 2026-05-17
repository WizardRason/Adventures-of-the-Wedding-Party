---
publish: true
title: Quest List
created: 2026-03-22T23:17:01.532-04:00
modified: 2026-05-16T20:44:03.406-04:00
published: 2026-05-16T20:44:03.406-04:00
---

Quests of the [[Wedding Party]], the complete, the unrewarded, and the history

```base
filters:
  and:
    - file.inFolder("Quests")
    - file.name != "index"
properties:
  note.Complete:
    displayName: Done
  file.name:
    displayName: Quest
views:
  - type: table
    name: Available
    filters:
      and:
        - Collected == false
        - Complete == false
    order:
      - file.name
      - Quest-Giver
      - Location
      - Reward
    sort: []
    columnSize: {}
    rowHeight: medium
  - type: table
    name: Complete
    filters:
      and:
        - Collected == true
    order:
      - file.name
      - Quest-Giver
      - Location
      - Reward
    sort: []
    columnSize: {}
    rowHeight: medium
  - type: table
    name: Uncollected
    filters:
      and:
        - Collected == false
        - Complete == true
    order:
      - file.name
      - Quest-Giver
      - Location
      - Reward
    sort:
      - property: Location
        direction: ASC
    columnSize: {}
    rowHeight: medium

```
