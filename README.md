<div align="center">

<img src="snap/gui/sonora.png" alt="Sonora logo" width="128" />

# Sonora

**Music streaming and your local library in one native app.**

[![sonora](https://snapcraft.io/sonora/badge.svg)](https://snapcraft.io/sonora)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architectures: amd64 and arm64](https://img.shields.io/badge/Architectures-amd64%20%7C%20arm64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [Sonora](https://github.com/sonorahq/sonora), with lyrics, themes, gapless playback and scrobbling.

</div>

---

## Getting Started

<a href="https://snapcraft.io/sonora"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install sonora
sonora
```

Choose a music service or add your local music folder in the app.

## Configure

Manage accounts, music folders and themes in the app. There are no `snap set` options.

| Optional access | Command |
| --- | --- |
| Music on removable storage | `sudo snap connect sonora:removable-media` |

App data and cached music stay in `~/snap/sonora/common/` between updates.

## Limitations

- Streaming services retain their account and subscription requirements.
- Protected playback may require installing Widevine through Sonora. Google's Linux Widevine download is unavailable on ARM64.
- Discord Rich Presence cannot reach a host Discord installation.
- Settings from a native installation are not imported automatically. Updates are managed by snapd.

## Build

```bash
git clone https://github.com/sidalit/sonora-snap.git
cd sonora-snap
sudo snap install snapcraft --classic
snapcraft pack
```

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/sonora-snap/issues).
- **Application bugs:** [report them upstream](https://github.com/sonorahq/sonora/issues).

## License

Snap packaging: [MIT](https://github.com/sidalit/sonora-snap/blob/main/LICENSE).
