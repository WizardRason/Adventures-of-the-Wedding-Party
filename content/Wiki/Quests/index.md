---
publish: true
title: Quest List
created: 2026-03-22T23:17:01.532-04:00
modified: 2026-05-08T23:05:16.000-04:00
published: 2026-05-08T23:05:16.000-04:00
---

Quests of the [[Wedding Party]], the complete, the unrewarded, and the history

![[Quest List]]

![[Quests.base]]

| Quest                                                               | Quest Giver                                   | Location                                | Reward                      |
| ------------------------------------------------------------------- | --------------------------------------------- | --------------------------------------- | --------------------------- |
| [[Wiki/Quests/Butterskull Ranch Quest.md\|Butterskull Ranch Quest]] | Quest Board                                   | [[Wiki/Places/Phandalin.md\|Phandalin]] | 100gp                       |
| [[Wiki/Quests/Marsh Hag.md\|Marsh Hag]]                             | Mama Mary                                     | Mere of Dead Men                        | Return of Doe's soul        |
| [[Wiki/Quests/Phandalin Election.md\|Phandalin Election]]           | [[Wiki/People/Phandalin/Sildar.md\|Sildar]]   | [[Wiki/Places/Phandalin.md\|Phandalin]] | Reduced Zhentarim Influence |
| [[Wiki/Quests/Attacks at the Mine.md\|Attacks at the Mine]]         | [[Wiki/People/Phandalin/Gundren.md\|Gundren]] | [[Wiki/Places/Phandalin.md\|Phandalin]] | Unknown                     |

# Completed

| Quest                                                                                           | Quest Giver                                                 | Location                                    | Reward                    | Paid |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------- | ------------------------------------------- | ------------------------- | ---- |
| [[Wiki/Quests/Spell book of Bogentle.md\|Spell book of Bogentle]]                               | [[Wiki/People/Phandalin/Sister Garaele.md\|Sister Garaele]] | [[Wiki/Places/Phandalin.md\|Phandalin]]     | 2 Health Potions          | ☑    |
| [[Wiki/Quests/Secure Aid from Neverwinter.md\|Secure Aid from Neverwinter]]                     | [[Wiki/Organizations/Lords' Alliance.md\|Lords' Alliance]]  | [[Wiki/Places/Neverwinter.md\|Neverwinter]] | Aid for Phandalin         | ☐    |
| [[Wiki/Quests/Deliver Letter to the Lords’ Alliance.md\|Deliver Letter to the Lords’ Alliance]] | [[Wiki/People/Phandalin/Sildar.md\|Sildar]]                 | [[Wiki/Places/Phandalin.md\|Phandalin]]     | Guards for Phandalin      | ☐    |
| [[Wiki/Quests/Save the Rockseekers.md\|Save the Rockseekers]]                                   | [[Wiki/People/Phandalin/Gundren.md\|Gundren]]               | [[Wiki/Places/Phandalin.md\|Phandalin]]     | Influence in the election | ☐    |
| [[Wiki/Quests/Umbrage Hill Quest.md\|Umbrage Hill Quest]]                                       | Quest Board                                                 | [[Wiki/Places/Phandalin.md\|Phandalin]]     | 25gp                      | ☑    |

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
