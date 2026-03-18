# quake3-holyshit-mod

The announcer will exclaim "Holy shit!"
when someone _almost_ wins (or almost doesn't).

As you might know, in the original Quake III Arena (and Team Arena)
if one gets killed while being very close to scoring the flag
or the cubes, the announcer will exclaim "Holy Shit!".
Those are the only two cases (see
[the source code](https://github.com/id-Software/Quake-III-Arena/blob/dbe4ddb10315479fc00086f08e25d968b4b43c49/code/game/g_combat.c#L455-L458)
).

We think it's a bit of a wasted potential.
And this mod aims to fix that!

Still, we recognize the holiness of this shit
(how special the voice line is),
so we take care to only play it
when something of equal or greater level happens
(compared to almost bringing the flag),
keeping the original spirit.

This mod also introduces the `g_canDamageAfterMatchEnd` variable
which allows damaging and fragging during that one second
between the match end and the intermission.
This is necessary for the mod to work in Free For All.
Frags made during that period will not affect the scores,
so don't worry, this doesn't really change gameplay.

## Integrating into other mods

Apply the patches with `git am`.

See another mod that takes this approach:
<https://github.com/WofWca/quake3-better-gibs-mod>.

## License

These patches are dual-licensed under either
the ["QIIIA Game Source License"](./QIIIA%20Game%20Source%20License.txt),
or the ["GPL-2.0"](./COPYING.txt),
at your option.
That is, you may apply these pathes to any other project
based on Quake III Arena source code, be it the GPL or pre-GPL release.

Some more about Quake III licensing here:

- <https://github.com/ioquake/ioq3?tab=readme-ov-file#standalone-game-licensing>
- <https://github.com/ec-/baseq3a/pull/59>
