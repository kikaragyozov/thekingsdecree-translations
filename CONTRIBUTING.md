# Contributing to The King's Decree translations

Thank you for considering a contribution. This guide explains how to submit a correction, what to preserve, and what changes get accepted.

## Workflow

1. **Fork** this repository on GitHub.
2. **Edit** the JSON file for the language you want to improve, e.g. `translations/jpn/events.json`.
3. **Test your JSON is still valid** — most editors show syntax errors; or run `python -c "import json; json.load(open('translations/jpn/events.json', encoding='utf-8'))"`.
4. **Commit** your changes to a branch in your fork.
5. **Open a pull request** to this repository, explaining what you changed and why. If a phrase had an obvious problem (e.g., unnatural wording, wrong gender agreement, mistranslated game term), calling it out helps review.

You'll be added to `CREDITS.md` and the mod's Nexus page credits in the next release.

## What to preserve — these are the non-negotiable rules

### 1. Color tags must stay balanced and unchanged

Every piece of text contains formatting tags like `[red]`, `[gold]`, `[green]`, `[blue]`, `[purple]`, `[jitter]`, `[sine]`, `[b]`. They render as colored or styled text in-game.

- **Never delete a tag.** If you remove `[red]X[/red]` you'll lose the red rendering.
- **Keep them balanced.** Every opening tag needs a matching closing tag.
- **Keep the word inside them** roughly matching the role — if the English has `[red]Upgrade[/red]` meaning "upgrade your card" marked in red, the translation should also mark the word for "upgrade" in red (not a different word).

### 2. Dynamic variables must stay verbatim

Placeholders like `{HpLoss}`, `{Heal}`, `{Gold}`, `{Cards}`, `{Curse}` get replaced by numbers or card names at runtime. **Do not translate them. Do not rename them. Do not remove them.**

Example: `"Lose [red]{HpLoss}[/red] HP."` → Spanish: `"Pierde [red]{HpLoss}[/red] PV."` — the `{HpLoss}` stays literal.

### 3. Use vanilla game terminology — not a synonym you think is better

Every language has the exact vanilla MegaCrit vocabulary for game mechanics. For example:

| English | German | Spanish (esp) | French |
|---------|--------|---------------|--------|
| Power (card type) | Macht | Poder | Pouvoir |
| Upgrade | Verbessere | Mejora | Améliorez |
| Downgrade | Verschlechtere | Desmejora | Détériorez |
| Rare | Seltene | Rara | Rare |
| Turn | Zug | Turno | Tour |
| Ascension | Aufstieg | Ascensión | Ascension |

If you see a game term in the translation that doesn't match vanilla STS2's term for that same concept in your language, **that is a bug and worth fixing**. If you want to replace a game term with a synonym you personally prefer but that doesn't match vanilla, that's not a bug and will likely not be accepted.

Cross-check by loading *Slay the Spire 2* in your language and looking at vanilla card text.

### 4. Proper nouns stay untranslated where vanilla would do the same

The mod's unique characters and items — "Mardan Fu Mardan", "Sultan" — are proper nouns. In transliterated scripts (Japanese katakana, Chinese, Korean, Thai), transliterate them phonetically. In Latin-alphabet languages, keep them as-is.

### 5. `THEKINGSDECREE-generic.selectionScreenPrompt` is off-limits

That key's value is copied byte-for-byte from MegaCrit's own "Choose a Card." translation for every language. Don't rewrite it.

## What gets accepted

- Fixes to clear mistranslations.
- Replacements of non-vanilla game terminology with vanilla terminology.
- Fixes to grammar, gender agreement, verb conjugation.
- Typography improvements (quote marks, spacing, punctuation) if they match vanilla STS2's convention.
- Rephrasing awkward prose for better flow, *as long as the meaning is preserved* and no game term is changed.

## What doesn't get accepted

- Changes to `eng/` — English is the authoritative source and changes there are driven by the mod author.
- Changes to `THEKINGSDECREE-generic.selectionScreenPrompt`.
- Terminology swaps toward a personal-preference synonym that diverges from vanilla STS2.
- Tone/style changes that are taste-based rather than correctness-based.
- Mass "cleanup" changes across many keys in one PR — please keep PRs focused.

## Questions

Leave an issue on the repo or comment on the [Nexus mod page](https://www.nexusmods.com/slaythespire2/mods/493).

Thanks again — every correction makes the mod better for a player who'd otherwise read awkward translated prose.
