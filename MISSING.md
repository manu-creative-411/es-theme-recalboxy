# Platforms without artwork

> Platforms with a folder in `platforms/` now have at least a logo (`images/logo.*`), taken from
> the Carbon theme, and many also a console picture and a controller. The systems below are Batocera
> systems (`es_systems.yml`) that have **no folder at all**, because neither the original Slate nor
> Carbon has artwork for them: they use the default band colors and the system name as text.
> If you add `images/logo.svg` (and optionally `consolegame.svg`, `controller.svg`, `colors.xml`,
> `systeminfo.xml`) to a folder with that name inside `platforms/`, it will be used.

- `beena` (Advanced Pico Beena)
- `catacomb` (CatacombGL)
- `ctvboy` (Compact Vision TV Boy)
- `doom3` (Doom 3)
- `gametank` (GameTank)
- `halflife` (Half-Life 1)
- `jazz2` (Jazz Jackrabbit 2)
- `jkdf2` (Jedi Knight - Dark Forces 2)
- `jknight` (Star Wars - Jedi Academy)
- `mc10` (MC-10)
- `mohaa` (Medal Of Honor - Allied Assault)
- `mz2000` (Sharp MZ-2000)
- `mz2500` (Sharp MZ-2500)
- `mz700` (Sharp MZ-700)
- `mz800` (Sharp MZ-800)
- `mz80k` (Sharp MZ-80K)
- `pc80` (PC-8001)
- `pcw` (Amstrad PCW)
- `pv2000` (PV-2000)
- `quake2` (Quake II)
- `rott` (Rise of the Triad)
- `rtcw` (Return To Castle Wolfenstein)
- `rx78` (RX-78)
- `screenshots` (Screenshots)
- `segaai` (Sega AI Computer)
- `sv8000` (Super Vision 8000)
- `systemsp` (Sega System SP)
- `traider` (Tomb Raider I, II & III)
- `tvc` (Videoton TVC)
- `uqm` (Ur-Quan Masters)
- `uzdoom` (UZDoom)

# Platforms with partial artwork

Platforms added or completed from Carbon (see `CREDITS.md`) only got what Carbon has: a logo
(`logo.svg`, `logo-w.svg`, or a raster `logo.webp` where Carbon has no vector one), a console picture
(raster, `consolegame.webp`/`.png`) and a controller (`controller.svg`: white line-art, tinted with the
palette's text color through `systemControllerTint`). Carbon has no technical data or band colors, so
those were written for Recalboxy afterwards: every platform folder now has its own `colors.xml` bands
and `systeminfo.xml` (see `CREDITS.md`).

`bk` and `dragon64` got console/controller images, band colors and system info from the Recalbox
theme (recalbox-next v9), but still have no `images/logo.svg`: the system name is shown as text.

# Original Slate folders kept without an equivalent system

They may be useful for automatic arcade collections, user-added systems or
future Batocera versions: `ags`, `android`, `androidapps`, `androidgames`, `arcade`, `auto-allgames`, `auto-favorites`, `auto-lastplayed`, `chailove`, `cps`, `cps1`, `cps2`, `cps3`, `custom-collections`, `doom`, `dos`, `fpinball`, `kodi`, `naomigd`, `stv`, `switch`, `type-x`, `zxnext`.

# Platforms still without a logo (system name as text)

`bk`, `dragon64`.

# Carbon files that were not added

* `consoles/aquarius.jpg`: a full 1280x720 photo with background, not a cut-out console.
* Heavy files (over 1 MB; slow to rasterize on small devices): `consoles/linux.png`,
  `consoles/pocketstation.png`, `consoles/projectarcade.png`, `consoles/segastv.png` and
  `logos/br/sega32x.svg` / `sega32x-w.svg` (1.5 MB each; a traced bitmap).
* `controllers/jp/nes.svg`: white line-art pad that would clash with the full-color base NES pad.
* Series and manufacturer collections (`mario`, `zelda`, `capcom`, `konami`...), the `custom-collections-*`
  logos and the translated logos (`<name>-es.svg`, `-fr`...): they are for custom collections / per-language
  logos, not for systems.
