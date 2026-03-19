# Japanese Kana Converter

Japanese Kana Converter is a Raycast extension for converting Japanese text into hiragana and katakana. It is aimed at quick lookup for single words, kanji compounds, and short sentences directly from the Raycast command bar.

## Features

- Convert Japanese input directly from the Raycast search bar.
- Support kanji, mixed kana, and short Japanese sentences.
- Show both hiragana and katakana results at the same time.
- Copy either output with one action.

## Current Scope

- Accept Japanese input from the Raycast search bar.
- Convert kanji, mixed Japanese text, and short phrases into hiragana.
- Convert the same input into katakana.
- Provide one-click copy actions for each converted result.

## Tech Choice

- `kuroshiro` handles Japanese syllabary conversion.
- `kuroshiro-analyzer-kuromoji` provides tokenization so kanji and short sentences can be converted reliably.
- `kuromoji` supplies the dictionary used by the analyzer.

## Example Inputs

- `学校` -> `がっこう` / `ガッコウ`
- `食べる` -> `たべる` / `タベル`
- `日本語を勉強します` -> `にほんごをべんきょうします` / `ニホンゴヲベンキョウシマス`

## Repository Status

- This repository is prepared for public GitHub publishing.
- The Raycast manifest `author` value is still temporary and must be replaced with your real Raycast handle before publishing to the Raycast Store.

## Local Development

```bash
npm install
npm run dev
```

Useful checks:

```bash
npm run lint
npm run build
```

## Publish To GitHub

```bash
git init
git add .
git commit -m "feat: add initial Raycast Japanese kana converter"
gh repo create tatuan19/raycast-japanese-kana-converter --public --source=. --remote=origin --push
```

## Notes Before Publishing

- The `author` field in `package.json` is temporarily set to a public Raycast handle so local validation can pass. Replace it with your own Raycast author handle before publishing.
- The first conversion initializes the kuromoji dictionary, so the first lookup may be slightly slower than later ones.
