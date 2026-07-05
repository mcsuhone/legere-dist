# apt/ — Legere APT repository

Published automatically by CI (`reprepro`) from the `legere-app` release workflow. Once populated it contains `dists/`, `pool/`, and `key.gpg` (the repository signing public key).

## Install (once the first release is published)

The `.deb` self-registers this repository on first install, so normally you just download and install the `.deb` and updates flow through `apt` afterward. To add the repository manually:

```bash
curl -fsSL https://mcsuhone.github.io/legere-dist/apt/key.gpg | sudo tee /usr/share/keyrings/legere.gpg >/dev/null
echo "deb [signed-by=/usr/share/keyrings/legere.gpg] https://mcsuhone.github.io/legere-dist/apt stable main" | sudo tee /etc/apt/sources.list.d/legere.list
sudo apt update && sudo apt install legere
```

Updates then arrive via `sudo apt upgrade` (or automatically, via `unattended-upgrades`).

> Not yet populated — the first `v0.1.0` release will publish the initial package here.
