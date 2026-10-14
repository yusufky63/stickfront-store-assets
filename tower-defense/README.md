# Stickfront: Tower Defense store assets

Screenshots, the feature graphic and the icons for the App Store and Google Play listings of
Stickfront: Tower Defense, in English (`en`) and Turkish (`tr`). The layout follows
[Stickfront's](../stickfront/README.md).

Made on 2026-10-14 from the game at commit `5934b67` (version 0.6.0, chapters 1-3, Endless, the
Maze). Every screenshot is the game's own screen, captured as the iOS app for the App Store and as
the Android app for Google Play.

## What goes where

| Store field | Folder | Size | Count |
| --- | --- | --- | --- |
| App Store Connect → iPhone 6.9" Display → Screenshots | `app-store/screenshots/iphone-6.9-2868x1320/<lang>/` | 2868x1320 | 10 per language |
| App Store Connect → iPhone 6.3" Display → Screenshots | `app-store/screenshots/iphone-6.3-2622x1206/<lang>/` | 2622x1206 | 10 per language |
| App Store Connect → iPad 13" Display → Screenshots | `app-store/screenshots/ipad-13-2752x2064/<lang>/` | 2752x2064 | 10 per language |
| App Store icon (comes from the build, for reference) | `app-store/icon-1024x1024/` | 1024x1024 | 1 |
| Play Console → Phone screenshots | `google-play/screenshots/phone-1920x1080/<lang>/` | 1920x1080 | 10 per language (Play takes up to 8) |
| Play Console → 7-inch and 10-inch tablet screenshots | the iPad set, `app-store/screenshots/ipad-13-2752x2064/<lang>/` | 2752x2064 (4:3) | up to 8 |
| Play Console → Feature graphic | `google-play/feature-graphic-1024x500/<lang>/` | 1024x500 | 1 per language |
| Play Console → App icon | `google-play/icon-512x512/` | 512x512 | 1 |

- **iPhone sets and Play:** the iPhone sets are about 2.17:1. Play allows the long side to be at
  most twice the short one, so Play phones get their own 16:9 set.
- **Play tablets:** they take the iPad set, which is 4:3.
- **Images:** every PNG is opaque RGB, icons included.
- **Platform names:** the App Store images and captions name no other platform or store (App Review
  2.3.10).

## Screenshots

Numbered in the suggested upload order. Google Play takes eight per device type: upload 01-08.

| # | File | English | Turkish |
| --- | --- | --- | --- |
| 01 | `01-volcano.png` | Hold the Volcano Front. Build beside the road and hold every wave. | Volkan cephesini tut. Yolun kenarına kur, her dalgaya dayan. |
| 02 | `02-branch.png` | Branch Every Defense. 12 defenses, three steps each, then one of 24 branches. | Her savunmayı dallandır. 12 savunma, üçer kademe, sonra 24 daldan biri. |
| 03 | `03-hero.png` | Send In Your Heroes. 7 heroes with their own abilities, and spells like the air strike. | Kahramanlarını gönder. Kendi yetenekleriyle 7 kahraman ve hava saldırısı gibi büyüler. |
| 04 | `04-boss.png` | Face the Bosses. The Giant blot, the Ghost ship and Ember's Furnace. | Patronlarla yüzleş. Dev leke, Hayalet gemi ve Kor'un Fırını. |
| 05 | `05-campaign.png` | 18 Hand-Made Maps. 3 chapters from village roads to a volcano pass, with stars on every map. | 18 el yapımı harita. Köy yollarından volkan geçidine 3 bölüm, her haritada yıldızlar. |
| 06 | `06-maze.png` | Build the Road Yourself. The Maze: lay walls and towers across an open field. | Yolu sen kur. Labirent: açık tarlaya duvar ve kule diz. |
| 07 | `07-flood.png` | Survive the Blot Flood. Only blots, night after night. | Leke Seli'ne dayan. Yalnızca lekeler, gece gece. |
| 08 | `08-sheet.png` | Plan Every Map. Pick your hero and two spells before the fight. | Her haritayı planla. Savaştan önce kahramanını ve iki büyünü seç. |
| 09 | `09-notebook.png` | Know Your Enemy. 20 kinds of enemy, each with a page and an answer. | Düşmanını tanı. 20 düşman türü, her birine bir sayfa ve bir karşılık. |
| 10 | `10-title.png` | Campaign, Endless and More. A tower defense drawn in ink on notebook paper. | Kampanya, Sonsuz ve fazlası. Defter kâğıdına mürekkeple çizilmiş bir kule savunması. |

- **Counts:** from the game's code (`src/content/store.ts`, `STORE_COUNTS` at 0.6.0):
  - 12 defenses with 24 branches,
  - 10 troops, 7 heroes and 6 spells,
  - 20 enemies and 3 bosses,
  - 3 chapters and 18 campaign maps,
  - 4 Endless maps and 3 Maze maps.
- **Feature graphic:** the subtitle is the App Store subtitle from the same file.
- **Matches:** they open with the game's dev hook `?play=<map>&all&demo=<seconds>`. The balance bot
  plays the map that far, then goes on playing; nothing is placed by hand.
  - In 02, the archer tower is brought to its third step so its ring shows the branch choice.
  - In 03, Pilot Frost's paratroopers and an air strike are called.
  - In 04, the bot plays 3-6 until Ember's Furnace is on the field.
- **Not in the set:** the daily siege's leaderboard needs the game server.

## To come

- **Chapters 4-6** (Winter, the Eraser, the Inkwell; 0.7-0.9): when they ship, add a few scenes and
  update the counts in the captions above and in the images.
- **Videos:** the Play and social promo (1920x1080) and an App Store preview made only of the app's
  own screen recording (1920x886 for iPhone, 1600x1200 for iPad) are planned for when the game's v2
  is done.

## Remaking them

The capture and layout scripts are in `C:\Projeler\videos\td-store\tools`:

- `td-capture.mjs <iphone|ipad|play> <en|tr>`: takes the raw screens from a dev server of the game
  on port 5199.
- `td-compose.mjs`: the screenshots.
- `td-feature.mjs`: the feature graphic.
