# WordFlow: Octanove C1/C2 flashcards in 10 languages

Flashcard data for the **C1 and C2** levels of the English vocabulary list used in the WordFlow
vocabulary-learning app (iOS). A card shows a word in the learner's language, and the learner says
or types the English translation.

## Attribution

This work is an adaptation of the **Octanove Vocabulary Profile C1/C2 (version 1.0)**, created by
[Octanove Labs](http://www.octanove.com/) and published in the
[Open Language Profiles](https://github.com/openlanguageprofiles/olp-en-cefrj) repository
(file `octanove-vocabulary-profile-c1c2-1.0.csv`).

The original is licensed under the
[Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).
This adaptation is released under the **same license** (see `LICENSE`). It is exactly the C1/C2 data
shipped in the WordFlow app.

## Changes made to the original

- Kept only nouns, verbs, adjectives and adverbs; dropped prepositions, conjunctions and entries with errors in the part-of-speech field.
- Dropped entries that are already covered by the A1–B2 cards of the app, or that are not suitable as a card (abbreviations, very rare or ambiguous forms).
- Added the list of accepted English answers for every entry (American spelling first, then synonyms and British variants), and common speech-recognition mishearings that are also accepted.
- Added example sentences for the accepted answers.
- Added translations (card prompts) into 10 languages, with a short context in parentheses where the word alone would be ambiguous.
- Where several original entries are near-synonyms with the same prompt, only one card was kept.

## Files

| Path | Content |
|---|---|
| `data/en/core_C1.json`, `data/en/core_C2.json` | English side: 1001 C1 and 907 C2 cards — id, accepted answers, accepted mishearings, example sentences |
| `data/<lang>/<lang>_C1.json`, `<lang>_C2.json` | Card prompts in one language, matched to the English cards by `id` |
| `tools/octanove_translations.txt` | Source of the Russian prompts and English answers, one line per original entry: `headword\|part of speech \|\| Russian prompt \|\| answer1; answer2; …` (`SKIP` marks an excluded entry) |
| `tools/octanove_fixes.txt` | Russian prompts changed later so they do not duplicate A1–B2 cards |
| `LICENSE` | Full text of CC BY-SA 4.0 |

Languages: `ru` Russian, `fr` French, `de` German, `it` Italian, `es-419` Spanish (Latin America),
`es-ES` Spanish (Spain), `pt-BR` Portuguese (Brazil), `tr` Turkish, `ja` Japanese, `ko` Korean.
`es-ES` contains only the cards that differ from `es-419`; all other Spain cards are taken from `es-419`.

### Format

English card:

```json
{"id": "c1-exterior", "en": ["exterior", "outside", "outer surface"], "h": ["..."],
 "ex": [{"s": "The exterior of the house is painted white.", "f": "exterior", "i": 4}]}
```

- `en` — accepted answers, the first one is the main answer.
- `h` — optional: speech-recognition mishearings that are also accepted.
- `ex` — example sentences: `s` sentence, `f` the answer form used in it, `i` its character offset in `s`.

Language card: `{"id": "c1-exterior", "t": "внешняя сторона (поверхность)"}` — `t` is the prompt shown on the card.

## Reuse

You may share and adapt these files under CC BY-SA 4.0: give credit to Octanove Labs and to this adaptation, indicate
your changes, and distribute your version under the same license.

The translations and example sentences were prepared with the help of an AI model and may contain mistakes.
Corrections are welcome.

## Not covered by this license

The WordFlow app code and the A1–B2 word lists (based on the CEFR-J Wordlist, © Tono Laboratory, TUFS) are separate works
under their own terms and are not part of this repository.
