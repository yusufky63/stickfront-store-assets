# Stick universe store assets

App Store and Google Play assets for the Stickfront games, one folder per game. Each folder has the
same layout:

- `app-store/`
- `google-play/`
- `social/`, when the game has a social cut

Each folder also has a README saying which file goes into which store field.

| Game | Folder | What is there |
| --- | --- | --- |
| Stickfront: Land, Sea and Air | [`stickfront/`](stickfront/README.md) | Videos (App Store preview, Play promo, social), screenshots for iPhone 6.9" and 6.3", iPad 13", Play phone and tablet, the feature graphic, icons, logos |
| Stickfront: Tower Defense | [`tower-defense/`](tower-defense/README.md) | Videos (App Store previews for iPhone and iPad, Play promo, social), screenshots for iPhone 6.9" and 6.3", iPad 13" (also Play tablets) and Play phone, the feature graphic, icons |
| Stickfront: Hero | [`hero/`](hero/README.md) | Videos (upright App Store previews for iPhone and iPad, Play promo, social), upright screenshots for iPhone 6.9" and 6.3", iPad 13" (also Play tablets) and Play phone, the feature graphic, icons |

## Rules every set follows

- **Languages:** English (`en`) and Turkish (`tr`), each in its own folder.
- **Content:** the game's own screens only. The App Store sets are captured as the iOS app, the
  Google Play sets as the Android app.
- **App Store:** no other platform or store is named or shown (App Review 2.3.10), and no price is
  given (2.3.7).
  - Screenshots are opaque PNGs at App Store Connect's exact sizes.
  - Previews are 15-30 s at 30 fps or less.
- **Google Play:**
  - No store badges and no "free", "best" or calls to action in the listing images or the promo
    video.
  - A phone screenshot's long side is at most twice its short side.
- **Numbers in captions:** counted from each game's code on the day the set was made, as noted in its
  README.
