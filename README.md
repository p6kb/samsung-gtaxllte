# postmarketOS Duranium on the Samsung Galaxy Tab A 10.1 LTE (SM-T585)

Part of [exynos-linux](https://exynos-linux.github.io): upstream Linux on
Samsung Exynos devices, with [postmarketOS](https://postmarketos.org)
Duranium on top. Not an official postmarketOS or Samsung project.

| | |
|---|---|
| Device | Samsung Galaxy Tab A 10.1 LTE (SM-T585), Exynos 7870 |
| Status | bring-up ([docs/STATUS.md](docs/STATUS.md)) |
| Images | Phosh, GNOME: [releases](https://github.com/p6kb/samsung-gtaxllte/releases) |
| Community | [Discord](https://discord.gg/exynos-linux) |

## Install

On a Linux PC, with the device on USB:

```
git clone https://github.com/p6kb/samsung-gtaxllte
cd samsung-gtaxllte && ./setup.sh
```

It first only puts our Linux into BOOT (Android stays as it is; `./setup.sh
undo` brings it back), then offers a full Android backup and the install.
Requirements, every step and the way back: [docs/INSTALL.md](docs/INSTALL.md).

## Updates

Installed devices update from the
[releases](https://github.com/p6kb/samsung-gtaxllte/releases) (`updatectl update`, or the
software centre): A/B, signed, with automatic fallback to the previous
version. The images are rebuilt automatically on every postmarketOS
publish. Release channels carry only builds verified on the device; the
`-dev` channels carry every build and a root-over-USB debug layer, for
development devices only. [docs/RELEASES.md](docs/RELEASES.md)

Vendor firmware is not included: the installer takes it from your own
stock firmware, on your PC.

## Development

- What works: [docs/STATUS.md](docs/STATUS.md), hardware:
  [docs/HARDWARE.md](docs/HARDWARE.md), tests:
  [docs/TESTPLAN.md](docs/TESTPLAN.md)
- Layout: [docs/STRUCTURE.md](docs/STRUCTURE.md), configuration:
  [config.toml](config.toml) / [docs/CONFIG.md](docs/CONFIG.md)
- A local image, exactly as CI builds it:
  `scripts/build-image --ui phosh --channel dev`
- Agents: [CLAUDE.md](CLAUDE.md)

## License

Our code: GPL-2.0 (see [LICENSE](LICENSE)) unless a file says otherwise.
postmarketOS, its packages and the upstream projects keep their own
licenses. Samsung's firmware is Samsung's and is never distributed here.
