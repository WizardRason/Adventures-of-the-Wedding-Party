---
publish: true
title: Quest List
created: 2026-03-22T23:17:01.532-04:00
modified: 2026-05-08T13:58:16.000-04:00
---

Quests of the [[Wiki/Organizations/Wedding Party]], the complete, the unrewarded, and the history

```base
filters:
  and:
    - file.inFolder("Wiki/Quests")
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
    groupBy:
      property: Complete
      direction: ASC
    order:
      - file.name
      - Quest-Giver
      - Location
      - Reward
      - Complete
      - Collected
    sort: []
    columnSize:
      file.name: 159
      note.Quest-Giver: 123
      note.Location: 105
      note.Reward: 149
    rowHeight: medium
```

```base
filters:
  and:
    - file.inFolder("Wiki/Quests")
    - file.name != "index"
properties:
  note.Complete:
    displayName: Done
  file.name:
    displayName: Quest
views:
  - type: table
    name: Completed
    filters:
      and:
        - Collected == true
    groupBy:
      property: Complete
      direction: ASC
    order:
      - file.name
      - Quest-Giver
      - Location
      - Reward
    sort: []
    columnSize: {}
    rowHeight: medium

```