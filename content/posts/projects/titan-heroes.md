---
title: "Titan Heroes"
date: 2024-07-10T02:34:19+08:00
draft: false

description:

author:
  name: Yong Khang

hero: /images/projects/titan-heroes.jpg
menu:
  sidebar:
    name: "Titan Heroes"
    identifier: titan-heroes
    weight: 5
    parent: projects
tags:
  - Featured!!
  - Roblox
---

<table style="margin-left: auto; margin-right: auto;">
  <tr><td>Role</td>					<td>Lead Designer</td>
  <tr><td>Company</td>				<td>Common Extract</td>
  <tr><td>Year Involved</td>		<td>2023 - 2024</td>
  <tr><td>Link</td>		<td><a href="https://roblox.com/games/15160302599">View on Roblox</a></td>
</table>

---

## Game Introduction

Titan Heroes is a MMORPG-like TPV Shooter game on the Roblox platform. It features a PvE progression system with optional PvP in both overworld and specialized PvP Arena. Players can craft various guns using the materials dropped from monsters and upgrading them. Additionally, there are also a variety of minibosses and bosses for the players to challenge themselves against.

## The Story

The development started in mid 2023. This would be the largest Roblox project we've ever undertaken. Under the stakeholders's direction, we managed to come up with GDD that closely matches their vision. Due to the time constraint for the first vertical slice, we had to cut some of the larger features. After careful consideration, we managed to make adjustments to several relevant mechanics to ensure everything would still integrates seamlessly.

## My Responsibities

Below are my responsibilities throughout the development cycle of Titan Heroes.

### Map Expansion

In addition to collaborating on the GDD with another designer, I was responsible for expanding the first map (originally designed by an artist) to accommodate more monsters without feeling cramped. Under my guidance, an artist and I managed to expand the map with additional POIs here and there, and made sure the non-combat POIs provided scenic view with leading lines highlighting the next goal / POI.

### Excel Hell 1 - Combat Stats, Progression Simulaton, Resource Faucets & Sinks

The first excel hell started with combat balancing. I assigned levels to various zones and the monsters spawning within the zones would be of specific level. Then, the monsters would have stats designed based on player's stat of that level. The scaling algorithm for both players and monsters work differently to build up a nice difficulty curve.

I was also in charge of simulating the progression system via Google Sheet and balance various aspect of the games with it, such as:
  - Player's and Monsters' Stats Growth
  - Player's EXP requirement and drop rate
    - Along with Quest's EXP and rewards
  - Crafting requirement and drop rate
  - Projected player's level VS playing time

The spreadsheet that simulates the progression system took these parameters into account:
  - Time to Kill (TTK)
  - Quest EXP and Quest EXP overflow
  - Time needed for quests
  - EXP per hunt (selectable with or without EXP Boost

Then, I adjusted the EXP requirement with it. It also gave me kills needed per level, which I would be able to work out the EXP and loot drop rate, and project player economy with it. With that data, I could work out the costs of various items and upgrades.


### The Guns and the Skills

Additionally, I was tasked with setting the general feel of each weapon by adjusting their stats. such as:
  - Some weapon would feel more impactful at closer range, slow but steadily hits hard, reliable reload time, but quick damage falloff over distance
  - PDW-like guns that compensate for slightly lower damage with a smooth barrage at a more desirable distance and good accuracy
  - Or my favorite: a 5-shots burst grenade launcher that scatters widely and affected by gravity, which works well as a mob clearer at medium-close distance or doubling as an OP face-range shotty.

The guns were balanced at a base level. Then, they would be scaled up based on the a power scaling formula, so that they would feel challenging at every stage of progression.

Similarly, this was also done on the Skills balancing.


### Overboard with the Retention System

Furthermore, I designed the <abbr title='as well as acquisition, engagement and conversion. Thereinafter "retention"'>retention</abbr> system and in-app purchases (IAPs). On the Roblox platform, mechanisms for acquisition / engagement / retention / conversion need to be significantly more heavy handed compared to PC or even mobile games. For example, aside from Daily Login Rewards, most Roblox games would also have Session Rewards, where players receive free items at intervals ranging from 3 minutes to 30 minutes, generally over a 2-hours period. This is because the Roblox SEO algorithm favors a longer session time (and multiple sessions per day).

Below were some of the retention mechanisms that I've designed:
  - Game <abbr title='Think it as "Download Goal", but with "Likes" instead'>Likes Goal</abbr>
  - Friend Invite Rewards
    - <abbr title="Invite friends who are also a Roblox Premium subscriber">Premium</abbr> Friends Invite Rewards
  - Friend <abbr title="EXP Boost with diminishing return">Online</abbr> Bonus
  - Daily Rewards
  - <abbr title="Similar to Daily, but at an increasing time interval counted in minutes, for 2 hours. Reset if log out. Extremely common on Roblox">Session</abbr> Rewards
  - Daily <abbr title="Like how you get your Shopee Coins">Spin the Wheel</abbr>
    - Premium players get extra Spins
  - <abbr title="duh">Daily Quest</abbr>
  - Daily 30 minutes EXP Boost


### Excel Hell 2 - Monetization

As for the IAP, I've designed a Google Sheet table that allows one to input item base price, calculate the value and display it as either "xx% more value" or "xx% discount" (selectable), label as <abbr title="I call this FOMO-ness">once per day/week/month or no limit or xx hours limit</abbr>. Multiple items can also be grouped into IAP Packages and it will automatically calculate the value of the package based on the contents.



