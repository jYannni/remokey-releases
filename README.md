# ReMoKey for Mac — downloads

Control a Mac's keyboard, trackpad and media keys from an iPhone over your local
Wi-Fi. This repo holds the **downloads and the update feed only** — the source
lives elsewhere.

> ## ⚠️ No release yet
>
> The first build is still going through Apple's notarization. **There is nothing
> to download from this repo yet** — the `downloads` release exists but has no
> assets attached, and `appcast.xml` is not published, so the in-app updater has
> no feed to read.
>
> Everything below describes the app as built and tested, not as currently
> downloadable. This banner comes down when the first DMG lands.

## Install

Download the latest `ReMoKey-for-Mac-*.dmg` from the
[**downloads** release](https://github.com/jYannni/remokey-releases/releases/tag/downloads),
open it, and drag **ReMoKey for Mac** to Applications.

The app is signed with a Developer ID certificate and notarized by Apple, so it
opens without a Gatekeeper warning beyond the standard "downloaded from the
internet" confirmation on first launch. It is stapled, so it also opens on a Mac
with no network connection.

On first launch a setup window walks you through granting Accessibility,
optionally starting at login, and pairing your iPhone. It appears once — reopen it
any time from the menu-bar icon → **Setup…**.

## Updates

The app checks for updates daily and installs them itself, via
[Sparkle](https://sparkle-project.org). The feed is `appcast.xml` at the root of
this repo. Every update is signed with an EdDSA key; the app rejects anything not
signed by the matching private key, so a compromise of this repo alone cannot ship
you a payload.

You can also check manually from the menu-bar icon → **Check for Updates…**.

## What you also need

ReMoKey for Mac is the *host*. It does nothing on its own — it waits for the
**ReMoKey** iPhone app to connect. Without the phone app there is nothing to
control it with.
