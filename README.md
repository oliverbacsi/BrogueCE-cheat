Brogue CE
=========

# Oliver's Cheat Hacks

> This is the Cheat Hacked version of the original Brogue CE game !!!

For those lamers and n00bs for whom even the Wizard Mode is not good enough, or are fed up with starving or still getting affected by poisions or bolts or still dying of whatever, or simply don't need the full Wizard package just one thing of minor help for practicing purposes, here comes the cheated version of Brogue CE.
You can invoke the game with any of the following command-line arguments to get one thing or more things cheated at the same time:

* **`--cheatHealth`**
	* Your Health Points never decrease. Nothing can affect or poison You.
	* You win all Your battles instantly with one hit, while Your enemies always lose.
* **`--cheatNutrition`**
	* Your Nutrition will never decrease. No more dying on hunger.
* **`--cheatMagicMap`**
	* All levels get instantly Magic Mapped upon entering.
	* No more hidden rooms or features.
* **`--cheatIdentify`**
	* All picked up items will be instantly identified in Your backpack when viewing inventory.
	* This includes the "Detect Magic" feature as well, so items will show up with their blue/red icon.
* **`--cheatConfusion`**
	* Never get influenced by Confusion or any negative effects again.
	* This includes: Confusion, Hallucination, Paralysis, Poison, Nausea, Entrancement, Discord, Darkness, etc, all this crap.
	* Not depending if it comes from drinking a potion, gas trap, or magical hit from an enemy. You can literally drink anything.
* **`--cheatStuck`**
	* Don't get stuck in webs, be always free to move.
	* Applies for net traps as well as for spider monster's web.
* **`--cheatLight`**
	* No darkening and no shrinking of visibility radius on deper levels.
* **`--cheatKeys`**
	* Pass all doors without the matching key.
	* Theoretically this is useless as finding a key to a door on a certain level is easy but sometimes there is a reward room opening from an other reward room and the key for it is among the other rewards, so if You pick the key and open the second door and find out that You could have used a reward from the previous room better then there is no way back any more. This way You can preliminarily check the contents of a reward room.
	* Unforeseen consequence : As in the reward rooms the artifacts belonging to their original place are also treated as "matching keys" by the program, but this cheat eliminates the need for matching keys, so as a result: If You pick up an artifact from a reward room, You can drop any valueless sh*t onto its place, the program will handle it as matching key, so all the other cages remain open in the reward room, so You can collect all artifacts eventually...
* **`--cheatDisturb`**
	* Don't get disturbed by a distant monster during running. (still to clarify for myself which events should disturb a running player)
	* It is quite annoying that running gets stopped basically on everything. Certainly if You are playing fair without cheats, this is necessary. But if You ar invincible then it is quite annoying that Your running is interrupted just because there is a rat moving in the other corner of the level.
* **`--cheatWeakEels`**
	* Eels are surprisingly powerful (HP 18, defense 27, accuracy 100, damage 3-7-2), knowing that they can appear at relatively low levels when the player is not yet developped and experienced too much.
	* This cheat will make eels the same strong as rats (HP 6, defense 0, accuracy 80, damage 1-3-1)
* **`--cheatALL`**
	* Switch on **all** above cheats. To keep You from typing too much.


# FURTHER CHEATS :

* **`variants/GlobalsBrogue.c`**
	* itemGenerationProbabilities (vector) : change item type probabilities when generating
	* Vault room probabilities , contents, levels, etc
	* extraItemsPerLevel = 0 : how many additional items to give per level
* **`Items.c`**
	* `item *makeItemInto()`
		* rand_percent(40) : probability if item is non zero (either enchanted or coursed)
		* rand_percent(50) : enchanted or coursed
		* rand_percent(33) : good or bad runic
		* Item->flags : ITEM_CURSED or ITEM_Blessed???????
	* `void populateItems()`
		* numberOfItems=3 : how many items on the level


