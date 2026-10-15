# Stickfront: Hero store assets

Videos, screenshots, the feature graphic and the icons for the App Store and Google Play listings
of Stickfront: Hero, in English (`en`) and Turkish (`tr`). Hero is played upright. The layout
follows [Stickfront's](../stickfront/README.md).

- **Made:** 2026-10-16 from the game at commit `d67c3b0`: version 0.8.0, with 12 maps in 4 regions
  (the Countryside, the Desert, the Mist and the Volcano), perks, elites and chests.
- **Source:** everything is the game's own screen, captured as the iOS app for the App Store and as
  the Android app for Google Play and social, with the phone's safe area (62 px top and 34 px bottom
  on iPhone).

## What goes where

| Store field | Folder | Size | Count |
| --- | --- | --- | --- |
| App Store Connect → iPhone 6.9" Display → Screenshots | `app-store/screenshots/iphone-6.9-1320x2868/<lang>/` | 1320x2868 | 10 per language |
| App Store Connect → iPhone 6.3" Display → Screenshots | `app-store/screenshots/iphone-6.3-1206x2622/<lang>/` | 1206x2622 | 10 per language |
| App Store Connect → iPad 13" Display → Screenshots | `app-store/screenshots/ipad-13-2064x2752/<lang>/` | 2064x2752 | 10 per language |
| App Store Connect → iPhone → App Previews | `app-store/app-previews/iphone-886x1920/<lang>/` | 886x1920, 30 fps, 29 s | 1 per language |
| App Store Connect → iPad → App Previews | `app-store/app-previews/ipad-1200x1600/<lang>/` | 1200x1600, 30 fps, 29 s | 1 per language |
| App Store icon (comes from the build, for reference) | `app-store/icon-1024x1024/` | 1024x1024 | 1 |
| Play Console → Phone screenshots | `google-play/screenshots/phone-1080x1920/<lang>/` | 1080x1920 | 10 per language (Play takes up to 8) |
| Play Console → 7-inch and 10-inch tablet screenshots | the iPad set, `app-store/screenshots/ipad-13-2064x2752/<lang>/` | 2064x2752 (3:4) | up to 8 |
| Play Console → Store listing → Video (YouTube URL) | `google-play/promo-video/1920x1080/<lang>/` | 1920x1080, 60 fps, 30 s | 1 per language |
| Play Console → Feature graphic | `google-play/feature-graphic-1024x500/<lang>/` | 1024x500 | 1 per language |
| Play Console → App icon | `google-play/icon-512x512/` | 512x512 | 1 |
| X, the website, anywhere outside the stores | `social/video/1920x1080/<lang>/` | 1920x1080, 60 fps, 30 s | full and `-small` copy |

- **iPhone sets and Play:** the iPhone sets are about 1:2.17. Play allows the long side to be at most
  twice the short one, so Play phones get their own 9:16 set.
- **Images:** every PNG is opaque RGB, icons included.
- **Platform names:** the App Store images, videos and captions name no other platform or store (App
  Review 2.3.10).

## Videos

- **App Store previews** (`app-store/app-previews/`):
  - Upright, only the iOS app's own screen: no title card, no logo, no text laid over it (App Review
    2.3.4).
  - Hard cuts on the music's beats: walking out, a crowd, the Caldera's lava closing in, the Misty
    Swamp, an elite, an elite chest, a perk taken, Ink rain, Crimson's tank, the giant blot, the
    heroes, the title.
  - Encoding: H.264 High 4.0 at about 10 Mbps, 30 fps, 256 kbps stereo AAC, 29 s (Apple allows
    15-30 s).
- **Play promo** (`google-play/promo-video/`) and **social** (`social/video/`):
  - The format is 16:9, because Play shows the promo in YouTube's wide player and X plays it as it
    is. The upright game runs in a column in the middle, with Stickfront's promo type on the paper
    either side.
  - Content: 30 s with:
    - the hook (move to aim, pick your cards, hold the ink),
    - the four counts (14 weapons, 30 perks, 18 kinds of blot, 11 bosses),
    - 12 maps in 4 regions, one shot for each: the Countryside, the Desert, the Mist (the Misty
      Swamp) and the Volcano (the Caldera),
    - Crimson's tank, the chests, the heroes and Headquarters,
    - the modes (maps, daily run, endless).
  - The Play cut has no store badge, no "free" and no call to action.
  - The social cut adds "Free in the browser · hero.stickwars.dev" on its end card.
  - Play shows a YouTube link: upload the file to YouTube (public or unlisted, ads off, embedding
    allowed), then paste the URL into the store listing.
