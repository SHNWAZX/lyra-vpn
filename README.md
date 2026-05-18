# Lyra VPN for Android

Lyra VPN is a GPLv3 Android VPN client forked from the open-source ProtonVPN Android app.

This fork changes the visible app name, package ID, launcher icon, deep-link scheme, and APK archive name for a separate Lyra VPN build. It also disables in-app upgrade/payment launchers and the home upsell carousel. It does not bypass Proton paid entitlements or unlock Proton VPN Plus servers.

## Important

- Original source: <https://github.com/ProtonVPN/android-app>
- Original copyright: Copyright (c) 2019 Proton AG and later contributors
- License: GPLv3, see [LICENSE](LICENSE)
- Android application ID: `app.lyra.vpn`
- App deep-link scheme: `lyravpn`

To operate Lyra VPN as a real independent VPN service, connect this client to your own legal VPN backend, API, accounts, server list, certificates, and infrastructure. The stock Proton API/service endpoints are not yours to re-sell or bypass.

## Build

Install Android SDK, NDK, CMake, SWIG, and JDK 17, then run:

```bash
./gradlew assembleProductionVanillaOpenSourceDebug
```

For a signed release APK:

```bash
./gradlew assembleProductionVanillaOpenSourceRelease \
  -PkeyStoreFilePath=<keystore> \
  -PkeyStoreKeyAlias=<alias> \
  -PkeyStorePassword=<pass> \
  -PkeyStoreKeyPassword=<key-pass>
```
