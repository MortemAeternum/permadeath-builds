# Mortem Aeternum: Permadeath builds

This repository contains a collection of permadeath-ready and permadeath-viable
[Dungeons &amp; Dragons Online](https://www.ddo.com/) character builds. The
format that these builds are in is the format used by [EllisDee37&rsquo;s
&ldquo;Character Builder Lite&rdquo;](https://www.ddo.com/forums/showthread.php/455712-Character-Builder-Lite).

Character Builder Lite is a [Windows
NT](https://en.wikipedia.org/wiki/Windows_NT) program (written in [classic
Visual Basic 6.0](https://en.wikipedia.org/wiki/Visual_Basic)), but can be
easily run under macOS and various Linux distributions (indeed, any OS that is
supported by [Wine](https://www.winehq.org/)) by running the program using
Wine. However, this may or may not require a number of
[`winetricks`](https://github.com/Winetricks/winetricks) invocations, as
follows (try it first without using `winetricks`, and if that doesn&rsquo;t
work, then try the first invocation and test it, &amp;c.):

```bash
winetricks -q vb6run

winetricks -q native_oleaut32

winetricks -q allfonts
```

## Filename format

The names of the build files in this repository follow a certain systematic
naming scheme, for ease of reading and use. The scheme consists of the
following elements, in the following order, each element being separated by the
string `_-_`. Then the name is suffixed with the string `.build`. Note that
there is no `_-_` between the last element and `.build`:

* The class split (at level 20) of the build, each class being formatted as
  the 3-letter abbreviation of the class followed by the number of levels in
  that class, and the classes being separated by underscores. The classes
  should be ordered from greatest to least in terms of number of levels. E.g. a
  build that ultimately takes 15 levels of Artificer, 4 levels of Fighter, and
  1 level of Wizard would format this section as `art15_ftr4_wiz1`. The
  3-letter class name abbreviations are as follows:
    + `art` : Artificer
    + `bbn` : Barbarian
    + `brd` : Bard
    + `clr` : Cleric
    + `drd` : Druid
    + `fvs` : Favored soul
    + `ftr` : Fighter
    + `mnk` : Monk
    + `pal` : Paladin
    + `rgr` : Ranger
    + `rog` : Rogue
    + `src` : Sorcerer
    + `wlk` : Warlock
    + `wiz` : Wizard
* The 3-letter abbreviation of the race of the build. E.g. a Warforged build
  would format this element as `wfd`. The 3-letter race name abbreviations are
  as follows:
    + `aas` : Aasimar
    + `asc` : Aasimar Scourge
    + `bfd` : Bladeforged
    + `dgo` : Deep Gnome
    + `dbn` : Dragonborn
    + `drw` : Drow Elf
    + `dwf` : Dwarf
    + `elf` : Elf [Khorvaire]
    + `gno` : Gnome
    + `hef` : Half-Elf
    + `hoc` : Half-Orc
    + `hlg` : Halfling
    + `hum` : Human
    + `mor` : Morninglord [Sun Elf]
    + `pdk` : Purple Dragon Knight
    + `shk` : Shadar-kai
    + `tie` : Tiefling
    + `tsc` : Tiefling Scoundrel
    + `wfd` : Warforged
    + `wef` : Wood Elf
* The string `trapper`. This element is *optional*, and should only be present
  if the build can be expected to competently find and disable traps.
* The abbreviated name of the enhancement tree that the build takes tier 5 of
  (if any), possibly followed by either one or two other enhancement trees that
  are similarly central to the build. These abbreviated enhancement tree names
  are to be separated by underscores, and the abbreviations are taken from the
  [DDO Wiki](https://ddowiki.com/). E.g. a build that takes tier 5 enhancements
  from Renegade Mastermaker, but also makes heavy use of the Stalwart Defender
  tree, would format this element as `RM_StD`. The DDO Wiki&rsquo;s enhancement
  tree abbreviations are as follows:
    + `race` : Use this to mean &ldquo;racial enhancement tree&rdquo;
    + `AT` : Arcanotechnician
    + `BE` : Battle Engineer
    + `RM` : Renegade Mastermaker
    + `FB` : Frenzied Berserker
    + `OS` : Occult Slayer
    + `Rav` : Ravager
    + `SB` : Swashbuckler
    + `SS` : Spellsinger
    + `WC` : Warchanter
    + `DD` : Divine Disciple
    + `RS` : Radiant Servant
    + `War` : Warpriest **or** War Soul
    + `NW` : Nature&rsquo;s Warrior
    + `NP` : Nature&rsquo;s Protector
    + `SH` : Season&rsquo;s Herald
    + `AoV` : Angel of Vengeance
    + `BoH` : Beacon of Hope
    + `Ken` : Kensei
    + `StD` : Stalwart Defender
    + `Van` : Vanguard [Fighter] **or** Vanguard [Paladin]
    + `HeM` : Henshin Mystic
    + `NiS` : Ninja Spy
    + `Shi` : Shintao
    + `KotC` : Knight of the Chalice
    + `SaD` : Sacred Defender
    + `AA` : Arcane Archer [includes racial Arcane Archer trees]
    + `DWS` : Deepwood Stalker
    + `Tem` : Tempest
    + `Ass` : Assassin
    + `Mec` : Mechanic
    + `TA` : Thief-Acrobat
    + `Air` : Air Savant
    + `Earth` : Earth savant
    + `EK` : Eldritch Knight [Sorcerer] **or** Eldritch Knight [Wizard]
    + `Fire` : Fire Savant
    + `Water` : Water Savant
    + `ES` : Enlightened Spirit
    + `SE` : Soul Eater
    + `TS` : Tainted Scholar
    + `AM` : Archmage
    + `PM` : Pale Master
    + `Fal` : Falconry
    + `Har` : Harper Agent
    + `Inq` : Inquisitive
    + `Vis` : Vistani Knife Fighter
* The main-hand weapon, off-hand weapon (includes shields/orbs/rune arms), and
  armor types intended to be used by the build. The types should be separated
  by underscores. The weapon types are as follows:
    + `none` : Nothing
    + `BAx` : Battle axe
    + `bow` : Long bow or short bow
    + `BSwd` : Bastard sword
    + `Buck` : Buckler
    + `Club` : Club
    + `Dag` : Dagger
    + `Dart` : Dart
    + `DAx` : Dwarven war axe
    + `exbow` : Any exotic crossbow
    + `Falch` : Falchion
    + `GAx` : Great axe
    + `GClub` : Great club
    + `GSwd` : Great sword
    + `Gxbow` : Great crossbow
    + `HAx` : Handaxe
    + `HMace` : Heavy mace
    + `HPick` : Heavy pick
    + `Hwrap` : Handwraps
    + `Kho` : Khopesh
    + `KT` : Any Knight&rsquo;s Training weapon
    + `Kukri` : Kukri
    + `LBow` : Long bow
    + `LHam` : Light hammer
    + `light` : Any light weapon
    + `LMace` : Light mace
    + `LPick` : Light pick
    + `LShld` : Large shield
    + `LSwd` : Long sword
    + `Maul` : Maul
    + `Mstar` : Morningstar
    + `mthrw` : Any simple or martial thrown weapon
    + `Orb` : Orb
    + `pick` : Heavy pick or light pick
    + `Qstaff` : Quarterstaff
    + `Rap` : Rapier
    + `Rune` : Rune arm
    + `rxbow` : Heavy repeating crossbow or light repeating crossbow
    + `SBow` : Short bow
    + `Scimi` : Scimitar
    + `sceptr` : Exact weapon type doesn&rsquo;t matter because the build casts
                 spells instead
    + `Shkn` : Shuriken
    + `Sick` : Sickle
    + `SShld` : Small shield
    + `SSwd` : Short sword
    + `sthrw` : Any simple thrown weapon
    + `swash` : Any swashbuckling weapon
    + `TAx` : Throwing axe
    + `TDag` : Throwing dagger
    + `THam` : Throwing hammer
    + `THF` : Any two-handed weapon
    + `THFb` : Any two-handed bludgeoning weapon
    + `THFs` : Any two-handed slashing weapon
    + `thrw` : Any thrown weapon
    + `TShld` : Tower shield
    + `WHam` : War hammer
    + `xbow` : Heavy crossbow or light crossbow

    The armor types are as follows:

    + `BPlat` : Breastplate
    + `Chain` : Chainmail
    + `Cloth` : No armor (usually robes, or any Warforged lacking both the
                Mithral Body and Adamantine Body feats)
    + `FPlat` : Full plate
    + `HPlat` : Half plate
    + `heavy` : Any heavy armor, or Adamantine Body if Warforged
    + `Hide` : Hide
    + `Leath` : Leather
    + `light` : Any light armor, or Mithral Body if Warforged
    + `lm` : Any light or medium armor
    + `lmh` : Any light, medium, or heavy armor
    + `Med` : Any medium armor
    + `mh` : Any medium or heavy armor
    + `Scale` : Scalemail

    E.g. a typical pure Barbarian two-handed build would format this element as
    `THFs_none_lm`.
* The (unique and nonempty) name of the build, which can only contain the
  following characters:
    + Uppercase and lowercase letters
    + Digits
    + Underscores
    + Dots/periods/full-stops

    That is, the name must match the following regular expression:
    `^[A-Za-z0-9_\.]+$`

## Legal

The contents of this repository are licensed to you (or anyone else) under the
terms of the [GNU Affero General Public License, version
3](https://www.gnu.org/licenses/agpl-3.0.en.html) (or higher, at your option).

![GNU AGPL v3](https://www.gnu.org/graphics/agplv3-with-text-162x68.png "GNU AGPL v3")
