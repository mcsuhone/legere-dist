# legere-dist

Public **distribution surface** for [Legere](https://github.com/mcsuhone/legere-app) — the app source is private; only built, signed artifacts are published here. Served via GitHub Pages at **https://mcsuhone.github.io/legere-dist/**.

```
apt/       Debian/Ubuntu APT repository (signed) — Linux        [active]
windows/   Windows installers + update feed                     [reserved]
macos/     macOS builds + update feed                           [reserved]
```

**Do not commit artifacts here by hand.** Everything under `apt/` (and later `windows/`, `macos/`) is published automatically by CI from the `legere-app` release workflow, triggered by pushing a `vX.Y.Z` tag. See the deployment dossier in the Legere workspace for the full model.

`.nojekyll` is present so GitHub Pages serves files verbatim (no Jekyll processing).
