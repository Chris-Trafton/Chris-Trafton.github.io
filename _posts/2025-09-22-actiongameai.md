---
layout: post
title:  "Action Game AI"
summary: "AI Engineer"
date:   2025-09-22
preview: /assets/postpreview.png
---

![Picture 1](/assets/meleecombatai.png)

- Designed meelee and ranged NPCs to fight the player
- NPCs can be given a patrol path that they will guard
- NPCs will investigate noises they hear or enemies they see
- If an NPCs health gets too low they will flee combat and break line of sight in order to heal

- Meelee NPC with strafe around the player and attack in intervals
- Uses a query around the player to find a good position to attack from

- Ranged NPC will find a suitable position and shoot at the player then reposition
- Uses a query in line of sight to the player, preferrably farther away, and repositions to a nearby point
