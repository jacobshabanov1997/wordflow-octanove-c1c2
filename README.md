# WordFlow: Octanove C1/C2 — Russian translations and accepted answers

Russian flashcard data for the **C1 and C2** levels of the English vocabulary list used in the
WordFlow vocabulary-learning app (iOS). A card shows a Russian word, and the learner
says or types the English translation.

## Attribution

This work is an adaptation of the **Octanove Vocabulary Profile C1/C2 (version 1.0)**, created by
[Octanove Labs](http://www.octanove.com/) and published in the
[Open Language Profiles](https://github.com/openlanguageprofiles/olp-en-cefrj) repository
(file `octanove-vocabulary-profile-c1c2-1.0.csv`).

The original is licensed under the
[Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).
This adaptation is released under the **same license** (see `LICENSE`).

## Changes made to the original

- Kept only nouns, verbs, adjectives and adverbs; dropped prepositions, conjunctions and entries with errors in the part-of-speech field.
- Dropped entries that are already covered by the A1–B2 cards of the app, or that are not suitable as a card (abbreviations, very rare or ambiguous forms).
- Added a Russian translation for every entry, with a short Russian context in parentheses where the Russian word alone would be ambiguous.
- Added the list of accepted English answers (American spelling first, then synonyms and British variants).
- Where several original entries are near-synonyms with the same Russian prompt, only one card was kept.

## Files

| File | Content |
|---|---|
| `words_C1.json` | 1001 cards, level C1 |
| `words_C2.json` | 907 cards, level C2 |
| `translations.txt` | Source of the translations, one line per entry: `headword|part of speech || Russian prompt || answer1; answer2; …` (`SKIP` marks an excluded entry) |
| `LICENSE` | Full text of CC BY-SA 4.0 |

Card format (JSON): `{"id": "c1-exterior", "ru": "внешняя сторона (поверхность)", "en": ["exterior", "outside", "outer surface"], "level": "C1"}`.
The first item of `en` is the main answer.

## Reuse

You may share and adapt these files under CC BY-SA 4.0: give credit to Octanove Labs and to this adaptation, indicate
your changes, and distribute your version under the same license.

The translations were prepared with the help of an AI model and may contain mistakes. Corrections are welcome.

## Not covered by this license

The WordFlow app code and the A1–B2 word lists (based on the CEFR-J Wordlist, © Tono Laboratory, TUFS) are separate works
under their own terms and are not part of this repository.
