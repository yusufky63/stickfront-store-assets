# Stickfront: Tower Defense store assets

Videos, screenshots, the feature graphic and the icons for the App Store and Google Play listings
of Stickfront: Tower Defense, in English (`en`) and Turkish (`tr`). The layout follows
[Stickfront's](../stickfront/README.md).

- **Made:** 2026-10-15 from the game at commit `deb4e59`: version 2.0.0, all six chapters, the Inkwell
  at the end.
- **Source:** everything is the game's own screen, captured as the iOS app for the App Store and as
  the Android app for Google Play and social.

## What goes where

| Store field | Folder | Size | Count |
| --- | --- | --- | --- |
| App Store Connect → iPhone 6.9" Display → Screenshots | `app-store/screenshots/iphone-6.9-2868x1320/<lang>/` | 2868x1320 | 8 per language |
| App Store Connect → iPhone 6.3" Display → Screenshots | `app-store/screenshots/iphone-6.3-2622x1206/<lang>/` | 2622x1206 | 8 per language |
| App Store Connect → iPad 13" Display → Screenshots | `app-store/screenshots/ipad-13-2752x2064/<lang>/` | 2752x2064 | 8 per language |
| App Store Connect → iPhone → App Previews | `app-store/app-previews/iphone-1920x886/<lang>/` | 1920x886, 30 fps, 29 s | 1 per language |
| App Store Connect → iPad → App Previews | `app-store/app-previews/ipad-1600x1200/<lang>/` | 1600x1200, 30 fps, 29 s | 1 per language |
| App Store icon (comes from the build, for reference) | `app-store/icon-1024x1024/` | 1024x1024 | 1 |
| Play Console → Phone screenshots | `google-play/screenshots/phone-1920x1080/<lang>/` | 1920x1080 | 8 per language |
| Play Console → 7-inch and 10-inch tablet screenshots | the iPad set, `app-store/screenshots/ipad-13-2752x2064/<lang>/` | 2752x2064 (4:3) | 8 |
| Play Console → Store listing → Video (YouTube URL) | `google-play/promo-video/1920x1080/<lang>/` | 1920x1080, 60 fps, 30 s | 1 per language |
| Play Console → Feature graphic | `google-play/feature-graphic-1024x500/<lang>/` | 1024x500 | 1 per language |
| Play Console → App icon | `google-play/icon-512x512/` | 512x512 | 1 |
| X, the website, anywhere outside the stores | `social/video/1920x1080/<lang>/` | 1920x1080, 60 fps, 30 s | full and `-small` copy |

- **iPhone sets and Play:** the iPhone sets are about 2.17:1. Play allows the long side to be at
  most twice the short one, so Play phones get their own 16:9 set.
- **Play tablets:** they take the iPad set, which is 4:3.
- **Images:** every PNG is opaque RGB, icons included.
- **Platform names:** the App Store images, videos and captions name no other platform or store (App
  Review 2.3.10).

## Screenshots

The game's own 2.0.0 scene list and titles (`docs/play-yayin.md` §0, `docs/ios-yayin.md` §10), in
order. Play takes all eight.

| # | File | English | Turkish |
| --- | --- | --- | --- |
| 01 | `01-lava.png` | Hold the Ink. 29 kinds of enemy, from ink blots to Crimson's tanks. | Mürekkebi durdur. Mürekkep lekelerinden Kızıl'ın tanklarına 29 düşman türü. |
| 02 | `02-branch.png` | Branch Every Defense. 12 defenses, three steps each, then one of 24 branches. | Her savunmayı dallandır. 12 savunma, üçer kademe, sonra 24 daldan biri. |
| 03 | `03-hero.png` | Send Your Heroes. 9 heroes, each with an ability, and 6 spells. | Kahramanlarını gönder. Her birinin bir yeteneği olan 9 kahraman ve 6 büyü. |
| 04 | `04-campaign.png` | Six Chapters on One Road. 36 hand-made maps, with stars on every one. | Altı bölüm tek yolda. 36 el yapımı harita, her birinde yıldızlar. |
| 05 | `05-boss.png` | Beat the Bosses. 6 bosses, from the Giant blot to the Inkwell. | Patronları yen. Dev lekeden Hokka'ya 6 patron. |
| 06 | `06-weather.png` | Snow, Sand and Lava. Thin ice, blizzards, quicksand and sandstorms. | Kar, kum ve lav. İnce buz, tipi, bataklık kumu ve kum fırtınası. |
| 07 | `07-maze.png` | Build the Enemy's Road. The Maze: 6 open fields, walls and towers. | Düşmanın yolunu sen kur. Labirent: 6 açık tarla, duvarlar ve kuleler. |
| 08 | `08-flood.png` | Hold Till Dawn. The Blot flood: only blots, night after night. | Şafağa kadar dayan. Leke Seli: yalnızca lekeler, gece gece. |

The scenes:

- 01: 6-3, the lava fields, while the lava runs across the road.
- 02: the upgrade ring at the fourth step on 4-1, the snow field.
- 03: Major Mirage's sandstorm on 5-2, the oasis.
- 04: the campaign road at its sixth chapter.
- 05: the Inkwell and its card on 6-6.
- 06: the sandstorm over the quicksand on 5-4.
- 07: the Maze on m-6.
- 08: the Blot flood at night.

How they were made:

- **Counts:** from the game's store text (`docs/ios-yayin.md` §9, `src/content/store.ts` `STORE_COUNTS`
  at `deb4e59`):
  - 12 defenses with 24 branches, 10 troops, 9 heroes, 6 spells,
  - 29 enemies, 6 bosses,
  - 6 chapters and 36 campaign maps, 7 Endless maps, 6 Maze maps.
