# Japanese Pronunciation
[![CI](https://github.com/tatuan19/raycast-japanese-pronunciation/actions/workflows/ci.yml/badge.svg)](https://github.com/tatuan19/raycast-japanese-pronunciation/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

Japanese Pronunciation is a Raycast extension for converting Japanese text into hiragana and katakana pronunciation. It is aimed at quick lookup for single words, kanji compounds, and short sentences directly from the Raycast command bar.

## Features

- Convert Japanese input directly from the Raycast search bar.
- Support kanji, mixed kana, and short Japanese sentences.
- Show both hiragana and katakana pronunciation at the same time.
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

## Use Cases

- Check the reading of a kanji compound quickly.
- Convert a short Japanese sentence into kana for study or pronunciation reference.
- Copy hiragana or katakana output into notes, flashcards, or other apps.

## Install For Development

1. Clone this repository.
2. Install dependencies with `npm install`.
3. Start Raycast development mode with `npm run dev`.

## Commands

- `npm run dev`
- `npm run lint`
- `npm run build`

## Raycast Store Status

- This repository is public on GitHub.
- The Raycast manifest `author` value is still temporary and must be replaced with your real Raycast handle before any Raycast Store submission.

## Notes Before Publishing

- The `author` field in `package.json` is temporarily set to a public Raycast handle so local validation can pass. Replace it with your own Raycast author handle before publishing.
- The first conversion initializes the kuromoji dictionary, so the first lookup may be slightly slower than later ones.
