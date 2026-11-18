
# Multilogin for Manjaro Linux

An unofficial community packaging project for running Multilogin Desktop on Manjaro Linux.

## Package Information

| Detail | Information |
|---|---|
| Application | Multilogin |
| Version | 12.17.0 |
| Package release | 1 |
| Architecture | x86_64 |
| Package format | Arch Linux |
| Target OS | Manjaro Linux |

## Installation

1. Download the `.pkg.tar.zst` file from the Releases section.
2. Open a terminal in your download folder.
3. Install the package:

```bash
sudo pacman -U ./mlxapp-12.17.0-1-x86_64.pkg.tar.zst
```

4. Launch Multilogin:

```bash
mlxapp
```

You can also search for Multilogin in your application menu.

## Dependencies

The package declares these dependencies:

- webkit2gtk-4.1
- gtk3
- libayatana-appindicator
- libx11
- glibc
- gcc-libs

Pacman handles dependency installation.

## Optional: PKGBUILD

The repository includes a PKGBUILD as a reference for the package-building process.

The original application files from the official Ubuntu package are needed to build it.

## Disclaimer

This is an unofficial community project.

It is not affiliated with, endorsed by, or maintained by Multilogin.

Multilogin is proprietary software. Please obtain the application from its official source and respect its licensing terms.

## Credits

Package conversion and testing performed on Manjaro Linux.
