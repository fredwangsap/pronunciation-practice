# 🗣️ English Pronunciation Practice

An interactive, single-page web app for mastering **every sound in English** — from individual letters to the full set of 44 IPA phonemes, letter combinations, stress patterns, and a pronunciation game with speech recognition.

**▶️ Live demo:** https://fredwangsap.github.io/pronunciation-practice/

No install, no build step — it is one self-contained `index.html` you can open in any modern browser.

## Features

The app is organized into **6 progressive steps**:

1. **🔤 A–Z Letters** — the sound each letter makes (letter *sound* vs. letter *name*), with example words you can click to hear.
2. **🔊 20 Vowel Sounds** — all 7 short + 5 long + 8 diphthong vowels, each with articulation tips, example words, and every common spelling.
3. **🦷 24 Consonant Sounds** — all consonants grouped by type (stop, fricative, affricate, nasal, …) and voiced/voiceless, with tips and spellings.
4. **🔗 Letter Combinations** — digraphs and patterns such as `sh`, `ch`, `th`, `igh`, `tion`, `ough`, and the sounds they make.
5. **🥁 Word & Sentence Stress** — interactive syllable-stress practice plus content-word vs. grammar-word sentence stress.
6. **🎮 Pronunciation Game** — 5 levels of words to sound out, with hints, audio, and **microphone-based scoring**.

### 🔊 Click-to-hear every one of the 44 sounds
On the Vowels and Consonants steps, **tap the IPA symbol** on any card to hear that phoneme played on its own. Because browser text-to-speech cannot read raw IPA, each of the 44 sounds is mapped to a tuned pronounceable form (sustained continuants like `/s/`, light-schwa stops like `/p/`, held vowels like `/iː/`). The example-word buttons remain the precise reference for each sound.

### 🎤 Speak and get scored
The game uses the browser Speech Recognition API to listen to your pronunciation and score it, with streaks and automatic level-ups.

### 🔉 Robust text-to-speech
Click any word anywhere to hear it. The app uses the Web Speech `speechSynthesis` API with a built-in diagnostic panel and guidance if your browser blocks audio.

## Tech

- **Single file**: everything lives in [`index.html`](index.html) — HTML, CSS, and vanilla JavaScript, with no dependencies or build tooling.
- **APIs**: Web Speech API (`speechSynthesis` for playback, `SpeechRecognition` for the game).
- **Hosting**: GitHub Pages (auto-deploys from `main`).

## Running locally

Open `index.html` directly in a browser, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

> **Tip:** Speech synthesis and recognition work best in **Safari** and **Chrome**. Recognition requires microphone permission and a secure context (`https://` or `localhost`).

## A note on "44 sounds"

This app follows the standard Received Pronunciation (RP) analysis: **44 phonemes = 20 vowels + 24 consonants**, the count used in most phonetics textbooks and phonics programs.
