---
# ─── identity ───────────────────────────────────────────────
id: ady-Cyrl-tr-Latn-transliteration
title: "Adyghe (ady) Cyrillic ↔ Turkish (tr) Latin Transliteration Table"
type: transliteration-table
version: 1.0.0
status: stable
updated: 2026-08-14

# ─── subject ────────────────────────────────────────────────
languages: [ady, tr]
scripts: [Cyrl, Latn]
direction: bidirectional
reversibility: designed
# RFC 6497 (BCP 47 extension T) — the standard identifier for transformed
# content. This, not the filename, is the machine-readable identifier.
transform: tr-Latn-t-ady-Cyrl
reverse-transform: ady-Cyrl-t-tr-Latn

# ─── people ─────────────────────────────────────────────────
authors:
  - name: M. Uğur Nemlioğlu
    orcid: 0000-0002-1969-2356
reviewers:
  - name: Saida Abregova Nemlioğlu
    scope: ady

# ─── provenance and use ─────────────────────────────────────
based-on: >
  Transliteration proposal by Dr. Murat Topçu (Papşu); computational suitability
  reviewed with Bülent Özden; alphabet ordering after Omniglot (ady),
  accessed 2024-10-23.
license: CC-BY-4.0
summary: >
  A grapheme-and-phoneme oriented mapping between the Adyghe Cyrillic alphabet and
  Turkish Latin letters, designed so that the conversion can also be reversed.
cite-as: >
  Nemlioğlu, M. U. (2026). Adyghe (ady) Cyrillic ↔ Turkish (tr) Latin Transliteration Table
  (Version 1.0.0) [Data set]. ady-kbd-language-resources.
  https://github.com/nemerko/ady-kbd-language-resources
machine-readable: ady-Cyrl-tr-Latn-transliteration.json
related:
  - kbd-Cyrl-tr-Latn-transliteration
---

<!-- ══════════════════════════ COVER ══════════════════════════
     Rendered from the front matter above, which is the normative
     source. If you change a field, update this block to match.
     ═══════════════════════════════════════════════════════════ -->

# Adyghe (ady) Cyrillic ↔ Turkish (tr) Latin Transliteration Table

> *A grapheme-and-phoneme oriented mapping between the Adyghe Cyrillic alphabet and
> Turkish Latin letters, designed so that the conversion can also be reversed.*

