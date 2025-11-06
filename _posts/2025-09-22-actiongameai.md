---
layout: post
title:  "Action Game AI"
summary: "AI Engineer"
date:   2025-09-22
preview: /assets/postpreview.png
---

- Designed meelee and ranged NPCs to fight the player
- NPCs can be given a patrol path that they will guard
- NPCs will investigate noises they hear or enemies they see
- If an NPCs health gets too low they will flee combat and break line of sight in order to heal

Behavior Trees:

![Picture 1](/assets/action_btbase.png)

- Meelee NPC with strafe around the player and attack in intervals
- Uses a query around the player to find a good position to attack from

![Picture 2](/assets/action_btmelee.png)

- Ranged NPC will find a suitable position and shoot at the player then reposition
- Uses a query in line of sight to the player, preferrably farther away, and repositions to a nearby point

![Picture 3](/assets/action_btranged.png)

Sub-Trees:

![Picture 4](/assets/action_stfrozen.png)

![Picture 5](/assets/action_stinvestigating.png)

![Picture 6](/assets/action_stpassive.png)

Tasks & Enviromental Queries:

![Picture 7](/assets/action_bttpatrol.png)

![Picture 8](/assets/action_eqscover.png)

![Picture 9](/assets/action_eqsrangedlocation.png)

![Picture 10](/assets/action_eqsstrafe.png)

Enemy Blueprints:

![Picture 11](/assets/action_bpbase.png)

![Picture 12](/assets/action_bpmelee.png)

![Picture 13](/assets/action_bpranged.png)

AI Controller:

![Picture 14](/assets/action_aic.png)

Blackboard:

![Picture 15](/assets/action_bbbase.png)

Blueprint Interfaces & Damage Struct:

![Picture 16](/assets/action_bpienemyai.png)

![Picture 17](/assets/action_bpidamage.png)

![Picture 18](/assets/action_sdamage.png)
