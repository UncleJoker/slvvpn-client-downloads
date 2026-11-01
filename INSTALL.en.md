# Install the client and connect

The 123 Cloud Drive folder contains download instructions. Get installers from the [GitHub download page](https://github.com/UncleJoker/slvvpn-client-downloads/releases/latest); you do not need a drive membership to use these GitHub links.

| Device | Installer |
| --- | --- |
| Windows | `openvpn-connect-3.9.0.5008_signed.msi` — OpenVPN Connect |
| Mac | `openvpn-connect-3.8.2.6009_signed.dmg` — OpenVPN Connect |
| Android phone or tablet | `ics-openvpn-0.7.65.apk` — OpenVPN for Android |
| iPhone or iPad | [OpenVPN Connect on the App Store](https://apps.apple.com/app/openvpn-connect/id590379981) |

These are verified fixed versions, not a claim that they are the latest upstream releases.

1. **Install on your target device.** Run the Windows MSI, open the Mac DMG and follow its installation instructions, or install the Android APK after allowing installation from your browser or file manager when prompted. iPhone and iPad use the App Store. On a GitHub Release page, expand **Assets** and choose your installer; source archives are for developers.
2. **Export your connection profile.** In SLVVPN, open Settings → Multi-device, select your platform and export your certificate as a `.ovpn` file. Eligibility follows the account status shown in the app. Transfer the profile only to your own device using system sharing or AirDrop.
3. **Import and connect.** In OpenVPN Connect on Windows, Mac or iPad, use file import to add your `.ovpn` profile, then connect. In OpenVPN for Android, import the `.ovpn`, save the profile and tap it to connect. Allow the system VPN configuration when prompted.

The installer installs the application; the `.ovpn` file is your personal connection credential. Never upload a profile or private key to a public repository or public drive share. If you export a replacement profile, import the new file on your device.

GitHub and its download domains may be unavailable on some networks. Retry later, use another network, or use the [OpenVPN Connect official site](https://openvpn.net/client/) or the [Android developer's official releases](https://github.com/schwabe/ics-openvpn/releases).

Checksums, upstream sources and license information are listed in the [main download guide](README.md). The Release includes the OpenVPN Connect EULA, Android license, GPL text and corresponding Android source with pinned submodules. This download repository is maintained for SLVVPN users and is not an official OpenVPN repository.
