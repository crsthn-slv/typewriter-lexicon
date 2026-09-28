# typewriter-lexicon

Data-only repository. Word-form → lemma and per-sense synonym packs for the
[Typewriter](https://github.com/) desktop markdown editor's synonym lookup
and accent-suggestion features.

One `<lang>.json.gz` per language (gzip level 9 of a `lexicon.json` pack:
`{ v, lang, source, forms, entries }`). Downloaded on demand by the app from
jsDelivr, pinned to a commit SHA, and decompressed in the browser with the
native `DecompressionStream("gzip")`.

Languages: de, en, es, fr, it, nl, pl, pt-BR, pt-PT, ru, sv, tr.

## Source

Extracted from [Wiktionary](https://www.wiktionary.org/) by
[Wiktextract](https://github.com/tatuylonen/wiktextract) (Tatu Ylonen),
distributed by [kaikki.org](https://kaikki.org/). Dump dates and exact
source URLs per language are in `ATTRIBUTION`.

## License

CC BY-SA 4.0, inherited from Wiktionary. See `LICENSE` for the summary and
`ATTRIBUTION` for per-language sources and the changes made to the raw data
(field extraction, key normalization, regional filtering for pt-BR/pt-PT —
see `ATTRIBUTION`).

## Regeneration

Built by `scripts/lexicon/build.mjs` in the Typewriter app repository (not
published here — this repository holds only the generated data). See
`SPECs/lexico-multilingue-spec.md` there for the pipeline.
