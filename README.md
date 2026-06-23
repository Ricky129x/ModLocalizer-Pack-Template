# ModLocalizer Pack Template

A template for creating translation packs for [ModLocalizer](https://github.com/Ricky129x/ModLocalizer).

No DLL or code required — just JSON files.

## Setup

1. Copy the `MyModJpn` folder and rename it to `YourModJpn` (or any name you like)
2. Rename `MyModJpn.json` to match your folder name (e.g. `YourModJpn.json`)
3. Edit the manifest fields: `id`, `name`, `author`, and `dependencies` (add your target mod's id)
4. Add translation files under `translations/<lang>/<mod name>/`

## File Structure

```
YourModJpn/
  YourModJpn.json        ← mod manifest
  modlocalizer.pack      ← required marker file (leave empty, do not delete)
  translations/
    jpn/
      YourMod/
        cards.json       ← translation entries for the "cards" table
        relics.json      ← translation entries for the "relics" table
        ...              ← any table name the target mod uses
```

## Translation File Format

Each file is a JSON object mapping localization keys to translated strings:

```json
{
  "MyMod_CardName_ExampleCard": "サンプルカード",
  "MyMod_CardDesc_ExampleCard": "これはサンプルの説明文です。"
}
```

The filename (without `.json`) must match the table name used by the target mod.

## Requirements

- [BaseLib](https://store.steampowered.com/app/2868840)
- Target mod (e.g. Matthias)
- [ModLocalizer](https://steamcommunity.com/workshop/filedetails/?id=3749659251)
