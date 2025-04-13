---
title: "Ejen Ali Agents' Arena"
date: 2024-07-15T04:37:25+08:00
draft: false

description:

author:
  name: Yong Khang

hero: /images/projects/ejen-ali-agents-arena.jpg
menu:
  sidebar:
    name: "Ejen Ali Agents' Arena"
    identifier: ejen-ali-agents-arena
    weight: 1
    parent: projects
tags:
  - Featured!!
  - Unity
  - Android
  - iOS
---

<table style="margin-left: auto; margin-right: auto;">
  <tr><td>Role</td>					<td>Lead Designer</td>
  <tr><td>Company</td>				<td>Common Extract</td>
  <tr><td>Year Involved</td>		<td>2018 - 2023</td>
  <tr><td>Link</td>		<td><a href="https://play.google.com/store/apps/details?id=com.commonextract.agentsarena">View on Google Play</a></td>
  <tr><td>Link</td>		<td><a href="https://apps.apple.com/my/app/ejen-ali-agents-arena/id1504360885">View on Apple App Store</a></td>
</table>

---

## Game Introduction

Ejen Ali: Agents' Arena is a <abbr title="Similar to Brawl Stars by Supercall">simplified MOBA</abbr> game where players can choose their favourite hero and battle against each other or bots in a 3v3 arena. The main game mode is [Domination](https://gamewith.net/cod-modernwarfare/article/show/12369), where players need to capture POIs that generate scores for the controlling team. Players can also upgrade and select up to 4 gears that provide various passive effects. One of the unique selling points is that the map is in 3D, allowing for more strategic plays.


## The Story

Agents’ Arena is the second title of Ejen Ali that I have worked on. Initially, the idea was to create a co-op game defending waves of enemies, but it later evolved into a simplified MOBA.

We spent considerable time fine-tuning character controls and combat difficulty to ensure a frustration-free experience for younger players, whether they're attacking or defending.

Later, I adjusted the each of the character differently. For instance, the starting character, Ali, is straightforward: charge in against squishy opponents and kite tanky ones, then spam your attacks. Higher-level play involves energy management, timing of Ultimates, and strategic objective clearing.

After the soft launch, I also created and managed the official Discord server, bridging communication between the player base and Media Prima. Without a green light for further updates, it became mentally exhausting to ask players to keep waiting, a situation that persisted for about three years until abandonment.


## My Responsibities

