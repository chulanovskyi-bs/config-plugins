# @config-plugins/ios-stickers

Config plugin to auto-configure iOS iMessage stickers

## Install

> Tested against Expo SDK 48

```
yarn add @config-plugins/ios-stickers
```

## Example

In your app.json `plugins` array:

```json
[
  "@config-plugins/ios-stickers",
  {
    "name": "Stickers!",
    "icon": "./assets/imessage-icon.png",
    "stickerBundleId": "dev.bacon.iosstickers.stickers",
    "columns": 4,
    "stickers": [
      "./assets/stickers/annoyed.png",
      "./assets/stickers/cuddle.png",
      "./assets/stickers/crazy.png",
      "./assets/stickers/cant.png",
      "./assets/stickers/donno.png",
      "./assets/stickers/cozzy.png",
      "./assets/stickers/dork.png",
      "./assets/stickers/focus.png",
      "./assets/stickers/avocool.png",
      "./assets/stickers/coder-girl.png",
      "./assets/stickers/teapot.png"
    ]
  }
]
```

- `name`: defaults to the iOS app name
- `stickerBundleId`: custom bundle identifier for the stickers project, if not provided, it will defaults to `${ios.bundleIdentifier}.${name}-Stickers` given your expo config values.
- `icon`: defaults to the iOS app icon
- `columns`: number of stickers to render, defaults to `3`. Can be one of `2`, `3`, `4`.
- `stickers`: local file paths or remote URLs, or `{ image: "...", name: "...", accessibilityLabel: "..." }`. Order is preserved.
