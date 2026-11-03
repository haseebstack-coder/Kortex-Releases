# Kortex Releases

Public download page for **Kortex SMS** installers. The source code lives in a
private repository - this repo only hosts published builds, and it is the
endpoint the in-app update banner reads:

- Update check: `https://api.github.com/repos/haseebstack-coder/Kortex-Releases/releases/latest`
- Download page: https://github.com/haseebstack-coder/Kortex-Releases/releases/latest

## Installers

| Platform | File | Requirements |
|----------|------|--------------|
| Windows PC | `Kortex SMS_<version>_x64-setup.exe` | Windows 10/11 (64-bit) |
| Android | `Kortex SMS <version>.apk` | Android 7.0+ (API 24), signed |

Step-by-step install instructions ship with every release and in the
project's `releases/README.txt`.

## How updates reach installed apps

The PC app asks this repo for the latest release (throttled to once per
installed version per 12 h) and shows a banner with a Download link when a
newer version exists. Android builds are sideloaded: install the newest APK
over the old one (same signature, no uninstall needed).

## Publishing

Releases are published automatically by CI when a `v*` tag is pushed to the
code repository (Windows installer + Android APK attached to one release).