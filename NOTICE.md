# Notice - licenses in this package

Recalboxy is a collection of separate works under different licenses.

## 1. The theme itself - CC BY-NC-SA

`theme.xml`, `layouts/`, `views/`, `colors/`, `lang/`, the rest of the
platform artwork and everything not listed below: see `LICENSE`
(Creative Commons Attribution-NonCommercial-ShareAlike), inherited from
Slate for ES-DE / recalbox-multi.

## 2. Third-party assets - CC BY-NC-ND 4.0

The files listed in `THIRD-PARTY-ASSETS.txt` (console/controller images and
per-platform rating icons) come from the **recalbox-next** theme by
**Supernature2k**, licensed under
[CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/).

* They are included here **only as separate, unmodified copies** (a
  collection, not an adaptation) and are **not** relicensed under CC BY-NC-SA:
  they stay under their original license. Do not modify them and
  redistribute the result.
* Attribution: recalbox-next, Supernature2k, CC BY-NC-ND 4.0, copied without
  changes. Distribution is non-commercial.
* The theme's own XML (`rating.xml`, `colors.xml`, `systeminfo.xml`) that
  references those images is original configuration of this theme and is
  covered by section 1. They only point to the images; they are not copies of
  recalbox-next files.
* If you want to replace any of these images, delete the file and drop your
  own in its place; the theme falls back to default artwork if it is missing.

## 3. Background music

The tracks in `core/music/` (`Recalbox Main Theme 00` to `05` by **machette**,
`06 - SMB` and `07 - TETRIS` by **djpostka**) are the Recalbox main theme music,
also distributed in the music folder of recalbox-next.

* The only licensing information that accompanies them (recalbox-next's
  `music/licence.md`) lists the authors and **states no license**. They are
  therefore **not** covered by the CC BY-NC-SA license of the theme and no
  license is granted for them here.
* They are included as separate, unmodified audio files and are credited to
  their authors. `06 - SMB` and `07 - TETRIS` are arrangements of third-party
  compositions, whose rights stay with their respective owners.
* To remove them, delete the files in `core/music/`; the theme works the same
  without them (ES then plays the user's music).

## 4. Logos and trademarks

Logos and trademarks belong to their respective owners (see `LICENSE`).

The images in `splash/` are original wordmark compositions made for Recalboxy.
They only use the names of the distributions (Recalbox, Batocera, Knulli,
EmuELEC, RetroBat, Retrobox), which belong to their respective owners; they are
not the official logos and imply no endorsement. `splash/none.svg` is the generic
image (the theme's own name, "recalboxy"). The same images are reused by
`gamesplash.xml`. They are covered by the theme's license (section 1).
