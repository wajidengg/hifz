# Hifz حِفْظ

Memorize the Quran a few verses at a time.

**Open the app:** https://wajidengg.github.io/hifz

Hifz shows the Quran in short passages that are easy to memorize: up to 5 verses, or about half a page, whichever is shorter. Short surahs show several verses at once, and long verses appear on their own.

## Features

- **Search** by surah name or number, juz (“Juz 30” or “Para 30”), or verse (“2:255”)
- **Practice modes:** Read, Hint (first word only) and Test (tap each verse to reveal it)
- **Translation** in one block under the Arabic, with a toggle to hide it
- **Progress tracking** for each surah and all 30 juz
- **Resumes** where you left off
- **Shareable links**, for example `/hifz/#36` or `/hifz/#2:255`
- **Comfortable reading:** light and dark mode, adjustable text size, swipe or arrow keys to move between passages

Progress is saved in your own browser. There are no accounts and nothing is sent to a server.

## Files

| File | What it is |
|------|-----------|
| `index.html` | The whole app: HTML, CSS and JavaScript in one file |
| `quran.json` | Quran text, translation and juz start points |

## Data

- **Arabic text:** Tanzil Uthmani text ([tanzil.net](https://tanzil.net)), via [AlQuran.cloud](https://alquran.cloud)
- **English translation:** Muhammad Asad, via AlQuran.cloud

Changes from the downloaded data:

- The Bismillah is shown as a separate header instead of being joined to verse 1. It stays verse 1 of Al-Fatiha, and At-Tawbah has none.
- Hidden characters were removed: a byte-order mark and soft hyphens.
- A few digitization typos in the translation were fixed.
- The 30 juz start points were added.

The Arabic wording itself is unchanged. If you spot an error, please [open an issue](../../issues).

## Run it yourself

Download the two files and serve them from any static host. Opening `index.html` directly from your computer won't work, because browsers block local data files. For a quick local test:

```
python -m http.server
```

Then open `http://localhost:8000`.

## Coming later

- Audio recitation with repeat
