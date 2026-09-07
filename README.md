<p align="center">
  <img src="assets/Uplink-1024.png" alt="Uplink icon" width="128" height="128">
</p>

<h1 align="center">Uplink</h1>

<p align="center">
  <a href="release-notes/v1.0.1.md"><img src="https://img.shields.io/badge/version-1.0.1-007AFF" alt="Version 1.0.1"></a>
  <img src="https://img.shields.io/badge/language-Swift-F05138?logo=swift&amp;logoColor=white" alt="Language Swift">
  <img src="https://img.shields.io/badge/macOS-15.4%2B-333333?logo=apple&amp;logoColor=white" alt="Requires macOS 15.4 or later">
</p>

Uplink mounts remote folders over SSH as Finder volumes on macOS 15.4 or later. It includes its FUSE T and SSHFS runtime.

## Use

This release of Uplink is offered for noncommercial use only.

The bundled FUSE T binary is free for noncommercial use. Its authors require a commercial licence for commercial use or bundling with commercial software. Work or business use may fall into that category. This release does not include a commercial FUSE T licence, so do not assume that a free download covers workplace use. Contact the FUSE T authors to confirm the permissions needed for your intended use.

The bundled components keep their own licences. See the [FUSE T terms](https://github.com/macos-fuse-t/fuse-t/blob/1.2.7/License.txt) and the component notices included with the app.

## Install

Download [Uplink 1.0.1](https://github.com/SuperSonnix71/uplink-releases/releases/download/v1.0.1/Uplink-1.0.1.dmg) or read the [release notes](release-notes/v1.0.1.md).

Version 1.0.1 fixes the installer permissions that prevented some users from opening version 1.0.0. Install this version over the old copy. Your saved connections and credentials are kept.

Open the Uplink disk image, then open Uplink.pkg. The installer asks for administrator approval and places the app in `/Applications/Uplink.app`. It also adds `127.0.0.1 uplink` to the local hosts file. Existing connections and credentials are preserved during an update.

Free builds are not notarized. macOS may require you to approve opening the installer in Privacy & Security. Only approve a download whose origin you have checked. Do not disable Gatekeeper or other system protections.

## Connections

Add a connection with the server, SSH port, username, remote folder and local mount location. Choose a Finder volume name. Test the connection before mounting it. When a server is first encountered, check its host key fingerprint before approving it.

Connections can use a password saved in macOS Keychain or an existing private key. Keys with and without a passphrase are supported. Uplink references your selected key file and does not replace it. Keychain or file access may require your approval.

Select a connection and choose Mount or Unmount. You can also use the menu bar controls. Finder uses the configured volume name and identifies the mounted location as `uplink`. The local mount path is also available to terminal tools.

Each connection can be read only, mount at launch, reconnect automatically and open in Finder after a successful mount. Mounted connections cannot be edited or removed until unmounted. If a volume is busy, close files that use it and retry an ordinary unmount. A force unmount requires explicit confirmation.

Uplink appears in the Dock and menu bar and keeps one running app instance. Quit asks to unmount active connections before exiting.

## Settings and notifications

Settings includes Launch at Login and Notifications. Notifications report mount outcomes without including passwords or key contents. macOS notification permission also applies.

## Updates

Settings lets you choose whether Uplink checks for updates automatically. You can also choose Check for Updates yourself. Automatic checks remain under your control.

Updates use a disk image containing an Installer package. Each package installation requires administrator approval. The updater verifies the archive signature before extraction. An available update does not bypass your installation approval.

Version 1.0.1 uses internal build 6. Installation of a downloaded update through Check for Updates still needs testing.

Uplink's app source stays private. This page contains its public guide, downloads and update information.

## Diagnostics

Choose Export Diagnostics in Settings to save app, system and bundled runtime versions, connection state counts and fixed error categories. Diagnostics omit connection names, servers, usernames, paths, keys and credentials. Review the exported file before sharing it.
