# Zmist data / Дані гри «Зміст»

Repository / Репозиторій: https://github.com/OleksO/zmist-data

## Українською

Це відкриті дані гри «Зміст» (щоденна словесна головоломка). Стан на 2026-10-30: пакети рейтингів лише для днів до цієї дати.

Файли:

- `dictionary.txt` - словник іменників (лема і прапорці, по одній на рядок).
- `forms.txt` - таблиця форм слів: форма і номери лем у словнику.
- `wallwords.txt` - список слів для початкового екрана.
- `manifest.json` - опис файлів і версії даних; для кожного пакета вказано номер головоломки та дату.
- `packs/*.bin` - рейтинги близькості слів за один день (4 пакетів, дні 2026-10-26 ... 2026-10-29).
- `DATA-LICENSE.md` - умови ліцензії та авторство.

Пакети публікуються із затримкою: пакет дня містить загадане слово, тому він з'являється тут лише після того, як день минув (зазвичай щотижня або щомісяця).

Ліцензія: Creative Commons Attribution-NonCommercial-ShareAlike 4.0 (CC BY-NC-SA 4.0), https://creativecommons.org/licenses/by-nc-sa/4.0/. Некомерційне використання, із зазначенням авторства, зі збереженням тієї ж ліцензії.

Авторство: словник і таблиця форм походять зі словника VESUM проєкту dict_uk (https://github.com/brown-uk/dict_uk), версія v6.8.6: Андрій Рисін, Василь Старко, команда БрУК.

Дані змінено: ми відібрали поширені іменники та їхні форми, прибрали імена, абревіатури та непридатні записи, позначили слова прапорцями, відсіяли рідкісні слова за частотою, нормалізували текст і прибрали граматичні теги. Рейтинги порахували ми з моделями LaBSE (Apache-2.0) і spaCy `uk_core_news_lg` (MIT, вектори CC0); самі моделі не входять до даних.

Без гарантій: дані надаються як є.

## English

These are the open data files of the daily word game "Zmist" (Contexto-style). State as of 2026-10-30: ranking packs are included only for puzzle days before that date.

Files:

- `dictionary.txt` - noun dictionary (lemma and flags, one per line).
- `forms.txt` - word-form table: a form and the dictionary indexes of its lemmas.
- `wallwords.txt` - word list for the start screen.
- `manifest.json` - describes the files and the data version; every pack lists its puzzle number and date.
- `packs/*.bin` - word-closeness rankings, one per day (4 packs, days 2026-10-26 ... 2026-10-29).
- `DATA-LICENSE.md` - licence terms and credits.

Packs are published with a delay: the pack of a day holds that day's answer (rank 1), so it appears here only after the day has passed (usually in a weekly or monthly batch).

Licence: Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0), https://creativecommons.org/licenses/by-nc-sa/4.0/. Non-commercial use only, with attribution, under the same licence.

Credits: the dictionary and the form table are derived from VESUM of the dict_uk project (https://github.com/brown-uk/dict_uk), release v6.8.6, by Andriy Rysin, Vasyl Starko and the BrUK team (Андрій Рисін, Василь Старко, команда БрУК).

The data was modified: we selected common nouns and their forms, dropped names, abbreviations and unsuitable entries, marked words with flags, removed rare words by frequency, normalised the text and removed grammar tags. The rankings are our own computation, made with the models LaBSE (Apache-2.0) and spaCy `uk_core_news_lg` (MIT, vectors CC0); the models are not part of the data.

No warranty: the data is provided as is.
