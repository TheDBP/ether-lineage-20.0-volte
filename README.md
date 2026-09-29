# ether-lineage-20.0-volte

**LineageOS 20.0 (Android 13) for the Nextbit Robin, and it can make phone calls again.**

The Robin's voice calls went over 3G. US carriers finished shutting 3G down in 2022, and VoLTE on this
hardware needs the IMS stack in its stock Nougat blobs — which use the binding Android 9 deleted. So
every build on 9 or newer, 18.1 included, had data and SMS but no way to place a call. This one bridges
that stack to Android 13's telephony framework. Calls work both ways with audio, verified on T-Mobile US.

`ether` / msm8992 / Snapdragon 808, 2016. `main` carries no build config; the build lives on
[`lineage-20.0-volte`](../../tree/lineage-20.0-volte).

| | |
|---|---|
| Android | 13 (LineageOS 20.0) |
| VoLTE | working, verified on T-Mobile US |
| Wi-Fi calling | not achievable on this hardware — the modem never attempts an ePDG tunnel and a newer modem build will not load |
| Images | [Releases](../../releases) |

LineageOS never carried ether past 18.1. This branch replays a 75-patch series onto the recovered 19.1
device tree ([ether-trees](https://github.com/TheDBP/ether-trees)) and is built with
[rom-forge](https://github.com/TheDBP/rom-forge), vendored as `forge/`.

Android 21 is staged separately in
[ether-lineage-21.0-volte](https://github.com/TheDBP/ether-lineage-21.0-volte). 21 is the last version
this device will get: LineageOS 22 needs a kernel of at least 4.19 and this one is 3.10.

Installing, building, what is fixed and what is not: the README on the branch.