| | |
|---|---|
| **Identifier** | `ady-Cyrl-tr-Latn-transliteration` |
| **Type** | Transliteration table |
| **Version** | 1.0.0 — 2026-08-14 |
| **Status** | Stable |
| **Languages** | Adyghe (`ady`) ↔ Turkish (`tr`) |
| **Scripts** | Cyrillic (`Cyrl`) ↔ Latin (`Latn`) |
| **Transform tag** | [BCP 47 Extension T](https://www.rfc-editor.org/rfc/rfc6497): `tr-Latn-t-ady-Cyrl` — reverse `ady-Cyrl-t-tr-Latn` |
| **Direction** | Bidirectional by design; reverse conversion not yet verified |
| **Author** | M. Uğur Nemlioğlu ([ORCID](https://orcid.org/0000-0002-1969-2356)) |
| **Reviewer** | Saida Abregova Nemlioğlu (`ady`) |
| **Machine-readable** | [`ady-Cyrl-tr-Latn-transliteration.json`](./ady-Cyrl-tr-Latn-transliteration.json) |
| **Licence** | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |

> **Cite as —** Nemlioğlu, M. U. (2026). *Adyghe (ady) Cyrillic ↔ Turkish (tr) Latin Transliteration Table*
> (Version 1.0.0) [Data set]. ady-kbd-language-resources.

---

<a id="contents"></a>

## Table of contents

- [1. Scope](#scope)
- [2. Conventions](#conventions)
  - [2.1 Notation](#notation)
  - [2.2 Codepoints](#codepoints)
  - [2.3 The apostrophe](#apostrophe)
  - [2.4 Directionality and apparent collisions](#directionality)
  - [2.5 Order of application](#order)
- [3. Alphabet](#alphabet)
- [4. Tables](#tables)
  - [4.1 Lower case](#lower-case)
  - [4.2 Title case](#title-case)
  - [4.3 Upper case](#upper-case)
  - [4.4 Combination outside the alphabet](#outside-alphabet)
  - [4.5 Deliberately excluded](#excluded)
- [5. Auxiliary exemplar](#auxiliary)
  - [5.1 Dialectal letters](#dialectal)
- [6. Notes and limitations](#notes)
- [Footnotes](#footnotes)
- [References](#references)
- [Version history](#history)

---

<a id="scope"></a>

## 1. Scope

This file maps the letters of the Adyghe Cyrillic alphabet to Turkish Latin
letters. The mapping is oriented towards both the written letter and the sound
it stands for: each Adyghe letter is matched with the Turkish letter whose usual
sound value is closest to it.<sup><a id="fnref1"></a>[1](#fn1)</sup>

It was built for a practical purpose — allowing Adyghe speakers who read Latin
script but not Cyrillic to take part in corpus work — and it is shaped by that
purpose. It is not an orthographic reform proposal and it is not a phonetic
transcription; for sound values see `ady-Cyrl-ipa`, which is not published yet.

<sub>[↑ contents](#contents)</sub>

<a id="conventions"></a>

## 2. Conventions

<a id="notation"></a>

### 2.1 Notation

| Symbol | Meaning |
|---|---|
| `{…}` | a multigraph: two or more characters that behave as a single letter |
| `∅` | no output; the character is dropped in this direction |
| `A / B` | position-dependent, see [§2.4](#directionality) |
| `—` | not applicable |

<a id="codepoints"></a>

### 2.2 Codepoints

Every character is given with its Unicode codepoint. This is not decoration: it
is how a reader tells the palochka `ӏ` (U+04CF) apart from the Latin `l`
(U+006C), the Latin `I` (U+0049) and the digit `1` (U+0031) that are routinely
typed in its place. See the repository [README](../README.md).

**Codepoints in this file are generated from the characters themselves, not
typed by hand.** A mismatch between a glyph and its stated codepoint is a
defect; please report it.

<a id="apostrophe"></a>

### 2.3 The apostrophe

The apostrophe `'` (U+0027) carries meaning here; it is not decoration and not a
quotation mark.

It stands for the palochka on its own, and after a letter it marks that the
letter is glottalised. Reading `ş'üts'e` (шӏуцӏэ, *black*) aloud, the
apostrophes tell the reader where the flow of the word is interrupted — the same
signal a Turkish reader already knows from the apostrophe that separates a
suffix from a proper noun.

The three-way series `лы` → `lı` (*meat*), `лъы` → `lhı` (*blood*), `лӏы` →
`lh'ı` (*man*) shows what is at stake. Without the apostrophe the last two would
both read as `lhı`, although `лӏ` is pronounced with a glottalised, interrupted
`l`.

Words such as `ӏоф` (*job*) or `ӏэпыӏэн` (*help*) therefore transliterate as
`'of`, `'epı'en`. A leading apostrophe may look redundant at first sight, but it
is what keeps the sound distinction visible and the mapping reversible.

The apostrophe has no upper- and lower-case forms, so it cannot record whether
the palochka it stands for was capitalised. This has to be handled by the
software applying the table.

<a id="directionality"></a>

### 2.4 Directionality and apparent collisions

The table is designed to be reversible: every Adyghe letter has exactly one
Latin form, and reading the table backwards recovers the letter. Reverse
conversion has not yet been exercised on a corpus, so `reversibility` is
recorded as *designed* rather than *verified*. This section sets out the
reasoning behind that claim.

Read backwards, a Latin string can sometimes be cut in more than one place.
Where that happens, position settles the reading.

**Position-dependent forms.** Where two Latin forms are separated by `/`, the
right-hand form is used at the beginning of a word and the left-hand form
elsewhere.<sup><a id="fnref2"></a>[2](#fn2)</sup>

| Adyghe | Latin | Word-initial | Elsewhere | Also readable as |
|---|---|---|---|---|
| о | o / vo | `vo` | `o` | `в + о` |
| у | u / vu | `vu` | `u` | `в + у` |
| и | i / yi | `yi` | `i` | `й + и` |
| е | ê / yê | `yê` | `ê` | `й + е` |
| ё | ö / yö | `yö` | `ö` | `й + ё` |
| ю | ü / yü | `yü` | `ü` | `й + ю` |

The right-hand column is what a naive reverse conversion might produce instead.
It does not arise: no Adyghe word begins with these sequences, and a
word-initial `й` followed by a vowel is written with the single vowel letter.
Position alone therefore separates the two readings.

Collisions that a longer letter already absorbs do not arise at all. `ç'` could
be read as `ч` + `ӏ`, but `чӏ` is itself a letter and is consumed as one, so the
split never occurs.

**The apostrophe.** 12 entries in the tables below produce an apostrophe, so `'`
→ `ӏ` can only be applied after every longer match has been tried.

**Out of scope.** Loanwords and code-mixed material may place letters side by
side in ways native spelling does not allow. Such strings are outside the scope
of this file; the rules above describe Adyghe orthography, not arbitrary input.
Reverse conversion also assumes the input contains no all-caps writing; see
[§6](#notes).

<a id="order"></a>

### 2.5 Order of application

Because several letters are multigraphs, the table cannot be applied character
by character. **Conversion proceeds from the longest sequence to the shortest:**
all entries of the greatest length are converted first, then the next length,
and so on until every entry has been applied.

Applying the table in any other order corrupts the result — converting `ч`
before `{чӏ}` leaves a stray `ӏ` that no later rule can repair.

This method is safe **only while the source and target character sets stay
disjoint**, so that no output character can be mistaken for an input character
on a later pass. Keeping the two inventories apart is a requirement of this
file, not an accident of it.

<sub>[↑ contents](#contents)</sub>

<a id="alphabet"></a>

## 3. Alphabet

The official Adyghe alphabet has **66 letters**. Many of them are written with
two or three Unicode characters: `гъу` is one letter, not three. This is the
thing to settle before reading [§4](#tables) — the tables map *letters*, not
characters.

| # | Letter | U+ | Lower case | U+ |
|---|---|---|---|---|
| 1 | А | U+0410 | а | U+0430 |
| 2 | Б | U+0411 | б | U+0431 |
| 3 | В | U+0412 | в | U+0432 |
| 4 | Г | U+0413 | г | U+0433 |
| 5 | Гу | U+0413+U+0443 | гу | U+0433+U+0443 |
| 6 | Гъ | U+0413+U+044A | гъ | U+0433+U+044A |
| 7 | Гъу | U+0413+U+044A+U+0443 | гъу | U+0433+U+044A+U+0443 |
| 8 | Д | U+0414 | д | U+0434 |
| 9 | Дж | U+0414+U+0436 | дж | U+0434+U+0436 |
| 10 | Дз | U+0414+U+0437 | дз | U+0434+U+0437 |
| 11 | Дзу | U+0414+U+0437+U+0443 | дзу | U+0434+U+0437+U+0443 |
| 12 | Е | U+0415 | е | U+0435 |
| 13 | Ё | U+0401 | ё | U+0451 |
| 14 | Ж | U+0416 | ж | U+0436 |
| 15 | Жъ | U+0416+U+044A | жъ | U+0436+U+044A |
| 16 | Жъу | U+0416+U+044A+U+0443 | жъу | U+0436+U+044A+U+0443 |
| 17 | Жь | U+0416+U+044C | жь | U+0436+U+044C |
| 18 | З | U+0417 | з | U+0437 |
| 19 | И | U+0418 | и | U+0438 |
| 20 | Й | U+0419 | й | U+0439 |
| 21 | К | U+041A | к | U+043A |
| 22 | Ку | U+041A+U+0443 | ку | U+043A+U+0443 |
| 23 | Къ | U+041A+U+044A | къ | U+043A+U+044A |
| 24 | Къу | U+041A+U+044A+U+0443 | къу | U+043A+U+044A+U+0443 |
| 25 | Кӏ | U+041A+U+04CF | кӏ | U+043A+U+04CF |
| 26 | Кӏу | U+041A+U+04CF+U+0443 | кӏу | U+043A+U+04CF+U+0443 |
| 27 | Л | U+041B | л | U+043B |
| 28 | Лъ | U+041B+U+044A | лъ | U+043B+U+044A |
| 29 | Лӏ | U+041B+U+04CF | лӏ | U+043B+U+04CF |
| 30 | М | U+041C | м | U+043C |
| 31 | Н | U+041D | н | U+043D |
| 32 | О | U+041E | о | U+043E |
| 33 | П | U+041F | п | U+043F |
| 34 | Пӏ | U+041F+U+04CF | пӏ | U+043F+U+04CF |
| 35 | Пӏу | U+041F+U+04CF+U+0443 | пӏу | U+043F+U+04CF+U+0443 |
| 36 | Р | U+0420 | р | U+0440 |
| 37 | С | U+0421 | с | U+0441 |
| 38 | Т | U+0422 | т | U+0442 |
| 39 | Тӏ | U+0422+U+04CF | тӏ | U+0442+U+04CF |
| 40 | Тӏу | U+0422+U+04CF+U+0443 | тӏу | U+0442+U+04CF+U+0443 |
| 41 | У | U+0423 | у | U+0443 |
| 42 | Ф | U+0424 | ф | U+0444 |
| 43 | Х | U+0425 | х | U+0445 |
| 44 | Хъ | U+0425+U+044A | хъ | U+0445+U+044A |
| 45 | Хъу | U+0425+U+044A+U+0443 | хъу | U+0445+U+044A+U+0443 |
| 46 | Хь | U+0425+U+044C | хь | U+0445+U+044C |
| 47 | Ц | U+0426 | ц | U+0446 |
| 48 | Цу | U+0426+U+0443 | цу | U+0446+U+0443 |
| 49 | Цӏ | U+0426+U+04CF | цӏ | U+0446+U+04CF |
| 50 | Ч | U+0427 | ч | U+0447 |
| 51 | Чъ | U+0427+U+044A | чъ | U+0447+U+044A |
| 52 | Чӏ | U+0427+U+04CF | чӏ | U+0447+U+04CF |
| 53 | Ш | U+0428 | ш | U+0448 |
| 54 | Шъ | U+0428+U+044A | шъ | U+0448+U+044A |
| 55 | Шъу | U+0428+U+044A+U+0443 | шъу | U+0448+U+044A+U+0443 |
| 56 | Шӏ | U+0428+U+04CF | шӏ | U+0448+U+04CF |
| 57 | Шӏу | U+0428+U+04CF+U+0443 | шӏу | U+0448+U+04CF+U+0443 |
| 58 | Щ | U+0429 | щ | U+0449 |
| 59 | Ъ | U+042A | ъ | U+044A |
| 60 | Ы | U+042B | ы | U+044B |
| 61 | Ь | U+042C | ь | U+044C |
| 62 | Э | U+042D | э | U+044D |
| 63 | Ю | U+042E | ю | U+044E |
| 64 | Я | U+042F | я | U+044F |
| 65 | Ӏ | U+04C0 | ӏ | U+04CF |
| 66 | Ӏу | U+04C0+U+0443 | ӏу | U+04CF+U+0443 |

In running order, multigraphs in braces:

```text
а б в г {гу} {гъ} {гъу} д {дж} {дз} {дзу} е ё ж {жъ} {жъу} {жь} з и й к {ку} {къ} {къу} {кӏ} {кӏу} л {лъ} {лӏ} м н о п {пӏ} {пӏу} р с т {тӏ} {тӏу} у ф х {хъ} {хъу} {хь} ц {цу} {цӏ} ч {чъ} {чӏ} ш {шъ} {шъу} {шӏ} {шӏу} щ ъ ы ь э ю я ӏ {ӏу}

```

Sound values are not repeated here; `ady-Cyrl-ipa` *(not yet published)* lists
the same 66 letters in the same order with their IPA values.

[§4](#tables) maps 65 of these letters. [§4.5](#excluded) explains which letter
is left out of the mapping, and why.

<sub>[↑ contents](#contents)</sub>

<a id="tables"></a>

## 4. Tables

The three case forms are listed separately rather than derived, because Turkish
casing is not regular: `ы` upper-cases to a dotless `I` (U+0049) while `и`
upper-cases to a dotted `İ` (U+0130). In the title-case form of a multigraph
only the first character is capitalised.

All four tables below use the same columns, so a row can be compared across them
directly.

<a id="lower-case"></a>

### 4.1 Lower case

| # | ady | U+ | tr (ady) | U+ | Notes |
|---|---|---|---|---|---|
| 1 | а | U+0430 | a | U+0061 |  |
| 2 | б | U+0431 | b | U+0062 |  |
| 3 | в | U+0432 | v | U+0076 |  |
| 4 | г | U+0433 | g | U+0067 |  |
| 5 | гу | U+0433+U+0443 | gu | U+0067+U+0075 |  |
| 6 | гъ | U+0433+U+044A | ğ | U+011F |  |
| 7 | гъу | U+0433+U+044A+U+0443 | ğu | U+011F+U+0075 |  |
| 8 | д | U+0434 | d | U+0064 |  |
| 9 | дж | U+0434+U+0436 | c | U+0063 |  |
| 10 | дз | U+0434+U+0437 | dz | U+0064+U+007A |  |
| 11 | дзу | U+0434+U+0437+U+0443 | dzu | U+0064+U+007A+U+0075 |  |
| 12 | е | U+0435 | ê / yê | U+00EA / U+0079+U+00EA |  |
| 13 | ё | U+0451 | ö / yö | U+00F6 / U+0079+U+00F6 |  |
| 14 | ж | U+0436 | jj | U+006A+U+006A |  |
| 15 | жъ | U+0436+U+044A | zj | U+007A+U+006A |  |
| 16 | жъу | U+0436+U+044A+U+0443 | zjü | U+007A+U+006A+U+00FC |  |
| 17 | жь | U+0436+U+044C | j | U+006A |  |
| 18 | з | U+0437 | z | U+007A |  |
| 19 | и | U+0438 | i / yi | U+0069 / U+0079+U+0069 |  |
| 20 | й | U+0439 | y | U+0079 |  |
| 21 | к | U+043A | k | U+006B |  |
| 22 | ку | U+043A+U+0443 | ku | U+006B+U+0075 |  |
| 23 | къ | U+043A+U+044A | kh | U+006B+U+0068 |  |
| 24 | къу | U+043A+U+044A+U+0443 | khu | U+006B+U+0068+U+0075 |  |
| 25 | кӏ | U+043A+U+04CF | ç' | U+00E7+U+0027 |  |
| 26 | кӏу | U+043A+U+04CF+U+0443 | k'u | U+006B+U+0027+U+0075 |  |
| 27 | л | U+043B | l | U+006C |  |
| 28 | лъ | U+043B+U+044A | lh | U+006C+U+0068 |  |
| 29 | лӏ | U+043B+U+04CF | lh' | U+006C+U+0068+U+0027 |  |
| 30 | м | U+043C | m | U+006D |  |
| 31 | н | U+043D | n | U+006E |  |
| 32 | о | U+043E | o / vo | U+006F / U+0076+U+006F |  |
| 33 | п | U+043F | p | U+0070 |  |
| 34 | пӏ | U+043F+U+04CF | p' | U+0070+U+0027 |  |
| 35 | пӏу | U+043F+U+04CF+U+0443 | p'u | U+0070+U+0027+U+0075 |  |
| 36 | р | U+0440 | r | U+0072 |  |
| 37 | с | U+0441 | s | U+0073 |  |
| 38 | т | U+0442 | t | U+0074 |  |
| 39 | тӏ | U+0442+U+04CF | t' | U+0074+U+0027 |  |
| 40 | тӏу | U+0442+U+04CF+U+0443 | t'u | U+0074+U+0027+U+0075 |  |
| 41 | у | U+0443 | u / vu | U+0075 / U+0076+U+0075 |  |
| 42 | ф | U+0444 | f | U+0066 |  |
| 43 | х | U+0445 | x | U+0078 |  |
| 44 | хъ | U+0445+U+044A | xh | U+0078+U+0068 |  |
| 45 | хъу | U+0445+U+044A+U+0443 | xhu | U+0078+U+0068+U+0075 |  |
| 46 | хь | U+0445+U+044C | h | U+0068 |  |
| 47 | ц | U+0446 | ts | U+0074+U+0073 |  |
| 48 | цу | U+0446+U+0443 | çü | U+00E7+U+00FC |  |
| 49 | цӏ | U+0446+U+04CF | ts' | U+0074+U+0073+U+0027 |  |
| 50 | ч | U+0447 | ç | U+00E7 |  |
| 51 | чъ | U+0447+U+044A | çç | U+00E7+U+00E7 |  |
| 52 | чӏ | U+0447+U+04CF | çç' | U+00E7+U+00E7+U+0027 |  |
| 53 | ш | U+0448 | şş | U+015F+U+015F |  |
| 54 | шъ | U+0448+U+044A | şs | U+015F+U+0073 |  |
| 55 | шъу | U+0448+U+044A+U+0443 | şü | U+015F+U+00FC |  |
| 56 | шӏ | U+0448+U+04CF | ş' | U+015F+U+0027 |  |
| 57 | шӏу | U+0448+U+04CF+U+0443 | ş'ü | U+015F+U+0027+U+00FC |  |
| 58 | щ | U+0449 | ş | U+015F |  |
| 59 | ъ | U+044A | ∅ | — | see [note 4](#footnotes) |
| 60 | ы | U+044B | ı | U+0131 |  |
| 61 | ь | U+044C | ∅ | — | see [note 4](#footnotes) |
| 62 | э | U+044D | e | U+0065 |  |
| 63 | ю | U+044E | ü / yü | U+00FC / U+0079+U+00FC |  |
| 64 | я | U+044F | ya | U+0079+U+0061 |  |
| 65 | ӏ | U+04CF | ' | U+0027 | palochka — never Latin `l`, `I` or digit `1` |

<a id="title-case"></a>

### 4.2 Title case

| # | ady | U+ | tr (ady) | U+ | Notes |
|---|---|---|---|---|---|
| 1 | А | U+0410 | A | U+0041 |  |
| 2 | Б | U+0411 | B | U+0042 |  |
| 3 | В | U+0412 | V | U+0056 |  |
| 4 | Г | U+0413 | G | U+0047 |  |
| 5 | Гу | U+0413+U+0443 | Gu | U+0047+U+0075 |  |
| 6 | Гъ | U+0413+U+044A | Ğ | U+011E |  |
| 7 | Гъу | U+0413+U+044A+U+0443 | Ğu | U+011E+U+0075 |  |
| 8 | Д | U+0414 | D | U+0044 |  |
| 9 | Дж | U+0414+U+0436 | C | U+0043 |  |
| 10 | Дз | U+0414+U+0437 | Dz | U+0044+U+007A |  |
| 11 | Дзу | U+0414+U+0437+U+0443 | Dzu | U+0044+U+007A+U+0075 |  |
| 12 | Е | U+0415 | Ê / Yê | U+00CA / U+0059+U+00EA |  |
| 13 | Ё | U+0401 | Ö / Yö | U+00D6 / U+0059+U+00F6 |  |
| 14 | Ж | U+0416 | Jj | U+004A+U+006A |  |
| 15 | Жъ | U+0416+U+044A | Zj | U+005A+U+006A |  |
| 16 | Жъу | U+0416+U+044A+U+0443 | Zjü | U+005A+U+006A+U+00FC |  |
| 17 | Жь | U+0416+U+044C | J | U+004A |  |
| 18 | З | U+0417 | Z | U+005A |  |
| 19 | И | U+0418 | İ / Yi | U+0130 / U+0059+U+0069 |  |
| 20 | Й | U+0419 | Y | U+0059 |  |
| 21 | К | U+041A | K | U+004B |  |
| 22 | Ку | U+041A+U+0443 | Ku | U+004B+U+0075 |  |
| 23 | Къ | U+041A+U+044A | Kh | U+004B+U+0068 |  |
| 24 | Къу | U+041A+U+044A+U+0443 | Khu | U+004B+U+0068+U+0075 |  |
| 25 | Кӏ | U+041A+U+04CF | Ç' | U+00C7+U+0027 |  |
| 26 | Кӏу | U+041A+U+04CF+U+0443 | K'u | U+004B+U+0027+U+0075 |  |
| 27 | Л | U+041B | L | U+004C |  |
| 28 | Лъ | U+041B+U+044A | Lh | U+004C+U+0068 |  |
| 29 | Лӏ | U+041B+U+04CF | Lh' | U+004C+U+0068+U+0027 |  |
| 30 | М | U+041C | M | U+004D |  |
| 31 | Н | U+041D | N | U+004E |  |
| 32 | О | U+041E | O / Vo | U+004F / U+0056+U+006F |  |
| 33 | П | U+041F | P | U+0050 |  |
| 34 | Пӏ | U+041F+U+04CF | P' | U+0050+U+0027 |  |
| 35 | Пӏу | U+041F+U+04CF+U+0443 | P'u | U+0050+U+0027+U+0075 |  |
| 36 | Р | U+0420 | R | U+0052 |  |
| 37 | С | U+0421 | S | U+0053 |  |
| 38 | Т | U+0422 | T | U+0054 |  |
| 39 | Тӏ | U+0422+U+04CF | T' | U+0054+U+0027 |  |
| 40 | Тӏу | U+0422+U+04CF+U+0443 | T'u | U+0054+U+0027+U+0075 |  |
| 41 | У | U+0423 | U / Vu | U+0055 / U+0056+U+0075 |  |
| 42 | Ф | U+0424 | F | U+0046 |  |
| 43 | Х | U+0425 | X | U+0058 |  |
| 44 | Хъ | U+0425+U+044A | Xh | U+0058+U+0068 |  |
| 45 | Хъу | U+0425+U+044A+U+0443 | Xhu | U+0058+U+0068+U+0075 |  |
| 46 | Хь | U+0425+U+044C | H | U+0048 |  |
| 47 | Ц | U+0426 | Ts | U+0054+U+0073 |  |
| 48 | Цу | U+0426+U+0443 | Çü | U+00C7+U+00FC |  |
| 49 | Цӏ | U+0426+U+04CF | Ts' | U+0054+U+0073+U+0027 |  |
| 50 | Ч | U+0427 | Ç | U+00C7 |  |
| 51 | Чъ | U+0427+U+044A | Çç | U+00C7+U+00E7 |  |
| 52 | Чӏ | U+0427+U+04CF | Çç' | U+00C7+U+00E7+U+0027 |  |
| 53 | Ш | U+0428 | Şş | U+015E+U+015F |  |
| 54 | Шъ | U+0428+U+044A | Şs | U+015E+U+0073 |  |
| 55 | Шъу | U+0428+U+044A+U+0443 | Şü | U+015E+U+00FC |  |
| 56 | Шӏ | U+0428+U+04CF | Ş' | U+015E+U+0027 |  |
| 57 | Шӏу | U+0428+U+04CF+U+0443 | Ş'ü | U+015E+U+0027+U+00FC |  |
| 58 | Щ | U+0429 | Ş | U+015E |  |
| 59 | Ъ | U+042A | ∅ | — |  |
| 60 | Ы | U+042B | I | U+0049 |  |
| 61 | Ь | U+042C | ∅ | — |  |
| 62 | Э | U+042D | E | U+0045 |  |
| 63 | Ю | U+042E | Ü / Yü | U+00DC / U+0059+U+00FC |  |
| 64 | Я | U+042F | Ya | U+0059+U+0061 |  |
| 65 | Ӏ | U+04C0 | ' | U+0027 |  |

<a id="upper-case"></a>

### 4.3 Upper case

| # | ady | U+ | tr (ady) | U+ | Notes |
|---|---|---|---|---|---|
| 1 | А | U+0410 | A | U+0041 |  |
| 2 | Б | U+0411 | B | U+0042 |  |
| 3 | В | U+0412 | V | U+0056 |  |
| 4 | Г | U+0413 | G | U+0047 |  |
| 5 | ГУ | U+0413+U+0423 | GU | U+0047+U+0055 |  |
| 6 | ГЪ | U+0413+U+042A | Ğ | U+011E |  |
| 7 | ГЪУ | U+0413+U+042A+U+0423 | ĞU | U+011E+U+0055 |  |
| 8 | Д | U+0414 | D | U+0044 |  |
| 9 | ДЖ | U+0414+U+0416 | C | U+0043 |  |
| 10 | ДЗ | U+0414+U+0417 | DZ | U+0044+U+005A |  |
| 11 | ДЗУ | U+0414+U+0417+U+0423 | DZU | U+0044+U+005A+U+0055 |  |
| 12 | Е | U+0415 | Ê / YÊ | U+00CA / U+0059+U+00CA |  |
| 13 | Ё | U+0401 | Ö / YÖ | U+00D6 / U+0059+U+00D6 |  |
| 14 | Ж | U+0416 | JJ | U+004A+U+004A |  |
| 15 | ЖЪ | U+0416+U+042A | ZJ | U+005A+U+004A |  |
| 16 | ЖЪУ | U+0416+U+042A+U+0423 | ZJÜ | U+005A+U+004A+U+00DC |  |
| 17 | ЖЬ | U+0416+U+042C | J | U+004A |  |
| 18 | З | U+0417 | Z | U+005A |  |
| 19 | И | U+0418 | İ / Yİ | U+0130 / U+0059+U+0130 |  |
| 20 | Й | U+0419 | Y | U+0059 |  |
| 21 | К | U+041A | K | U+004B |  |
| 22 | КУ | U+041A+U+0423 | KU | U+004B+U+0055 |  |
| 23 | КЪ | U+041A+U+042A | KH | U+004B+U+0048 |  |
| 24 | КЪУ | U+041A+U+042A+U+0423 | KHU | U+004B+U+0048+U+0055 |  |
| 25 | КӀ | U+041A+U+04C0 | Ç' | U+00C7+U+0027 |  |
| 26 | КӀУ | U+041A+U+04C0+U+0423 | K'U | U+004B+U+0027+U+0055 |  |
| 27 | Л | U+041B | L | U+004C |  |
| 28 | ЛЪ | U+041B+U+042A | LH | U+004C+U+0048 |  |
| 29 | ЛӀ | U+041B+U+04C0 | LH' | U+004C+U+0048+U+0027 |  |
| 30 | М | U+041C | M | U+004D |  |
| 31 | Н | U+041D | N | U+004E |  |
| 32 | О | U+041E | O / VO | U+004F / U+0056+U+004F |  |
| 33 | П | U+041F | P | U+0050 |  |
| 34 | ПӀ | U+041F+U+04C0 | P' | U+0050+U+0027 |  |
| 35 | ПӀУ | U+041F+U+04C0+U+0423 | P'U | U+0050+U+0027+U+0055 |  |
| 36 | Р | U+0420 | R | U+0052 |  |
| 37 | С | U+0421 | S | U+0053 |  |
| 38 | Т | U+0422 | T | U+0054 |  |
| 39 | ТӀ | U+0422+U+04C0 | T' | U+0054+U+0027 |  |
| 40 | ТӀУ | U+0422+U+04C0+U+0423 | T'U | U+0054+U+0027+U+0055 |  |
| 41 | У | U+0423 | U / VU | U+0055 / U+0056+U+0055 |  |
| 42 | Ф | U+0424 | F | U+0046 |  |
| 43 | Х | U+0425 | X | U+0058 |  |
| 44 | ХЪ | U+0425+U+042A | XH | U+0058+U+0048 |  |
| 45 | ХЪУ | U+0425+U+042A+U+0423 | XHU | U+0058+U+0048+U+0055 |  |
| 46 | ХЬ | U+0425+U+042C | H | U+0048 |  |
| 47 | Ц | U+0426 | TS | U+0054+U+0053 |  |
| 48 | ЦУ | U+0426+U+0423 | ÇÜ | U+00C7+U+00DC |  |
| 49 | ЦӀ | U+0426+U+04C0 | TS' | U+0054+U+0053+U+0027 |  |
| 50 | Ч | U+0427 | Ç | U+00C7 |  |
| 51 | ЧЪ | U+0427+U+042A | ÇÇ | U+00C7+U+00C7 |  |
| 52 | ЧӀ | U+0427+U+04C0 | ÇÇ' | U+00C7+U+00C7+U+0027 |  |
| 53 | Ш | U+0428 | ŞŞ | U+015E+U+015E |  |
| 54 | ШЪ | U+0428+U+042A | ŞS | U+015E+U+0053 |  |
| 55 | ШЪУ | U+0428+U+042A+U+0423 | ŞÜ | U+015E+U+00DC |  |
| 56 | ШӀ | U+0428+U+04C0 | Ş' | U+015E+U+0027 |  |
| 57 | ШӀУ | U+0428+U+04C0+U+0423 | Ş'Ü | U+015E+U+0027+U+00DC |  |
| 58 | Щ | U+0429 | Ş | U+015E |  |
| 59 | Ъ | U+042A | ∅ | — |  |
| 60 | Ы | U+042B | I | U+0049 |  |
| 61 | Ь | U+042C | ∅ | — |  |
| 62 | Э | U+042D | E | U+0045 |  |
| 63 | Ю | U+042E | Ü / YÜ | U+00DC / U+0059+U+00DC |  |
| 64 | Я | U+042F | YA | U+0059+U+0041 |  |
| 65 | Ӏ | U+04C0 | ' | U+0027 |  |

<a id="outside-alphabet"></a>

### 4.4 Combination outside the alphabet

Not a letter of the alphabet. It is listed so that the sound change required by
the reading rules can be represented.<sup><a id="fnref3"></a>[3](#fn3)</sup>

| # | ady | U+ | tr (ady) | U+ | Notes |
|---|---|---|---|---|---|
| 26 | кӏо | U+043A+U+04CF+U+043E | k'o | U+006B+U+0027+U+006F | lower case |
| 26 | Кӏо | U+041A+U+04CF+U+043E | K'o | U+004B+U+0027+U+006F | title case |
| 26 | КӀО | U+041A+U+04C0+U+041E | K'O | U+004B+U+0027+U+004F | all caps |

<a id="excluded"></a>

### 4.5 Deliberately excluded

Present in the alphabet but not carried into the conversion table, because
converting the parts separately covers every case in which they occur
together.<sup><a id="fnref4"></a>[4](#fn4)</sup>

| # | ady | U+ | tr (ady) | U+ | Notes |
|---|---|---|---|---|---|
| 66 | ӏу | U+04CF+U+0443 | 'u | U+0027+U+0075 | covered by `ӏ` + `у` |

<sub>[↑ contents](#contents)</sub>

<a id="auxiliary"></a>

## 5. Auxiliary exemplar

Letters that occur in real material but are not part of the official Adyghe
alphabet. **They are deliberately kept out of [§4](#tables)**, so the main
tables describe the standard alphabet only. Material containing these letters
cannot be converted by §4 alone.

For their sound values see `ady-Cyrl-ipa` *(not yet published)*.

<a id="dialectal"></a>

### 5.1 Dialectal letters

| # | Letter | U+ | tr (ady) | U+ | Dialect | Example |
|---|---|---|---|---|---|---|
| 1 | `{гь}` | U+0433+U+044C | `gg` | U+0067+U+0067 | Shapsug | егьэ (jeɟɘ) = егъэджэ *reading* |
| 2 | `{кь}` | U+043A+U+044C | `kk` | U+006B+U+006B | Shapsug | кьэт (kʲɘt) = чэт *chicken* |
| 3 | `{кӏь}` | U+043A+U+04CF+U+044C | `kk'` | U+006B+U+006B+U+0027 | Shapsug | кӏьакӏьэ (kʲʼäkʲʼɘ) = кӏэнкӏэ *egg* |

Title case and all caps follow the same pattern as the tables in [§4](#tables):

| Letter | Title case | All caps |
|---|---|---|
| `{гь}` → `gg` | `{Гь}` → `Gg` | `{ГЬ}` → `GG` |
| `{кь}` → `kk` | `{Кь}` → `Kk` | `{КЬ}` → `KK` |
| `{кӏь}` → `kk'` | `{Кӏь}` → `Kk'` | `{КӀЬ}` → `KK'` |

The doubled letter is the device the main tables already use, and the added
apostrophe marks glottalisation exactly as it does there. Compare `ж` → `jj`,
`чъ` → `çç` and its glottalised counterpart `чӏ` → `çç'`.

Each of these letters ends in `ь`. Where `ь` follows `г`, `к` or `кӏ` it belongs
to one of these dialectal letters rather than standing alone, which is what
distinguishes the two cases in running
text.<sup><a id="fnref5"></a>[5](#fn5)</sup>

Order matters here as it does in [§2.5](#order): `кӏь` is three characters long
and must be converted before `кӏ` and before `к`, or it breaks apart. Longest
match first handles this without a special rule.

<sub>[↑ contents](#contents)</sub>

<a id="notes"></a>

## 6. Notes and limitations

- The reverse direction is a design goal, not a verified property. See
  [§2.4](#directionality).
- All-caps writing is not converted. The upper-case forms in
  [§4.3](#upper-case) are recorded so that the correspondence is on record, but
  the conversion has not been exercised on text written entirely in capitals.
- The apostrophe has no case distinction of its own; this has to be handled by
  the software applying the table.
- The mapping reflects the needs of one pair of languages. It has not been
  tested against other uses.

<sub>[↑ contents](#contents)</sub>

---

<a id="footnotes"></a>

## Footnotes

<a id="fn1"></a>

**1.** The mapping was built with reverse transliteration in mind, by bringing
each Adyghe letter close to the sound that the corresponding Turkish letter
usually represents — that is, at the level of both grapheme and phoneme.
[↩](#fnref1)

<a id="fn2"></a>

**2.** A form written `ê / yê` is read as `yê` when it opens a word and as `ê`
anywhere else. [↩](#fnref2)

<a id="fn3"></a>

**3.** This combination is not a letter of the alphabet. It is included so that
the sound change required by the reading rules can be represented. [↩](#fnref3)

<a id="fn4"></a>

**4.** `ӏ` and `у` each convert on their own, and converting them separately is
expected to cover every case in which they occur together. [↩](#fnref4)

<a id="fn5"></a>

**5.** `ъ` and `ь` never occur on their own; they appear only as part of a
letter, together with another character, and therefore have no transliteration
of their own. If one is left standing alone after the other letters have been
converted, it is dropped. The palochka `ӏ` differs in this respect: there are
words in which it stands alone as a letter, at the beginning of a word or inside
it. [↩](#fnref5)

<sub>[↑ contents](#contents)</sub>

<a id="references"></a>

## References

- Topçu (Papşu), M. Transliteration proposal for the Circassian languages
  *(personal communication)*.
- Omniglot. *Adyghe language, alphabet and pronunciation.*
  <https://www.omniglot.com/writing/adyghe.htm> (accessed 2024-10-23)
- ISO 639-2 language codes. Library of Congress.
  <https://www.loc.gov/standards/iso639-2/php/code_list.php>
- Davis, M., Phillips, A., Umaoka, Y. and Falk, C. (2012). *BCP 47 Extension T —
  Transformed Content.* RFC 6497. <https://www.rfc-editor.org/rfc/rfc6497>

<sub>[↑ contents](#contents)</sub>

---

<!-- ══════════════════════════ FOOTER ═════════════════════════ -->

<a id="history"></a>

## Version history

Changes to **this file only**. Repository-wide history is in
[`CHANGELOG.md`](../CHANGELOG.md). Any change that alters the result of
processing is marked ⚠ **Affects output**, whatever its version level.

### 1.0.0 — 2026-08-14

- Initial release. Nothing precedes it, so there is nothing to fix or change
  yet.
- Content carried over from the working spreadsheet. Every codepoint is
  generated from the character it describes rather than typed, and the tables,
  the alphabet listing and [§2.4](#directionality) are all produced from that
  one source, so the prose cannot drift away from the data.

<sub>[↑ contents](#contents)</sub>

---

> `ady-Cyrl-tr-Latn-transliteration` · v1.0.0 · 2026-08-14 ·
> [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) ·
> part of [ady-kbd-language-resources](https://github.com/nemerko/ady-kbd-language-resources)
