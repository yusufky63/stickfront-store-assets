# Stickfront: Hero store assets

Screenshots, the feature graphic and the icons for the App Store and Google Play listings of
Stickfront: Hero, in English (`en`) and Turkish (`tr`). Hero is played upright, so every
screenshot is upright. The layout follows [Stickfront's](../stickfront/README.md).

- **Made:** 2026-10-15 from the game at commit `4033509` (origin/main, the S3 perks in).
- **Source:** every screenshot is the game's own screen, captured as the iOS app for the App Store and
  as the Android app for Google Play, with the phone's safe area (62 px top and 34 px bottom on
  iPhone).

## What goes where

| Store field | Folder | Size | Count |
| --- | --- | --- | --- |
| App Store Connect → iPhone 6.9" Display → Screenshots | `app-store/screenshots/iphone-6.9-1320x2868/<lang>/` | 1320x2868 | 9 per language |
| App Store Connect → iPhone 6.3" Display → Screenshots | `app-store/screenshots/iphone-6.3-1206x2622/<lang>/` | 1206x2622 | 9 per language |
| App Store Connect → iPad 13" Display → Screenshots | `app-store/screenshots/ipad-13-2064x2752/<lang>/` | 2064x2752 | 9 per language |
| App Store icon (comes from the build, for reference) | `app-store/icon-1024x1024/` | 1024x1024 | 1 |
| Play Console → Phone screenshots | `google-play/screenshots/phone-1080x1920/<lang>/` | 1080x1920 | 9 per language (Play takes up to 8) |
| Play Console → 7-inch and 10-inch tablet screenshots | the iPad set, `app-store/screenshots/ipad-13-2064x2752/<lang>/` | 2064x2752 (3:4) | up to 8 |
| Play Console → Feature graphic | `google-play/feature-graphic-1024x500/<lang>/` | 1024x500 | 1 per language |
| Play Console → App icon | `google-play/icon-512x512/` | 512x512 | 1 |

- **iPhone sets and Play:** the iPhone sets are about 1:2.17. Play allows the long side to be at most
  twice the short one, so Play phones get their own 9:16 set.
- **Images:** every PNG is opaque RGB, icons included.
- **Platform names:** the App Store images and captions name no other platform or store (App Review
  2.3.10).

## Screenshots

Numbered in the suggested upload order; the scenes and captions are Hero's own list
(`docs/ios-yayin.md` §10). Google Play takes eight per device type: upload 01-08.

| # | File | English | Turkish |
| --- | --- | --- | --- |
| 01 | `01-crowd.png` | Hold the Page Against the Ink. Walk, aim by moving, and let your weapons fire. | Mürekkebe karşı sayfayı tut. Yürü, hareketinle nişan al, silahların ateş etsin. |
| 02 | `02-cards.png` | A Card at Every Level. Pick a weapon, a power or a rare upgrade. | Her seviyede bir kart. Bir silah, bir güç ya da nadir bir yükseltme seç. |
| 03 | `03-evolved.png` | Evolve Your Weapons. Bring two cards together into something bigger. | Silahlarını evrimleştir. İki kartı birleştir, daha büyüğünü al. |
| 04 | `04-tank.png` | Outrun Crimson's Tank. Watch where its shells will fall. | Kızıl'ın tankından kaç. Mermilerinin düşeceği yere dikkat et. |
| 05 | `05-boss.png` | Climb to the Giant Blot. The forest's trail ends in its clearing. | Dev lekeye tırman. Orman yolu onun açıklığında biter. |
| 06 | `06-camp.png` | Raid Crimson's Camps. Beat the guards, take the strongbox. | Kızıl'ın kamplarını bas. Muhafızları yen, kasayı al. |
| 07 | `07-heroes.png` | 5 Commanders, 5 Companions. Each starts with its own weapon. | 5 komutan, 5 yoldaş. Her biri kendi silahıyla başlar. |
| 08 | `08-hq.png` | Spend Your Gold at Headquarters. Upgrades that stay from run to run. | Altınını Karargâh'ta harca. Koşudan koşuya kalan geliştirmeler. |
| 09 | `09-title.png` | 3 Tiers on Every Map. Village, Forest and Desert. | Her haritada 3 kademe. Köy, Orman ve Çöl. |

- **Counts:** from the game's code (`src/content/store.ts`, `STORE_COUNTS` at `4033509`): 5 heroes, 5
  companions, 3 maps, 3 tiers.
- **Feature graphic:** its line is the App Store subtitle from the same file.
- **Runs:** they open with the game's dev hook `?run=<map>&seed=<n>&ahead=<seconds>`. The balance bot
  plays the run that far, with a seasoned player's Headquarters upgrades. Staged parts:
  - 02: the level's own cards are rolled by the game until a Legendary comes up.
  - 03: the bow is set at its top step with the inkwell power, then the evolution card the game
    offers (Ink rain) is taken.
  - 04 and 06: Graphite is moved up to Crimson's tank and to the first desert camp.
  - 05: the bot climbs the forest's trail until the giant blot is out (another seed when it falls
    on the way), then Graphite stands before it.
- **iPad:** the game's own layout on a 3:4 screen puts the run in a centered upright column (its
  stylesheet's `min-aspect-ratio: 3/4` rule takes the iPad 13" upright screen too). The iPad set
  shows the app as it is.
- **Left out:** the end of a run with a new best (scene 9 in Hero's list is optional).

## To come

- **After 0.6.0 (S4):** a perk choice or an elite and its chest takes the place of a scene, and the
  counts are brought up to date.
- **Videos for 0.6.0:**
  - Play and social promo, 1920x1080.
  - App Store previews made only of the app's own screen recording: 886x1920 for iPhone, 1200x1600
    for iPad.

## Remaking them

The scripts are in `C:\Projeler\videos\hero-store\tools`, against a dev server of the game on port 5201:

- `hero-capture.mjs <iphone|ipad|play> <en|tr>`: takes the raw screens.
- `hero-compose.mjs`: the screenshots.
- `hero-feature.mjs`: the feature graphic.
