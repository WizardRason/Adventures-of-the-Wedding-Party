---
publish: true
title: Quest List
created: 2026-03-23T03:17:01.532Z
modified: 2026-05-17T00:44:03.406Z
published: 2026-05-17T00:44:03.406Z
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