- **Matches:** they open with the game's dev hook `?play=<map>&all&demo=<seconds>`. The balance bot
  plays on to the moment the scene needs (the lava running, the sandstorm blowing, the Inkwell on the
  field); nothing is placed by hand. In 02 the archer tower is brought to its third step so its ring
  shows the branch choice.
- **Feature graphic:** its line is the App Store subtitle from the same file.

## Videos

- **App Store previews** (`app-store/app-previews/`):
  - Only the iOS app's own screen: no title card, no logo, no text laid over it (App Review 2.3.4).
  - Hard cuts on the music's beats: building, holding a wave, a branch on a winter map, Major
    Mirage's sandstorm, the Inkwell, the lava, the thin ice breaking, the sandstorm, the Maze, the
    Blot flood, the campaign's six chapters, the title.
  - Encoding: H.264 High 4.0 at about 10 Mbps, 30 fps, 256 kbps stereo AAC, 29 s (Apple allows
    15-30 s).
- **Play promo** (`google-play/promo-video/`) and **social** (`social/video/`): Stickfront's promo style,
  30 s.
  - Content:
    - the hook (tap a slot, build, hold the ink),
    - the four counts (12 defenses, 24 branches, 9 heroes, 6 spells),
    - an enemy roll call counting to 29 (+6 bosses),
    - the six chapters with their six bosses,
    - the campaign's 36 maps,
    - snow, sand and lava,
    - the Blot flood, the Maze, Endless and the daily siege.
  - The Play cut has no store badge, no "free" and no call to action.
  - The social cut adds "Free in the browser · tower-defense.stickwars.dev" on its end card.
  - Play shows a YouTube link: upload the file to YouTube (public or unlisted, ads off, embedding
    allowed), then paste the URL into the store listing.
- **Mix:** all are at -14 LUFS, true peak at or under -1 dBTP.

## Remaking them

The scripts are in `C:\Projeler\videos\td-store\tools`, against a dev server of the game on port 5199
(the saved game every take starts from is `td-seed.mjs`, read from the game's data):

- `td-capture.mjs <iphone|ipad|play> <en|tr>`: the raw screens.
- `td-compose.mjs`: the screenshots.
- `td-feature.mjs`: the feature graphic.
- `td-reel.mjs <play|iphone|ipad> <en|tr> <fps>`: records the video clips (`td-clips.mjs`) frame by
  frame from the dev server, on the page's own clock.
- `td-capture-rest.sh`: runs all the clips.
- `td-build.mjs <en|tr> <play|social>` and `td-preview.mjs <en|tr> <iphone|ipad>`: write the
  HyperFrames cut.
- `td-render.sh`: renders all of them and finishes the sound.
