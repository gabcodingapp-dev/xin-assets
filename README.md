# XIN HUB Assets

Catalog, art and metadata for the XIN HUB app. The app pulls `manifest.json`, compares
`catalog_version`, and downloads only the endpoints it needs.

```
manifest.json                 version, counts, endpoint map
catalog/skins.json            1550 skins, 874 injectable
catalog/heroes.json           133 heroes with roles and head art
catalog/effects.json          effects + loading intros + backgrounds
catalog/tags.json             88 release tags
catalog/menus.json            quick-menu entries
catalog/lobby_sounds.json     lobby tracks with preview URLs
catalog/latest.json           newest skin drops
catalog/upgrade.json          151 upgrades, 9 free Second Forms
images/                       app art, role icons, placeholders, guide screenshots
scripts/                      mirrored intro script archives
restore/                      protection archives and stock-intro restore kit
```

## Endpoints

Raw base: `https://raw.githubusercontent.com/gabcodingapp-dev/xin-assets/main/`

## Update flow

1. Regenerate the catalog.
2. Bump `catalog_version` in `manifest.json`.
3. Push to `main`.
4. Open the app → Home → Catalog row → tap the arrow. The new version replaces the cache.

Bundled snapshots inside the app are only a fallback; the remote copy always wins.
