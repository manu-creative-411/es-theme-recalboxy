# Recalboxy - credits

Recalboxy is a Batocera theme derived from Slate for ES-DE (slate-es-de) by the ES-DE project, which is in turn based on [recalbox-multi](https://gitlab.com/recalbox/recalbox-themes) by the Recalbox community, prior to their license change in 2018.

Some graphics from the [Carbon](https://github.com/RetroPie/es-theme-carbon) theme by Rookervik.

Some console and controller vector graphics by Bezza191.

Some logotype graphics by Dan Patrick.


Port to Batocera EmulationStation and rename to Recalboxy: platform folders renamed to the Batocera convention, theme rewritten in Batocera format 7 (subsets, layouts per aspect ratio).

Help icons (Xbox, PlayStation, SNES and generic button sets) in `help/icons/`: assets supplied by the theme user.

Bariol Bold (`core/fonts/Bariol-Bold.ttf`): supplied by the theme user.

Color palettes, menu icons (`core/images/menu_icons/`), menu fonts (Bariol Regular / Regular Italic in `core/fonts/`) and the SNES alt, Xbox One and Arcade help icon sets: taken from the Recalbox theme.

Vertical system list layout and per-platform rating icons: taken from the Recalbox theme (recalbox-next by Supernature2k, CC BY-NC-ND 4.0 as stated in its readme).

Console/controller images, rating icons, band colors and system info added to platforms that lacked them (and the `bk`, `dice`, `moonlight`, `pico` and `dragon64` folders): taken from the Recalbox theme (recalbox-next v9 by Supernature2k, CC BY-NC-ND 4.0). Existing Recalboxy files were never overwritten.

Platform folders now live under `platforms/`. Third-party assets from recalbox-next are kept as unmodified, separately licensed copies; see `NOTICE.md` and `THIRD-PARTY-ASSETS.txt`.

System logos (`platforms/*/images/logo.svg` and the white variants `logo-w.svg`): taken from the [Carbon](https://github.com/RetroPie/es-theme-carbon) theme by Rookervik, through the Batocera fork by fabricecaruso (`es-theme-carbon`). They replace the Iconic raster logos used in earlier versions of this theme. The logos themselves are trademarks of their respective owners.

Carbon artwork added in a later pass (platform folders, logos and white logos, console pictures `consolegame.*`,
controllers `controller.svg` and the regional artwork in `platforms/*/images/us|jp|br/`): taken from the same Carbon theme
(Rookervik / fabricecaruso fork, CC BY-NC-SA, same license as this theme). Raster images were converted from PNG to WebP.
Region option, `tools/update-regions.sh` and the controller tint: written for this theme.

Background music (`core/music/`): Recalbox Main Theme 00-05 by machette, 06 (SMB) and 07 (TETRIS) by djpostka, as distributed with recalbox-next. Used as the theme's exclusive music playlist (`views/common.xml`). See `NOTICE.md`.

System information (`systeminfo.xml`) and band colors (`colors.xml`) for the 222 platforms that came from Carbon and had neither (hardware, arcade boards, source ports, stores, tools and `auto-*` collections): written for Recalboxy from general knowledge, not copied from any other theme, and covered by the theme's license. Palettes follow each platform's branding. Specifications and dates were not checked against sources, so some details may be inaccurate. Hack, region and duplicate-name folders (`nesh`, `gbah`, `megadrive-japan`, `3dsen`, ...) reuse their parent platform's data with a short note on top.

Splash images (`splash/`, `splash.xml`, `gamesplash.xml`): original, made for Recalboxy. Their text was converted to paths using Exo 2 Bold / Regular Condensed (SIL OFL), Bariol Bold / Regular (supplied by the theme user; the generic `none.svg` uses Bariol Regular) and DejaVu Sans Bold / Sans Mono Bold (DejaVu / Bitstream Vera license). Not the official logos of the distributions; see `NOTICE.md`.
