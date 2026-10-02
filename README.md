# Recalboxy (es-theme-recalboxy)

A tribute to Recalbox and to older Batocera versions. Recalboxy is a Batocera
EmulationStation theme derived from the ES-DE **Slate** theme (itself based on
*recalbox-multi*), in theme format 7 (tested with `batocera-emulationstation`
compiled for [retrobox](https://github.com/manu-romero-411/retrobox-core)).

## Installation

Copy the `es-theme-recalboxy` folder to `/userdata/themes/` (over SSH or through
the shared `themes` folder). Then, in EmulationStation:
*User Interface Settings → Theme* and pick `es-theme-recalboxy`, and tweak the
options under *Theme Configuration*.

## Configurable options

| Option (subset) | Values | ES-DE equivalent |
|---|---|---|
| Color set (`colorset`) | Slate (default) / Standard / Darker / Black and white / White and black / Blue / Green / Grey / Orange / Pink / Purple / GameCube / Red / Yellow | Recalbox palettes (`colors/*.xml`; `GameCube` is our own: white text on indigo `#243075`), replacing Dark/Light |
| Font size (`fontsize`) | Medium (default) / Large | `fontSize` medium / large |
| System info (`systeminfo`) | Show (default) / Hide | (new) the 10 lines of technical data for each platform |
| Help icons (`helpicons`) | Default (Batocera) / Xbox / PlayStation / SNES / Generic 4, 6 and 8 buttons / SNES alt / Xbox One / Arcade | (new) icons for the bottom help bar; assets in `help/icons/` |
| System list (`systemview`) | Horizontal (default) / Vertical (left) | Recalbox's *vertical left* system view (`views/system-vertical.xml`); landscape 16:9 and 4:3 screens only |
| Rating icons (`ratingicons`) | Per platform (default) / Standard | each console's own icons instead of stars (`platforms/<platform>/rating.xml` + `images/rating_*.svg`) |

The Xbox, PlayStation and SNES sets map the physical position of Batocera's
gamepad buttons (A = east, B = south, X = north, Y = west): e.g. on
PlayStation, A→○, B→✕, X→△, Y→□. They are full-color icons and are not tinted
with the theme's help color; the generic sets are.

### Menu

The **menu** (Start button) uses the Recalbox style: Bariol Regular font
(italic for the footer) and the icons in `core/images/menu_icons/`. Colors come
from each palette (`menu*Color` variables in `colors/*.xml`):

* **Dark palettes** (light text: Darker, Grey, White and black, GameCube): the
  menu panel is a darker shade of the palette's `backgroundColor`, the text is
  an almost-white tint of the same color, the selected row is a lighter shade
  of the background (with white text) and the veil behind the menu
  (`core/images/fade/<palette>.png`) is dark.
* **Standard** (`default`) is an exception: it uses the classic
  EmulationStation menu look (white panel, gray `777777` text and arrows,
  gray `878787` selected row with white text) and a soft dark veil (black at
  25 %: noticeable, but the content behind stays visible). The clock,
  indicators and help bar keep their usual dark gray. It still uses Bariol.
* **Light palettes** (dark text) keep the usual light menu (background
  `F1F1F1`, text `35495E`) and its light veil.
* **Slate** (`colors/slate.xml`, the default palette; formerly "Light blue (Recalbox)" and named after the original theme) has light
  text but keeps the usual light menu, with its original dark blue veil.

Menu **section headers** (`menuGroup`) use Bariol Bold, an accent color
(`menuSectionColor`) and a background of a different shade than the panel
(`menuSectionBackgroundColor`): darker on dark menus, slightly darker and
bluer on light ones.

On every palette the clock, indicators and help bar take their color from the
`overlayColor` variable (the same as the usual help color, except on Standard).

### System list selector

The vertical system list selector (`systemSelectorColor`) is a lighter shade of
the `backgroundColor` on dark palettes and a darker shade on light palettes.

The palettes come from Recalbox; the carousel, game counter, rating and dimmed
values do not exist in Recalbox and are derived (see the header of each
`colors/*.xml`). `standard_noinfo` is not included: it equals *Standard* +
*System info: Hide*.

### Layout and language

The **layout** is chosen automatically from the screen ratio detected by
Batocera (`screen.ratio`): 16:9 (includes 16:10, 21:9, 3:2, 32:9…), 4:3
(includes 5:4, 6:5, 1:1…), and the vertical 16:9 and 4:3 versions for rotated
screens. These are the same four layouts the original Slate had.

The **language** of on-screen labels (Released, Developer…) follows Batocera's
language; all 21 languages of the original Slate are kept.

The **release date** is shown as the year only, in full (`%Y`, e.g. `1997`).
Many scraped games only carry a year, which would otherwise be displayed as
01/01 of that year.

### Original Slate variants -> Batocera gamelist styles

| Original Slate (ES-DE) | Batocera (User Interface Settings → Gamelist style) |
|---|---|
| `withVideos` | **Video** |
| `withoutVideos` | **Detailed** |
| `noGameMedia` | **Basic** |
| (did not exist) | **Grid** (simple version with the same frames and colors) |

In *Automatic* mode Batocera picks between them depending on the media each
system has.

## Platform names

All platform folders live under `platforms/` (one folder per system, plus the
collection folders `auto-*` and `custom-collections`); the rest of the theme
stays at the root (`core/`, `colors/`, `help/`, `lang/`, `layouts/`, `views/`).
Platform folders are named after the `<theme>` value in Batocera's
`es_systems.yml` (or, if missing, the system name), and also after the groups
(`snes`, `megadrive`, `ports`, `amiga`, `c64`, `windows`, `jaguar`, `atari8bit`,
`lcdgames`, `nes`). Batocera uses `${system.theme}` to locate, inside `platforms/`, each platform's
`images/logo.svg`, `images/consolegame.svg`, `images/controller.svg`,
`colors.xml` and `systeminfo.xml`.

Original Slate folders that were renamed/reused for Batocera's names:

| Batocera folder | Artwork taken from original Slate |
|---|---|
| `3ds` | `n3ds` |
| `amiga500` | `amiga600` |
| `amigacdtv` | `cdtv` |
| `atari8bit` | `atari800` |
| `c20` | `vic20` |
| `cdi` | `cdimono1` |
| `cplus4` | `plus4` |
| `creativision` | `crvision` |
| `gb2players` | `gb` |
| `gbc2players` | `gbc` |
| `jaguar` | `atarijaguar` |
| `megadrive-msu` | `megadrive` |
| `msx2+` | `msx2` |
| `pce-cd` | `pcenginecd` |
| `sgb-msu1` | `sgb` |
| `snes-msu1` | `snes` |
| `thomson` | `to8` |
| `trs80` | `trs-80` |
| `videopacplus` | `videopac` |
| `xegs` | `atarixe` |

The remaining 130 matches are direct. Batocera platforms with no original Slate artwork
are listed in `MISSING.md`: they use the default band colors and the system
name as the logo.

## Technical changes from the original Slate

* `theme.xml` in Batocera format (`formatVersion` 7) with `subset`, `lang`,
  `if` and `verticalScreen`; ES-DE's `capabilities.xml`, `aspectRatio`,
  `variant`, `colorScheme` and `fontSize` are gone.
* Renamed elements: `gamelistTextlist` -> `gamelist`, `systemCarousel` ->
  `systemcarousel` (`logoSize`, `maxLogoCount`, `logoScale`),
  `gameCounter` -> `systemInfo`, `developer`/`genre`/... -> `md_*`, labels
  -> `md_lbl_*`, `gameImage` -> `md_image`, `gameVideo` -> `md_video`,
  `letterCase` -> `forceUppercase`, `horizontalAlignment` -> `alignment`.
* Each platform's band colors change from `<image name="bandN">` to
  `band1..band4` variables; the `info1..info10` lines become
  `extra="true"` elements.
* Sounds become `sound` elements (`launch`, `back`, `menuOpen`) and
  `scrollSound` in the list, carousel and grid.
* Clock, controllers and battery are themed in the `screen` view; Batocera's
  menus follow the chosen color set.
* ES-DE's badges (favorite, kid game, manual, save state, achievements,
  netplay, gun, wheel and hidden) are **not drawn** in the right-hand panel:
  Batocera already shows their icons next to the title in the game list, so
  they were redundant. The SVGs are still in `core/images/badges/` in case you
  want them back: re-add the `md_favorite`, `md_manual`, etc. elements (an
  image with `path` and `color`) to `layouts/*.xml`.
* The header's game counter uses a *binding* (`{system:total}`) and the source
  system name in collections uses `{game:system:fullName}`.

## Differences with no Batocera equivalent

Theme transitions (in Batocera they are chosen in ES settings), video pillars,
counter filter indicators, custom collection headers (`platforms/custom-collections`: its
folder is kept; rename it to your collection's name if you want to use that
artwork), and the game carousel view (`gamecarousel`), which uses the default
look.

If something doesn't look right, check
`/userdata/system/logs/es_launch_stdout.log` or `es_launch_stderr.log` and
reload the theme with *Quit → Restart EmulationStation*.

License: CC-BY-NC-SA, the same as the original theme (see `LICENSE` and
`CREDITS.md`).

## Per-platform rating icons

They come from `recalbox-next` (`icon_filled.svg` / `icon_empty.svg`) and
replace the stars in `md_rating` on the *Detailed* and *Video* views. Only
platforms with their own icon are included (those identical to Recalbox's
generic one are omitted) and names were adapted to Batocera's. Non-square icons
are padded to a square, because ES requires square images. They are not tinted
with the theme's rating color.

## Clock, battery and controller indicators

On landscape screens the clock sits at the bottom right, aligned with the help
bar and with the same side margin (0.008). Clock, battery/wifi and controllers
always use the palette's help color. Controllers (`core/images/controller.svg`)
go under the battery, flush with the right edge, and turn electric green
(`39FF14`) when a button press or Hotkey is detected. ES only draws controllers
in a row, not a column: with more controllers the row grows to the left (4 fit).
On vertical screens the original position from `views/screen.xml` is kept, with
the same colors.

## Vertical system list

The selector element (`core/images/selector_narrow.svg`) is the one from
recalbox-next, in each palette's color (`systemSelectorColor`). In this view
the game counter has no box and uses the info text color.

## Added platforms and the menu veil

* **Added platforms** (not in the original Slate; artwork taken from the resource archive
  and descriptions made up, in English like the rest): `emuconfig`, `pcgames`,
  `now-playing` and `imageviewer` (screenshots). They use `images/logo.png`
  and, if present, `images/controller.png` (`imageviewer` uses `controller.svg`); `colors.xml` sets the bands and
  redefines `systemLogo` (and `systemControllerImage` where the controller is a PNG). If your screenshots folder
  has a different name on another setup, copy `platforms/imageviewer` under that name.
* **Menu**: Batocera paints the layer that darkens the background *before* the
  clock, battery, controller icons and help bar, and those use a single color
  (the palette's) that the theme cannot change while the menu is open. That is
  why `views/menu.xml` replaces that layer (`fadePath`) with a flat full-screen
  veil, one image per palette in `core/images/fade/<palette>.png`. To adjust a
  veil, edit the PNG (4×4 px; the alpha sets how much the background shows
  through).

## Layout of the theme

```
es-theme-recalboxy/
├── theme.xml
├── platforms/<system.theme>/   images/, colors.xml, systeminfo.xml, rating.xml
├── core/  colors/  help/  lang/  layouts/  views/
├── LICENSE  NOTICE.md  CREDITS.md  THIRD-PARTY-ASSETS.txt  MISSING.md
```

## License

See `LICENSE` (CC BY-NC-SA) for the theme and `NOTICE.md` for the third-party
assets that keep their own license.
