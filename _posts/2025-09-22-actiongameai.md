---
layout: post
title:  "Action Game AI"
summary: "AI Engineer"
date:   2025-09-22
preview: /assets/actionpreview.png
---

- Designed meelee and ranged NPCs to fight the player
- NPCs can be given a patrol path that they will guard
- NPCs will investigate noises they hear or enemies they see
- If an NPCs health gets too low they will flee combat and break line of sight in order to heal


Behavior Trees:

![Picture 1](/assets/action_btbase.png)

- Meelee NPC with strafe around the player and attack in intervals

![Picture 2](/assets/action_btmelee.png)

- Ranged NPC will find a suitable position and shoot at the player then reposition

![Picture 3](/assets/action_btranged.png)


Sub-Trees:

- Used to switch between different states in the behavior tree

![Picture 4](/assets/action_stfrozen.png)

![Picture 5](/assets/action_stinvestigating.png)

![Picture 6](/assets/action_stpassive.png)


Tasks & Enviromental Queries:

- Moves the enemy along the patrol route

![Picture 7](/assets/action_bttpatrol.png)

- Uses a query to find positions out of the player's line of sight to hide at

![Picture 8](/assets/action_eqscover.png)

- Uses a query in line of sight to the player, preferrably farther away, and repositions to a nearby point

![Picture 9](/assets/action_eqsrangedlocation.png)

- Uses a query around the player to find a good position to attack from

![Picture 10](/assets/action_eqsstrafe.png)


Enemy Blueprints:

- Creates the basic health bar widget and die/hit react functionality for all enemies

![Picture 11](/assets/action_bpbase.png)

- The melee enemy attacks in a sphere trace in front of itself

![Picture 12](/assets/action_bpmelee.png)

- The ranged enemy attacks in a line trace from itself to the player

![Picture 13](/assets/action_bpranged.png)


AI Controller:

- Initializes all enemies and defaults their state to passive
- Creates the perception for each enemy: sight, sound, & damage

![Picture 14](/assets/action_aic.png)


Blackboard:

- The basic blackboard for all enemies
- Uses the attack target to reference who they are fighting, the player or another npc
- The state keeps what current state the enemy is in
- Point of interest is if the enemy hears the player or sees the player for a moment and wants to investigate
- Attack radius is how much range the enemy has to make an attack
- Defend radius is how much range the enemy wants to keep between itself and the player

![Picture 15](/assets/action_bbbase.png)


Blueprint Interfaces & Damage Struct:

- Interfaces used to define functions for melee and ranged seperately

![Picture 16](/assets/action_bpienemyai.png)

![Picture 17](/assets/action_bpidamage.png)

- Structure used to store different types of damage and modifiers, like blockable or uninterruptable

![Picture 18](/assets/action_sdamage.png)
