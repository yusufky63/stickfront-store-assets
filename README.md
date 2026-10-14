# Stickfront store assets

Videos, screenshots and the feature graphic for Stickfront's App Store and Google Play listings,
plus a cut for X and the website. Every asset comes in English (`en`) and Turkish (`tr`) and sits in
a folder named for its store, its kind and its exact pixel size.

Made on 2026-10-14 from the game at commit `e7d11c8` (origin/main `007b3e5` plus the iOS app
shell). All footage is the game's own screen and renderer. Nothing is mocked up.

## What goes where

| Store field | Folder | Size | Count |
| --- | --- | --- | --- |
| App Store Connect → iPhone → App Previews | `app-store/app-previews/iphone-1920x886/<lang>/` | 1920x886, 30 fps, 29.5 s | 1 per language |
| App Store Connect → iPhone 6.9" Display → Screenshots | `app-store/screenshots/iphone-6.9-2868x1320/<lang>/` | 2868x1320 | 10 per language |
| App Store Connect → iPhone 6.3" Display → Screenshots | `app-store/screenshots/iphone-6.3-2622x1206/<lang>/` | 2622x1206 | 10 per language |
| App Store Connect → iPad 13" Display → Screenshots | `app-store/screenshots/ipad-13-2752x2064/<lang>/` | 2752x2064 | 10 per language |
| Play Console → Store listing → Video (YouTube URL) | `google-play/promo-video/1920x1080/<lang>/` | 1920x1080, 60 fps, 30 s | 1 per language |
| Play Console → Store listing → Feature graphic | `google-play/feature-graphic-1024x500/<lang>/` | 1024x500 | 1 per language |
| Play Console → Phone screenshots | `google-play/screenshots/phone-1920x1080/<lang>/` | 1920x1080 | 10 per language (Play takes up to 8) |
| Play Console → 7-inch and 10-inch tablet screenshots | `google-play/screenshots/tablet-2560x1440/<lang>/` | 2560x1440 | 10 per language (Play takes up to 8) |
| X, the website, anywhere outside the stores | `social/video/1920x1080/<lang>/` | 1920x1080, 60 fps, 30 s | full and `-small` copy |

App Store Connect holds each language in its own localization: upload `en` under English and `tr`
under Turkish. In Play Console, add Turkish as a translation of the store listing and give it the
`tr` files.

## Three cuts of one video

The same 30-second trailer is cut three ways, because each store has its own rules:

- **App Store** (`app-store/app-previews`)
  - The iPhone app's own screens, captured with the iOS interface.
  - No Google Play badge or name anywhere, as guideline 2.3.10 requires.
  - No "free" and no price (guideline 2.3.7).
  - The end card sits over gameplay, since previews show the app itself (2.3.4).
  - Encoding: 1920x886, 30 fps, H.264 High 4.0 at about 10 Mbps, 256 kbps stereo AAC, 29.5 s (the limit is 15-30 s).
- **Google Play** (`google-play/promo-video`)
  - No store badges, no "free", no calls to action.
  - Play shows a YouTube link: upload the file to YouTube first.
    - Make it public or unlisted, not private.
    - Turn ads off.
    - Allow embedding.
    - Make sure it is not age-restricted.
  - Then paste the URL into the store listing.
- **Social** (`social/video`)
  - The App Store badge and the Google Play badge, the App Store badge first, as Apple's badge guidelines ask.
  - Both trademark lines.
  - "Free · also at stickwars.dev".
  - Use this one on X and the website, never inside a store.
  - The `-small` copy is about 25 MB, for chat and phones.

All three are mixed to -14 LUFS with true peak at or under -1 dBTP.

## Screenshots

Ten screenshots per device and language, numbered in the suggested upload order. The App Store
takes all ten. Google Play takes eight per device type: upload 01-08.