- **Mix:** all are at -14 LUFS, true peak at or under -1 dBTP.

## Screenshots

Numbered in the suggested upload order; the scenes and captions follow Hero's own list
(`docs/ios-yayin.md` §10), with the 0.6.0 and 0.8.0 scenes in. Google Play takes eight per device
type: upload 01-08.

| # | File | English | Turkish |
| --- | --- | --- | --- |
| 01 | `01-crowd.png` | Hold the Page Against the Ink. Walk, aim by moving, and let your weapons fire. | Mürekkebe karşı sayfayı tut. Yürü, hareketinle nişan al, silahların ateş etsin. |
| 02 | `02-caldera.png` | 12 Maps in 4 Regions. Up to the Volcano, where the lava closes in. | 4 bölgede 12 harita. Lavın daraldığı Volkan'a kadar. |
| 03 | `03-swamp.png` | Into the Mist. Fog, poison bogs and the bog spirit. | Sise gir. Sis, zehirli bataklık ve Bataklık Ruhu. |
| 04 | `04-elite.png` | Elites With 12 Traits. Shielded, molten, splitting and more. | 12 nitelikli elitler. Kalkanlı, ateşli, bölünen ve fazlası. |
| 05 | `05-chest.png` | Open Their Chests. Elites, camps and bosses leave cards and perks. | Sandıklarını aç. Elitler, kamplar ve patronlar kart ve perk bırakır. |
| 06 | `06-perks.png` | 30 Perks. Every fifth level, a perk changes how the run plays. | 30 perk. Her 5. seviyede bir perk koşunun oynanışını değiştirir. |
| 07 | `07-evolved.png` | Evolve Your Weapons. 14 weapons, and two cards that come together into something bigger. | Silahlarını evrimleştir. 14 silah ve birleşip daha büyüğüne dönüşen iki kart. |
| 08 | `08-tank.png` | Outrun Crimson's Tank. Watch where its shells will fall. | Kızıl'ın tankından kaç. Mermilerinin düşeceği yere dikkat et. |
| 09 | `09-boss.png` | 11 Bosses. From the giant blot to the ember rider. | 11 patron. Dev lekeden Kor Atlı'ya. |
| 10 | `10-heroes.png` | 5 Commanders, 5 Companions. Each starts with its own weapon. | 5 komutan, 5 yoldaş. Her biri kendi silahıyla başlar. |

- **Counts:** from the game's store text (`docs/ios-yayin.md` §9, `src/content/store.ts`
  `STORE_COUNTS` at `d67c3b0`):
  - 12 maps in 4 regions, 3 tiers each,
  - 14 weapons, 2 evolutions, 30 perks, 12 elite traits,
  - 18 kinds of blot, 11 bosses,
  - 5 heroes, 5 companions.
- **Feature graphic:** its line is the App Store subtitle from the same file.
- **Runs:** they open with the game's dev hook `?run=<map>&seed=<n>`. The balance bot plays the run
  with a seasoned player's Headquarters upgrades, until the moment the scene needs: a time, an elite
  close by, a chest opened, Crimson's tank or the giant blot out. When the bot falls on the way,
  another seed is tried.
- **Staged parts:**
  - 04 and 05: the game's own perk offer, and the level's own cards rolled until a Legendary comes
    up.
  - 06: the bow is set at its top step with the inkwell power, then the evolution card the game
    offers (Ink rain) is taken.
  - 02, 08 and 09: Graphite is moved up to the Caldera's north-west lava pool (a few seconds before
    the shot, so the swarm catches up), Crimson's tank and the giant blot.
- **iPad:** since 0.6.0 the run fills the whole iPad screen (the column rule now starts at 751/1000).
- **Left out:** the level cards with a Legendary, the desert camp, Headquarters, the end of a run and
  the title screen; the promo shows the camp, Headquarters and the title.

## Remaking them

The scripts are in `C:\Projeler\videos\hero-store\tools`, against a dev server of the game on port 5201:

- `hero-capture.mjs <iphone|ipad|play> <en|tr>`: takes the raw screens.
- `hero-compose.mjs`: the screenshots.
- `hero-feature.mjs`: the feature graphic.
- `hero-reel.mjs <promo|iphone|ipad> <en|tr> <fps>`: records the video clips (`hero-clips.mjs`)
  frame by frame, on the page's own clock.
- `hero-build.mjs <en|tr> <play|social>` and `hero-preview.mjs <en|tr> <iphone|ipad>`: write the
  HyperFrames cut.
- `hero-video.sh [capture|render|all]`: records, renders and finishes all of them.
