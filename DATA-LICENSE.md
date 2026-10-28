# Data licence

The game data that ships with «Зміст» (the word dictionary, the form table, the per-day ranking packs and the files that describe them) is licensed under
**Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)**:
https://creativecommons.org/licenses/by-nc-sa/4.0/

This applies to the data files only (`dictionary.txt`, `forms.txt`, `packs/*.bin`, `manifest.json`, the start-screen word list `wallwords.txt` and files of the same kind, as they are in the app bundle). Where the files are published: https://github.com/OleksO/zmist-data (the files are added here with the first public release of the app; ranking packs are published for days that have already passed). The app code is a separate work and is not covered by this file. The data is kept in separate resource files so that the two stay separate.

## Attribution

The dictionary and the form table are derived from VESUM, the Ukrainian morphological dictionary of the dict_uk project (release v6.8.6):

- Copyright notice of the source: «© 2023 Андрій Рисін, Василь Старко, команда БрУК» (Andriy Rysin, Vasyl Starko, the BrUK team), as given in the README of https://github.com/brown-uk/dict_uk (the English part of the same README names 2025; see `docs/spikes/lemma-dictionary.md`). Taken from release v6.8.6, file `dict_corp_vis.txt` (sha256 `bff17035d8f088efc9f059acda38be639bc8462235e80a4d8edbc465e7a5ae11`).
- Data licence of VESUM: CC BY-NC-SA 4.0 (https://creativecommons.org/licenses/by-nc-sa/4.0/). The dict_uk README also says that its derivative projects (for example the morfologik and Hunspell releases) carry other licences; we do not use those and rely on CC BY-NC-SA 4.0 only.
- What we changed (this is an adaptation, not the original): we selected common noun lemmas and their forms, dropped names, abbreviations and other entries unsuitable for the game, marked words with flags (vulgar, junk, proper name, derivative-prone), removed rare lemmas with a frequency filter, normalised the text (lowercase, one apostrophe character, sorted), and removed all grammar tags.
- `wallwords.txt` is a hand-picked list of common nouns checked against that dictionary; it is treated as derived data under the same licence.
- No warranty: the data is provided as is, as in section 5 of the licence text (engineering note: the legal code was not re-read when writing this file).

The ranking packs order that dictionary by closeness to each daily word. They are computed with the models LaBSE (Apache-2.0) and spaCy `uk_core_news_lg` (MIT, vectors CC0; the models are not part of the data), plus hand-written overrides (our own work, written with the help of Claude), and are published under the same licence as the dictionary they index.

## What it means

- You may copy, change and share the data files, with attribution as above and a note of your changes.
- You may not use them commercially.
- If you share changed data, you must do it under CC BY-NC-SA 4.0.
- The app is free and non-commercial: no ads, no accounts, no purchases. See `docs/adr/0013-non-commercial-distribution.md`.
- The list of daily answers (`data/answers/*.tsv`), `schedule.json`, the override files (`data/overrides/*.yaml`) and the build tools are our own work and are not part of the published data files. They live in the private repository; it must not be made public with them in the tree or in the history. Note that each ranking pack has its answer at rank 1, so publishing a pack for a future day publishes that day's answer.
- `wordfreq` (code Apache-2.0, data CC BY-SA 4.0) is used only as a build-time frequency filter; no number or text from it is shipped. Whether ShareAlike reaches a cut-off derived from it is untested.

This is an engineering reading of the licence, not legal advice. Full origins and licences of every input: `docs/licenses.md` (section "Release inventory"). The icon and logo of the app are not covered by this file (their licence status is open, see the same file).