Have fun playing!
And don't forget: if You are trained enough using the cheats, then try the game with no cheats as well!

---

# Original description of this repository:

> *Countless adventurers before you have descended this torch-lit staircase,
> seeking the promised riches below. As you reach the bottom and step into
> the wide cavern, the doors behind you seal with a powerful magic...*
>
> ***Welcome to the Dungeons of Doom!***

*Brogue* is a single-player strategy game set in the halls of a mysterious
and randomly-generated dungeon. The objective is simple enough -- retrieve the
fabled Amulet of Yendor from the 26th level -- but the dungeon is riddled with
danger. Horrifying creatures and devious, trap-ridden terrain await. Yet it is
also riddled with weapons, potions, and artifacts of forgotten power. Survival
demands strength and cunning in equal measure as you descend, making the most
of what the dungeon gives you. You will make sacrifices, narrow escapes,
and maybe even some friends along the way -- but will you be one of the
lucky few to return alive?

- [Downloads][releases]
- [Wiki](https://brogue.fandom.com/wiki/Brogue_Wiki)
- [Forum (Reddit)](https://www.reddit.com/r/brogueforum/)
- [Roguelikes Discord](https://discord.gg/9pmFGKx) (we have a #brogue channel)
- IRC: [##brogue on Libera Chat](https://kiwiirc.com/nextclient/irc.libera.chat/##brogue)
- [Original website](https://sites.google.com/site/broguegame/)
- [Android port](https://github.com/bilgincoskun/brogue-android-port/releases)


Playing
-------

If you downloaded a [release][releases], you can open the game as follows:

### Windows

Run `brogue.exe`.

### Mac

Run the included app.

As it's an unsigned program, you may have to convince macOS to let you run it.
You can do this by right-clicking the app and choosing *Open* the first time you
run it.

### Linux

Run the `./brogue` script in the same the folder as this file.

Make sure you have SDL2 and SDL2_image installed via your package manager. The
required packages are:

- Debian/Ubuntu: `libsdl2-2.0-0 libsdl2-image-2.0-0`
- Fedora: `SDL2 SDL2_image`
- Arch: `sdl2 sdl2_image`

You can also run `./make-link-for-desktop.sh` to generate a .desktop file to
place on your desktop or applications folder.

### More information

Graphical tiles are included; press 'G' to toggle them.

For some tips on playing the game, see the original website, linked above. Also
check out the wiki -- although keep in mind CE may differ from it.

If you downloaded the source code, you will need to build the game first. For
instructions, see `BUILD.md`.

Brogue supports some command-line options; run `brogue --help` for more info.
(On Windows, if you want to see output in the command prompt, use
`brogue-cmd.bat`.)


Contributing
------------

Please see our [contribution guide][contrib] for all the ways you can help make
Brogue better!

[contrib]: https://github.com/tmewett/BrogueCE/wiki/Contribution-guide


About
-----

### What is Community Edition?

Brogue was created by Brian Walker. This version, *Brogue: Community Edition*,
is a continuation of its development. It has several main goals:

- fix bugs and crashes
- add useful quality of life and non-gameplay features
- improve the gameplay and keep it exciting
- ease development and maintenance
- be a convenient base for forks and ports to new platforms

### How is CE different from the original Brogue?

Please refer to the changelog or release history for a complete list. There is
also a wiki page: [Changes from original][cfo].

[cfo]: https://github.com/tmewett/BrogueCE/wiki/Changes-from-original

### How is the project run, and how are changes decided?

The project is run with a "benevolent dictator" model, with myself (tmewett) in
charge. There are many other testers and regular contributors; see the
contribution guide to get involved!

We always try to make changes in the same spirit as the rest of the game. Anyone
can propose a change - all discussion occurs in our GitHub issue tracker or on
our development Discord (see contributing guide). We also make sure that things are
well play-tested.


[releases]: https://github.com/tmewett/BrogueCE/releases