Throughout the development process, I served as the lead designer and owned/administered the [Ejen Ali Official Community](https://discord.gg/4njKpT5) Discord server since the soft launch.


### Game Mode and Map Design

As Lead Designer, my initial responsibility was researching suitable game modes. Drawing inspiration from [Brawl Stars](https://play.google.com/store/apps/details?id=com.supercell.brawlstars) we identified key fun factors like clear objectives, multiple approaches to objectives (defending, stealing, pushing), and comeback mechanics. Ultimately, Domination mode closely matched our objectives:
  - Clear objective: Capture zones to earn points.
  - First team to 100 points wins.
  - Multiple offensive strategies: frontal attacks, stealing undefended zones, holding chokepoints.
  - Multiple defensive strategies: maintaining zone presence to prevent or disrupt captures, knockout / knockback enemies to reset capture progress."

Then, I designed a symmetrical 3D map with multiple paths to objectives. Placing spawn points at higher levels made defending nearer zones easier, reducing the skill floor required to enjoy the game. Additionally, I ensured easy retreat to base and made enemy raids harder through camera angle and map height, providing clear visibility of one's side.


### Characters Abilties

I was also responsible for designing characters' skills and abilities. Below, I'll elaborate on the thought process behind their skill sets.

**Ali**, the starter character, is designed to be an all-rounder who is easy to control:
  - He has medium range attack, he shouldn't be sitting in the back row
  - Slightly longer dash range compared to most characters
  - Attack and dash consume slightly less Energy, making Energy management less of an issue, prolonging action uptime
  - Ultimate is a damaging dash, easy to connect and facilitating follow-up attacks if it doesn't secure a kill

{{< vs 2 >}}

**Alicia**, the subsequent unlockable character, also an all-rounder with a different flavor:
  - Much longer attack range with 3 projectiles in a spread mode
    - Enable her to defend herself at close range with the shotgun effect
  - Higher energy consumption than Ali to limit prolonged engagement
    - Despite that, faster projectile speed enable long range harassment safely
  - Ultimate is an explosive shot with wide range, discourage enemies from grouping up

{{< vs 2 >}}

**Mika** is a tank that can put up a frontal shield that block most projectiles, while sacrificing her movement speed:
  - Shield allows her to push through a choke point effectively, even if it's guarded by numerous range attackers
    - Provided that she doesn't get flanked
  - Ultimate stuns a big area around her after a brief charge, pushing enemies back
    - Which could potentially reset opponent's capture progression
  - Short-range melee attacks hit multiple close enemies
  - Compensates lack of dash with tanking ability and higher base movement speed

{{< vs 2 >}}

**Khai**, characterized by shyness and timidity, uses a rover companion to deal damage. I wanted to emphasize this by making him pretty annoying if being left alone, while he's pretty weak up frontal:
  - Excellent attack range, but good enough projectile speed to be still somewhat accurate at maximum range
  - Piercing attack that inflicts a brief slow debuff on enemies in a line, making him an excellent supporter
  - The only ranged character so far that can bypass Mika's shield
    - Together with the slowing effect, able to effectively shut down Mika's push
  - Togglable speed boost to compensate lack of dash, better matching his personality
  - Ultimate is basically a beefed up basic attack after a brief charge up, which also stuns enemies aside from the pierce effect

{{< vs 2 >}}

**Roza** is a sniper character that boast the longest attack range, and she hits hard:
  - Speedy projectile to hit off-screen enemies accurately
  - Farthest dash range, enabling effective repositioning.
  - The trade-off being costy Energy consumption on both attack and dash, and regenerates Energy only after being out of combat
    - Which makes Energy management extremely important:
	  - Need to pause between reallocating and attacking
	  - Difficult to counterattack if being pursued
  - Ultimate being a deadly laser beam attack that would melt most ranged character after a charge-up
    - However, the firing direction would get locked during the charging phase, easier for prepared opponent to dodge

{{< vs 2 >}}

**Rudy** is another melee character that specialize at infiltration:
  - Similar to Mika, basic attack is a series of unimpressive CQC
  - Skill that makes him semi-invisible, and causing auto-attacks not to lock into him
    - Which makes him excellent in stealing undefended objective with less chance of being spotted
	- Forcing enemy to opt for a manual aim
  - Ultimates throws 2 shackles to stun enemies in arc from both side
    - Require mastery to use at greater range, while still accurate at closer range
	- Trivial to launch follow-up attacks afterward


### Organize Game Test

Throughout the development I also organized numerous of game test session internally, with the client, as well as with alpha testers. We collected the feedback and made adjustment accordingly. One example is that, due to the 3D map, projectiles could not hit the target appropriately if they stand at a certain distance from cliff. I would then propose the idea of using 2 colliders: a smaller one to check for terrain and obstacles, and a larger one to check for eligible entities. The resulting effect is that projectiles would now be able to graze through obstacles and hit the nearby player. This reduces frustration while not disregards the hitbox for obstacles.


### Balancing Combat

I was also responsible in balancing the combat thoughout various game test and changes. I went with the route of buffing all characters until they're equally strong; rather than nerfing them until they're equally bland. This mindset had made sure each character shines in their role.


### Managing the Discord

In addition to that, I was responsible for creating and managing the Discord server. I configured several bots for ease of management, spam detection, language moderation, as well as utilities like a radio bot. I organized contests that offering unique titles and channel access, maintained regular player communication, compile their feedback to the client.

