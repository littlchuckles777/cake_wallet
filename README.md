<div align="center">

![logo](.github/assets/cake-wallet-gh-header-2.svg)

</div>

<div align="center">

[<img height="42" src=".github/assets/app-store-badge.svg">](https://apps.apple.com/us/app/cake-wallet/id1334702542?platform=iphone)
[<img height="42" src=".github/assets/google-play-badge.png">](https://play.google.com/store/apps/details?id=com.cakewallet.cake_wallet)
[<img height="42" src=".github/assets/f-droid-badge.png">](https://fdroid.cakelabs.com)
[<img height="42" src=".github/assets/mac-store-badge.svg">](https://apps.apple.com/us/app/cake-wallet/id1334702542?platform=mac)
[<img height="42" src=".github/assets/linux-badge.svg">](https://github.com/cake-tech/cake_wallet/releases)

</div>

# Cake Wallet

[Cake Wallet](https://cakewallet.com) is an open-source, non-custodial, and private multi-currency crypto wallet for Android, iOS, macOS, and Linux.

Cake Wallet includes support for several cryptocurrencies, including:
* Monero (XMR)
* Bitcoin (BTC)
* Ethereum (ETH)
* Litecoin (LTC)
* Bitcoin Cash (BCH)
* Polygon (POL)
* Base (BASE)
* Arbitrum (ARB)
* Solana (SOL)
* Tron (TRX)
* Nano (XNO)
* Zano (ZANO)
* Decred (DCR)
* Wownero (WOW)

## Features

### App-Wide Features

* Completely noncustodial. *Your keys, your coins.*
* Built-in exchange for dozens of pairs
* Easily pay cryptocurrency invoices with fixed rate exchanges
* Buy cryptocurrency (BTC/LTC/XMR/ETH) with credit/debit/bank
* Sell cryptocurrency by bank transfer
* Scan QR codes for easy cryptocurrency transfers
* Create several wallets
* Select your own custom nodes/servers
* Address book
* Backup to an external location or iCloud
* Send to OpenAlias, Unstoppable Domains, Yats, and FIO Crypto Handles
* Set desired network fee level
* Store local transaction notes
* Extremely simple user experience
* Convenient exchange and sending templates for recurring payments
* Create donation links and invoices in the receive screen
* Robust privacy settings (eg: Tor-only connections)
* Robust security settings (eg: Cake 2FA)

### Monero Specific Features

* The Monero view key is retained on the device for maximum privacy
* Full support for Monero subaddresses and accounts
* Specify restore height for faster syncing
* Specify multiple recipients for batch sending
* Optionally set Monero nodes as trusted for faster syncing
* Specify a proxy for Monero nodes, compatible with Tor and i2p

### Bitcoin Specific Features

* Bitcoin coin control (specify specific outputs to spend)
* Automatically generate new addresses
* Specify multiple recipients for batch sending

### Ethereum Specific Features

* Store ETH and all ERC-20 tokens
* Add custom tokens by contract address
* Enable or disable Etherscan for transaction history

### Litecoin Specific Features

* Litecoin coin control (specify specific outputs to spend)
* Automatically generate new addresses
* Specify multiple recipients for batch sending

# Monero.com by Cake Wallet for Android and iOS

## Open Source Monero-Only Wallet

*Exchanging to/from other assets is also supported.*

## Links

* Website: https://monero.com
* App Store (iOS): https://apps.apple.com/app/id1601990386
* Google Play: https://play.google.com/store/apps/details?id=com.monero.app
* F-Droid: https://fdroid.cakelabs.com
* APK: https://github.com/cake-tech/cake_wallet/releases

### APK Verification

APK releases on GitHub, Accrescent, and F-Droid use the same key. They can easily be verified using [apksigner](https://developer.android.com/tools/apksigner#options-verify) or [AppVerifier](https://github.com/soupslurpr/AppVerifier).

See below for Cake Wallet's SHA-256 signing certificate hash:

```
com.cakewallet.cake_wallet
C5:40:53:AB:0F:10:D9:54:17:62:A3:DA:76:65:AE:3D:BA:5E:7C:74:3A:B4:F1:08:A5:34:9D:62:AC:10:6E:F5
```

# Support

We have 24/7 free support. Please contact support@cakewallet.com

We have excellent user guides, which are also open-source and open for contributions: https://guides.cakewallet.com

# Build Instructions

More instructions to follow

For instructions on how to build for Android: please view file `howto-build-android.md`

## iOS: Installing on a Physical iPhone

These steps install a debug build directly to an iPhone from macOS.

### Prerequisites

1. macOS with the latest Xcode installed (open Xcode once to install components).
2. [Flutter](https://docs.flutter.dev/get-started/install/macos) installed and on your `PATH`.
3. CocoaPods installed (`sudo gem install cocoapods` or `brew install cocoapods`).
4. An Apple ID added to Xcode for code signing (Xcode > Settings > Accounts).
5. A physical iPhone connected via USB (or paired for Wi‑Fi debugging).

### Setup the project

1. Fetch dependencies:
   ```sh
   flutter pub get
   ```
2. Install iOS pods:
   ```sh
   cd ios
   pod install
   cd ..
   ```

### Configure signing in Xcode

1. Open the workspace:
   ```sh
   open ios/Runner.xcworkspace
   ```
2. Select the **Runner** target.
3. Go to **Signing & Capabilities**:
   - Enable **Automatically manage signing**.
   - Choose your Team (Apple ID).
   - If needed, update the Bundle Identifier to something unique (e.g. `com.yourname.cakewallet.dev`).

### Build & run on the iPhone

Option A — **Run from Xcode**:
1. Select your connected iPhone from the device selector in Xcode.
2. Click **Run** ▶️ to build and install.

Option B — **Run from Flutter CLI**:
1. List devices:
   ```sh
   flutter devices
   ```
2. Run on the iPhone:
   ```sh
   flutter run -d <device-id>
   ```

### Troubleshooting

- If code signing fails, confirm your Team is selected and the Bundle ID is unique.
- If pods are out of date, try:
  ```sh
  cd ios
  pod repo update
  pod install
  cd ..
  ```

# Contributing

## Improving translations

Edit the applicable `strings_XX.arb` file in `res/values/` and open a pull request with the changes.

## Current list of language files:

- English
- Spanish
- French
- German
- Italian
- Portuguese
- Dutch
- Polish
- Croatian
- Russian
- Ukrainian
- Hindi
- Japanese
- Chinese
- Korean
- Thai
- Arabic
- Turkish
- Burmese
- Urdu
- Bulgarian
- Czech
- Indonesian
- Hausa
- Yoruba

## Add a new language

1. Create a new `strings_XX.arb` file in `res/values/`, replacing XX with the language's [ISO 639-1 code](https://en.wikipedia.org/wiki/ISO_639-1).

2. Edit the strings in this file, replacing XXX below with the translation for each string.

`"welcome": "Welcome to",` -> `"welcome": "XXX",`

3. For strings where there is a variable, denoted by a $ symbol and braces, such as ${status}, the string in braces should not be translated. For example, when editing line 106:

"time" : "${minutes}m ${seconds}s"

The only parts to be translated, if needed, are the values m and s after the variables.

4. Add the language to `lib/entities/language_service.dart` under both `supportedLocales` and `localeCountryCode`. Use the name of the language in the local language and in English in parentheses after for `supportedLocales`. Use the [ISO 3166-1 alpha-3 code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) for `localeCountryCode`. You must choose one country, so choose the country with the most native speakers of this language or is otherwise best associated with this language.

5. Add a relevant flag to `assets/images/flags/XXXX.png`, replacing XXXX with the 3 letters localeCountryCode. The image must be 42x26 pixels with 3 pixels of transparent margin on all 4 sides. You can resize the flag with [paint.net](https://www.getpaint.net/) to 36x20 pixels, expand the canvas to 42x26 pixels with the flag anchored in the middle, and then manually delete the 3 pixels on each side to make it transparent. Or you can use another program like Photoshop.

6. Add the new language code to `tool/utils/translation/translation_constants.dart`

## Add a new fiat currency

1. Check with [Cake Wallet support](https://guides.cakewallet.com) to see if the desired new fiat currency is available through our fiat API. Not all fiat currencies are.

2. If the currency is associated strongly with a specific issuing country, map the [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217) currency code with the applicable [ISO 3166-1 alpha-3 code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) in `lib/entities/fiat_currency.dart`. If the currency is used in a whole region or organization, then map with a reasonable interpretation of this (eg: eur countryCode for EUR symbol).

3. Add the raw mapping underneath in `lib/entities/fiat_currency.dart` following the same format as the others.

4. Add a flag of the issuing country or organization to `assets/images/flags/XXXX.png`, replacing XXXX with the ISO 3166-1 alpha-3 code used above (eg: `usa.png`, `eur.png`). Do not add this if the flag with the same name already exists. The image must be 42x26 pixels with a 3 pixels of transparent margin on all 4 sides.

---

Copyright (C) 2018-2023 Cake Labs LLC
