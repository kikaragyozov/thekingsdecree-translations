# The King's Decree — Translations

Public translation repository for the **[The King's Decree](https://www.nexusmods.com/slaythespire2)** mod for *Slay the Spire 2*.

Only the localization JSON files live here — the rest of the mod source (C#, images, etc.) is kept private while the mod stabilizes. If there's community interest for a fully open repository in the future, that may change in a later release.

## What's in here

```
translations/
├── deu/   — German
├── eng/   — English (authoritative source)
├── esp/   — European Spanish
├── fra/   — French
├── ita/   — Italian
├── jpn/   — Japanese
├── kor/   — Korean
├── pol/   — Polish
├── ptb/   — Brazilian Portuguese
├── rus/   — Russian
├── spa/   — Latin American Spanish
├── tha/   — Thai
├── tur/   — Turkish
└── zhs/   — Simplified Chinese
```

Each language folder contains three files:

- `events.json` — the King's Servant and King's Throne Room event text (~37 keys).
- `relics.json` — the three relic titles, descriptions, and flavor text.
- `settings_ui.json` — the mod name and config dropdown labels.

## Why this exists

Translations for non-English languages were produced AI-assisted, with every mechanical term cross-referenced and locked to MegaCrit's official vanilla translations (e.g., *Power* stays as the exact word vanilla uses in each language, never an invented synonym). But prose translation is imperfect — if you're a native speaker and notice a mistranslation, an awkward phrase, or vocabulary drift, your correction is genuinely valued.

## How to contribute

See [CONTRIBUTING.md](CONTRIBUTING.md) for the full workflow. Short version:

1. Fork this repository.
2. Edit the JSON file for your language.
3. Open a pull request describing what you changed.

All accepted contributors are credited in [CREDITS.md](CREDITS.md) and in the mod's Nexus page.

## Non-technical feedback

If submitting a pull request feels like too much, just leave a comment on the [Nexus mod page](https://www.nexusmods.com/slaythespire2) describing the issue and the suggested fix. The mod author reads every comment.

## License

See [LICENSE](LICENSE). Contributions are released under the same license.
