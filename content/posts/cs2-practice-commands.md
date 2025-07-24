---
title: Counter Strike 2 Practice commands
date: 2025-04-27
draft: false
tags:
  - cs2
  - english
  - guide
---
# CS 2 Practice Commands

Here's the practice commands, copy and paste to your console.

### Server, teambalance, roundtime and remove bots

```
sv_cheats 1;bot_kick;mp_limitteams 0;mp_autoteambalance 0;mp_roundtime 60;mp_roundtime_defuse 60;mp_freezetime 0;mp_warmup_end;ammo_grenade_limit_total 5;sv_infinite_ammo 1;mp_maxmoney 60000;mp_startmoney 60000;mp_buytime 9999;mp_buy_anywhere 1;mp_restartgame 1
```

### Practice commands and give grenades

```
sv_showimpacts 1;sv_showimpacts_time 10;give weapon_incgrenade;give weapon_flashbang;give weapon_smokegrenade;give weapon_molotov;give weapon_decoy;give weapon_hegrenade;sv_grenade_trajectory_prac_pipreview 1; sv_grenade_trajectory_prac_trailtime 6;
```

### Bind button to re-throw grenades

```
bind p sv_rethrow_last_grenade
```

Then you can use `p` to re-throw grenades.

### Bind button to remove Smoke & Fire particles

```
bind l "ent_fire smokegrenade_projectile kill;ent_fire molotov_projectile kill;ent_fire flashbang_projectile kill;ent_fire hegrenade_projectile kill;ent_fire decoy_projectile kill;stopsound"
```

Then you can use `l` to kill all smokes & mollies.