| # | File | English | Turkish |
| --- | --- | --- | --- |
| 01 | `01-ground.png` | Massive Ground Battles. Command 85 units: infantry, tanks, artillery and more. | Dev kara savaşları. 85 birime komuta et: piyade, tank, topçu ve fazlası. |
| 02 | `02-ages.png` | Seven Ages in One Match. Advance from swords and legions to lasers. | Tek maçta yedi çağ. Kılıç ve lejyonlardan lazerlere ilerle. |
| 03 | `03-air.png` | Dominate the Skies. Launch jets, stealth aircraft, helicopters and dive bombers. | Gökyüzüne hükmet. Jetler, hayalet uçaklar, helikopterler ve pike bombardıman uçakları. |
| 04 | `04-sea.png` | Wage War at Sea. Deploy battleships, submarines, carriers and destroyers. | Denizde savaş. Zırhlılar, denizaltılar, uçak gemileri ve muhripler. |
| 05 | `05-nuke.png` | Call In the Atom Bomb. Build the silo, then strike anywhere on the field. | Atom bombasını çağır. Siloyu kur, sonra sahanın her yerine vur. |
| 06 | `06-story.png` | Two Story Campaigns. 20 chapters and 129 missions, from the notebook to the desk. | İki hikâye kampanyası. Defterden masaya 20 bölüm ve 129 görev. |
| 07 | `07-boss.png` | Face the Generals. Boss battles with their own tactics and lines. | Generallerle yüzleş. Kendi taktikleri ve replikleriyle patron savaşları. |
| 08 | `08-zombie.png` | Survive Zombie Night. Hold your keep night after night until dawn. | Zombi Gecesi'ni atlat. Kaleni her gece şafağa kadar tut. |
| 09 | `09-briefing.png` | Plan Every Mission. Choose a difficulty, read the objective and pick your commander. | Her görevi planla. Zorluğu seç, hedefi oku, komutanını belirle. |
| 10 | `10-title.png` | Story, Ages, Zombie Night and More. Jump into fast, clean stick-figure strategy. | Hikâye, Çağlar, Zombi Gecesi ve fazlası. Hızlı ve sade çöp adam stratejisine dal. |

- **Which build each set shows:**
  - App Store screenshots show the iOS app.
  - Google Play screenshots show the Android app.
  - Each is in its own language.
- **Image format:** every PNG is opaque RGB. App Store Connect refuses images with an alpha channel.
- **iPhone sizes:** App Store Connect asks for at least one iPhone screenshot at the medium Dynamic
  Island size (6.3", 2622x1206). The 6.9" set (2868x1320) is there for the large display.
  - Upload both, or only the 6.3" set. App Store Connect scales screenshots down for smaller iPhones.
- **Staged battles:** the battles are set up in the sandbox: the armies are placed by hand, then
  fight for a few seconds. They count toward population, so the HUD numbers are true.
  - In 07, a missile strike on each of 16-6's three rocket ramps brings the boss out.

## Numbers on screen

Counted from the game's code at `e7d11c8`. Update the assets when these change:

- 85 units, plus 18 defenses and 8 strikes and spells (111 cards).
- 7 ages: Sword, Legion, Powder, Industry, World War, Modern, Future. The Long path plays all seven in one match.
- 2 story campaigns: the notebook and the desk.
  - 20 chapters.
  - 129 missions.
  - The boss in 07 is 16-6, General Typewriter.
- 84 maps.
- Online: ranked seasons, friend rooms, 2 vs 2 co-op against bots.

## Remaking them

The sources, capture tools and notes live in the video project
`C:\Projeler\videos\stickfront-v2`. Its `tools/README.md` gives every step:

- the capture worktree of the game,
- `capture-all.sh` for the trailer footage,
- `build.mjs <lang> <target>` and `render-all.sh` for the videos,
- `store-capture.mjs` and `store-compose.mjs` for the screenshots,
- `feature.mjs` for the feature graphic.

The facts and the store rules each cut follows are in that project's `facts.md`.
