---
# ─── identity ───────────────────────────────────────────────
id: kbd-Cyrl-tr-Latn-transliteration
title: "Kabardian (kbd) Cyrillic ↔ Turkish (tr) Latin Transliteration Table"
type: transliteration-table
version: 1.0.0
status: stable
updated: 2026-08-14

# ─── subject ────────────────────────────────────────────────
languages: [kbd, tr]
scripts: [Cyrl, Latn]
direction: bidirectional
reversibility: designed
# RFC 6497 (BCP 47 extension T) — the standard identifier for transformed
# content. This, not the filename, is the machine-readable identifier.
transform: tr-Latn-t-kbd-Cyrl
reverse-transform: kbd-Cyrl-t-tr-Latn

# ─── people ─────────────────────────────────────────────────
authors:
  - name: M. Uğur Nemlioğlu
    orcid: 0000-0002-1969-2356
reviewers:
  - name: Murat Topçu
    scope: kbd

# ─── provenance and use ─────────────────────────────────────
based-on: >
  Transliteration proposal by Dr. Murat Topçu (Papşu); computational suitability
  reviewed with Bülent Özden; alphabet ordering after Omniglot (kbd),
  accessed 2024-10-23.
license: CC-BY-4.0
summary: >
  A grapheme-and-phoneme oriented mapping between the Kabardian Cyrillic alphabet and
  Turkish Latin letters, designed so that the conversion can also be reversed.
cite-as: >
  Nemlioğlu, M. U. (2026). Kabardian (kbd) Cyrillic ↔ Turkish (tr) Latin Transliteration Table
  (Version 1.0.0) [Data set]. ady-kbd-language-resources.
  https://github.com/nemerko/ady-kbd-language-resources
machine-readable: kbd-Cyrl-tr-Latn-transliteration.json
related:
  - ady-Cyrl-tr-Latn-transliteration
---

<!-- ══════════════════════════ COVER ══════════════════════════
     Rendered from the front matter above, which is the normative
     source. If you change a field, update this block to match.
     ═══════════════════════════════════════════════════════════ -->

# Kabardian (kbd) Cyrillic ↔ Turkish (tr) Latin Transliteration Table

> *A grapheme-and-phoneme oriented mapping between the Kabardian Cyrillic alphabet and
> Turkish Latin letters, designed so that the conversion can also be reversed.*

| | |
|---|---|
| **Identifier** | `kbd-Cyrl-tr-Latn-transliteration` |
| **Type** | Transliteration table |
| **Version** | 1.0.0 — 2026-08-14 |
| **Status** | Stable |
| **Languages** | Kabardian (`kbd`) ↔ Turkish (`tr`) |
| **Scripts** | Cyrillic (`Cyrl`) ↔ Latin (`Latn`) |
| **Transform tag** | [BCP 47 Extension T](https://www.rfc-editor.org/rfc/rfc6497): `tr-Latn-t-kbd-Cyrl` — reverse `kbd-Cyrl-t-tr-Latn` |
| **Direction** | Bidirectional by design; reverse conversion not yet verified |
| **Author** | M. Uğur Nemlioğlu ([ORCID](https://orcid.org/0000-0002-1969-2356)) |
| **Reviewer** | Murat Topçu (`kbd`) |
| **Machine-readable** | [`kbd-Cyrl-tr-Latn-transliteration.json`](./kbd-Cyrl-tr-Latn-transliteration.json) |
| **Licence** | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |

> **Cite as —** Nemlioğlu, M. U. (2026). *Kabardian (kbd) Cyrillic ↔ Turkish (tr) Latin Transliteration Table*
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
  - [4.4 Deliberately excluded](#excluded)
- [5. Auxiliary exemplar](#auxiliary)
  - [5.1 Dialectal letters](#dialectal)
  - [5.2 Normalisation before use](#normalisation)
- [6. Notes and limitations](#notes)
- [Footnotes](#footnotes)
- [References](#references)
- [Version history](#history)

---

<a id="scope"></a>

## 1. Scope

This file maps the letters of the Kabardian Cyrillic alphabet to Turkish Latin
letters. The mapping is oriented towards both the written letter and the sound
it stands for: each Kabardian letter is matched with the Turkish letter whose
usual sound value is closest to it.<sup><a id="fnref1"></a>[1](#fn1)</sup>

It was built for a practical purpose — allowing Kabardian speakers who read
Latin script but not Cyrillic to take part in corpus work — and it is shaped by
that purpose. It is not an orthographic reform proposal and it is not a phonetic
transcription; for sound values see `kbd-Cyrl-ipa`, which is not published yet.

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
letter is glottalised. Reading `f'ıts'e` (фӏыцӏэ, *black*) aloud, the
apostrophes tell the reader where the flow of the word is interrupted — the same
signal a Turkish reader already knows from the apostrophe that separates a
suffix from a proper noun.

The three-way series `лы` → `lı` (*meat*), `лъы` → `lhı` (*blood*), `лӏы` →
`lh'ı` (*man*) shows what is at stake. Without the apostrophe the last two would
both read as `lhı`, although `лӏ` is pronounced with a glottalised, interrupted
`l`.

Words such as `ӏуэху` (*job*) or `дэӏэпыкъун` (*help*) therefore transliterate
as `'uexu`, `de'epıkhun`. A leading apostrophe may look redundant at first
sight, but it is what keeps the sound distinction visible and the mapping
reversible.

The apostrophe has no upper- and lower-case forms, so it cannot record whether
the palochka it stands for was capitalised. This has to be handled by the
software applying the table.

<a id="directionality"></a>

### 2.4 Directionality and apparent collisions

The table is designed to be reversible: every Kabardian letter has exactly one
Latin form, and reading the table backwards recovers the letter. Reverse
conversion has not yet been exercised on a corpus, so `reversibility` is
recorded as *designed* rather than *verified*. This section sets out the
reasoning behind that claim.

Read backwards, a Latin string can sometimes be cut in more than one place.
Where that happens, position settles the reading.

**Position-dependent forms.** Where two Latin forms are separated by `/`, the
right-hand form is used at the beginning of a word and the left-hand form
elsewhere.<sup><a id="fnref2"></a>[2](#fn2)</sup>

| Kabardian | Latin | Word-initial | Elsewhere | Also readable as |
|---|---|---|---|---|
| о | o / vo | `vo` | `o` | `в + о` |
| у | u / vu | `vu` | `u` | `в + у` |
| и | i / yi | `yi` | `i` | `й + и` |
| е | ê / yê | `yê` | `ê` | `й + е` |
| ё | ö / yö | `yö` | `ö` | `й + ё` |
| ю | ü / yü | `yü` | `ü` | `й + ю` |

The right-hand column is what a naive reverse conversion might produce instead.
It does not arise: no Kabardian word begins with these sequences, and a
word-initial `й` followed by a vowel is written with the single vowel letter.
Position alone therefore separates the two readings.

Collisions that a longer letter already absorbs do not arise at all. `ç'` could
be read as `ч` + `ӏ`, but `чӏ` is itself a letter and is consumed as one, so the
split never occurs. In kbd, `чӏ` is normalised to `кӏь` before use (see
[§5.2](#normalisation)), so it does not arise there either.

**The apostrophe.** 9 entries in the tables below produce an apostrophe, so `'`
→ `ӏ` can only be applied after every longer match has been tried.

**Out of scope.** Loanwords and code-mixed material may place letters side by
side in ways native spelling does not allow. Such strings are outside the scope
of this file; the rules above describe Kabardian orthography, not arbitrary
input. Reverse conversion also assumes the input contains no all-caps writing;
see [§6](#notes).

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

The official Kabardian alphabet has **59 letters**. Many of them are written
with two or three Unicode characters: `гъу` is one letter, not three. This is
the thing to settle before reading [§4](#tables) — the tables map *letters*, not
characters.

| # | Letter | U+ | Lower case | U+ |
|---|---|---|---|---|
| 1 | А | U+0410 | а | U+0430 |
| 2 | Э | U+042D | э | U+044D |
| 3 | Б | U+0411 | б | U+0431 |
| 4 | В | U+0412 | в | U+0432 |
| 5 | Г | U+0413 | г | U+0433 |
| 6 | Гу | U+0413+U+0443 | гу | U+0433+U+0443 |
| 7 | Гъ | U+0413+U+044A | гъ | U+0433+U+044A |
| 8 | Гъу | U+0413+U+044A+U+0443 | гъу | U+0433+U+044A+U+0443 |
| 9 | Д | U+0414 | д | U+0434 |
| 10 | Дж | U+0414+U+0436 | дж | U+0434+U+0436 |
| 11 | Дз | U+0414+U+0437 | дз | U+0434+U+0437 |
| 12 | Е | U+0415 | е | U+0435 |
| 13 | Ё | U+0401 | ё | U+0451 |
| 14 | Ж | U+0416 | ж | U+0436 |
| 15 | Жь | U+0416+U+044C | жь | U+0436+U+044C |
| 16 | З | U+0417 | з | U+0437 |
| 17 | И | U+0418 | и | U+0438 |
| 18 | Й | U+0419 | й | U+0439 |
| 19 | К | U+041A | к | U+043A |
| 20 | Ку | U+041A+U+0443 | ку | U+043A+U+0443 |
| 21 | Къ | U+041A+U+044A | къ | U+043A+U+044A |
| 22 | Къу | U+041A+U+044A+U+0443 | къу | U+043A+U+044A+U+0443 |
| 23 | Кхъ | U+041A+U+0445+U+044A | кхъ | U+043A+U+0445+U+044A |
| 24 | Кхъу | U+041A+U+0445+U+044A+U+0443 | кхъу | U+043A+U+0445+U+044A+U+0443 |
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
| 35 | Р | U+0420 | р | U+0440 |
| 36 | С | U+0421 | с | U+0441 |
| 37 | Т | U+0422 | т | U+0442 |
| 38 | Тӏ | U+0422+U+04CF | тӏ | U+0442+U+04CF |
| 39 | У | U+0423 | у | U+0443 |
| 40 | Ф | U+0424 | ф | U+0444 |
| 41 | Фӏ | U+0424+U+04CF | фӏ | U+0444+U+04CF |
| 42 | Х | U+0425 | х | U+0445 |
| 43 | Ху | U+0425+U+0443 | ху | U+0445+U+0443 |
| 44 | Хъ | U+0425+U+044A | хъ | U+0445+U+044A |
| 45 | Хъу | U+0425+U+044A+U+0443 | хъу | U+0445+U+044A+U+0443 |
| 46 | Хь | U+0425+U+044C | хь | U+0445+U+044C |
| 47 | Ц | U+0426 | ц | U+0446 |
| 48 | Цӏ | U+0426+U+04CF | цӏ | U+0446+U+04CF |
| 49 | Ч | U+0427 | ч | U+0447 |
| 50 | Ш | U+0428 | ш | U+0448 |
| 51 | Щ | U+0429 | щ | U+0449 |
| 52 | Щӏ | U+0429+U+04CF | щӏ | U+0449+U+04CF |
| 53 | Ъ | U+042A | ъ | U+044A |
| 54 | Ы | U+042B | ы | U+044B |
| 55 | Ь | U+042C | ь | U+044C |
| 56 | Ю | U+042E | ю | U+044E |
| 57 | Я | U+042F | я | U+044F |
| 58 | Ӏ | U+04C0 | ӏ | U+04CF |
| 59 | Ӏу | U+04C0+U+0443 | ӏу | U+04CF+U+0443 |

In running order, multigraphs in braces:

```text
а э б в г {гу} {гъ} {гъу} д {дж} {дз} е ё ж {жь} з и й к {ку} {кӏ} {кӏу} {къ} {къу} {кхъ} {кхъу} л {лъ} {лӏ} м н о п {пӏ} р с т {тӏ} у ф {фӏ} х {ху} {хь} {хъ} {хъу} ц {цӏ} ч ш щ {щӏ} ъ ы ь ю я ӏ {ӏу}

```

Sound values are not repeated here; `kbd-Cyrl-ipa` *(not yet published)* lists
the same 59 letters in the same order with their IPA values.

[§4](#tables) maps 58 of these letters. [§4.4](#excluded) explains which letter
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

| # | kbd | U+ | tr (kbd) | U+ | Notes |
|---|---|---|---|---|---|
| 1 | а | U+0430 | a | U+0061 |  |
| 2 | э | U+044D | e | U+0065 |  |
| 3 | б | U+0431 | b | U+0062 |  |
| 4 | в | U+0432 | v | U+0076 |  |
| 5 | г | U+0433 | g | U+0067 |  |
| 6 | гу | U+0433+U+0443 | gu | U+0067+U+0075 |  |
| 7 | гъ | U+0433+U+044A | ğ | U+011F |  |
| 8 | гъу | U+0433+U+044A+U+0443 | ğu | U+011F+U+0075 |  |
| 9 | д | U+0434 | d | U+0064 |  |
| 10 | дж | U+0434+U+0436 | c | U+0063 |  |
| 11 | дз | U+0434+U+0437 | dz | U+0064+U+007A |  |
| 12 | е | U+0435 | ê / yê | U+00EA / U+0079+U+00EA |  |
| 13 | ё | U+0451 | ö / yö | U+00F6 / U+0079+U+00F6 |  |
| 14 | ж | U+0436 | jj | U+006A+U+006A |  |
| 15 | жь | U+0436+U+044C | j | U+006A |  |
| 16 | з | U+0437 | z | U+007A |  |
| 17 | и | U+0438 | i / yi | U+0069 / U+0079+U+0069 |  |
| 18 | й | U+0439 | y | U+0079 |  |
| 19 | к | U+043A | k | U+006B |  |
| 20 | ку | U+043A+U+0443 | ku | U+006B+U+0075 |  |
| 21 | къ | U+043A+U+044A | kh | U+006B+U+0068 |  |
| 22 | къу | U+043A+U+044A+U+0443 | khu | U+006B+U+0068+U+0075 |  |
| 23 | кхъ | U+043A+U+0445+U+044A | kxh | U+006B+U+0078+U+0068 |  |
| 24 | кхъу | U+043A+U+0445+U+044A+U+0443 | kxhu | U+006B+U+0078+U+0068+U+0075 |  |
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
| 35 | р | U+0440 | r | U+0072 |  |
| 36 | с | U+0441 | s | U+0073 |  |
| 37 | т | U+0442 | t | U+0074 |  |
| 38 | тӏ | U+0442+U+04CF | t' | U+0074+U+0027 |  |
| 39 | у | U+0443 | u / vu | U+0075 / U+0076+U+0075 |  |
| 40 | ф | U+0444 | f | U+0066 |  |
| 41 | фӏ | U+0444+U+04CF | f' | U+0066+U+0027 |  |
| 42 | х | U+0445 | x | U+0078 |  |
| 43 | ху | U+0445+U+0443 | xu | U+0078+U+0075 |  |
| 44 | хъ | U+0445+U+044A | xh | U+0078+U+0068 |  |
| 45 | хъу | U+0445+U+044A+U+0443 | xhu | U+0078+U+0068+U+0075 |  |
| 46 | хь | U+0445+U+044C | h | U+0068 |  |
| 47 | ц | U+0446 | ts | U+0074+U+0073 |  |
| 48 | цӏ | U+0446+U+04CF | ts' | U+0074+U+0073+U+0027 |  |
| 49 | ч | U+0447 | ç | U+00E7 |  |
| 50 | ш | U+0448 | şş | U+015F+U+015F |  |
| 51 | щ | U+0449 | ş | U+015F |  |
| 52 | щӏ | U+0449+U+04CF | ş' | U+015F+U+0027 |  |
| 53 | ъ | U+044A | ∅ | — | see [note 4](#footnotes) |
| 54 | ы | U+044B | ı | U+0131 |  |
| 55 | ь | U+044C | ∅ | — | see [note 4](#footnotes) |
| 56 | ю | U+044E | ü / yü | U+00FC / U+0079+U+00FC |  |
| 57 | я | U+044F | ya | U+0079+U+0061 |  |
| 58 | ӏ | U+04CF | ' | U+0027 | palochka — never Latin `l`, `I` or digit `1` |

<a id="title-case"></a>

### 4.2 Title case

| # | kbd | U+ | tr (kbd) | U+ | Notes |
|---|---|---|---|---|---|
| 1 | А | U+0410 | A | U+0041 |  |
| 2 | Э | U+042D | E | U+0045 |  |
| 3 | Б | U+0411 | B | U+0042 |  |
| 4 | В | U+0412 | V | U+0056 |  |
| 5 | Г | U+0413 | G | U+0047 |  |
| 6 | Гу | U+0413+U+0443 | Gu | U+0047+U+0075 |  |
| 7 | Гъ | U+0413+U+044A | Ğ | U+011E |  |
| 8 | Гъу | U+0413+U+044A+U+0443 | Ğu | U+011E+U+0075 |  |
| 9 | Д | U+0414 | D | U+0044 |  |
| 10 | Дж | U+0414+U+0436 | C | U+0043 |  |
| 11 | Дз | U+0414+U+0437 | Dz | U+0044+U+007A |  |
| 12 | Е | U+0415 | Ê / Yê | U+00CA / U+0059+U+00EA |  |
| 13 | Ё | U+0401 | Ö / Yö | U+00D6 / U+0059+U+00F6 |  |
| 14 | Ж | U+0416 | Jj | U+004A+U+006A |  |
| 15 | Жь | U+0416+U+044C | J | U+004A |  |
| 16 | З | U+0417 | Z | U+005A |  |
| 17 | И | U+0418 | İ / Yi | U+0130 / U+0059+U+0069 |  |
| 18 | Й | U+0419 | Y | U+0059 |  |
| 19 | К | U+041A | K | U+004B |  |
| 20 | Ку | U+041A+U+0443 | Ku | U+004B+U+0075 |  |
| 21 | Къ | U+041A+U+044A | Kh | U+004B+U+0068 |  |
| 22 | Къу | U+041A+U+044A+U+0443 | Khu | U+004B+U+0068+U+0075 |  |
| 23 | Кхъ | U+041A+U+0445+U+044A | Kxh | U+004B+U+0078+U+0068 |  |
| 24 | Кхъу | U+041A+U+0445+U+044A+U+0443 | Kxhu | U+004B+U+0078+U+0068+U+0075 |  |
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
| 35 | Р | U+0420 | R | U+0052 |  |
| 36 | С | U+0421 | S | U+0053 |  |
| 37 | Т | U+0422 | T | U+0054 |  |
| 38 | Тӏ | U+0422+U+04CF | T' | U+0054+U+0027 |  |
| 39 | У | U+0423 | U / Vu | U+0055 / U+0056+U+0075 |  |
| 40 | Ф | U+0424 | F | U+0046 |  |
| 41 | Фӏ | U+0424+U+04CF | F' | U+0046+U+0027 |  |
| 42 | Х | U+0425 | X | U+0058 |  |
| 43 | Ху | U+0425+U+0443 | Xu | U+0058+U+0075 |  |
| 44 | Хъ | U+0425+U+044A | Xh | U+0058+U+0068 |  |
| 45 | Хъу | U+0425+U+044A+U+0443 | Xhu | U+0058+U+0068+U+0075 |  |
| 46 | Хь | U+0425+U+044C | H | U+0048 |  |
| 47 | Ц | U+0426 | Ts | U+0054+U+0073 |  |
| 48 | Цӏ | U+0426+U+04CF | Ts' | U+0054+U+0073+U+0027 |  |
| 49 | Ч | U+0427 | Ç | U+00C7 |  |
| 50 | Ш | U+0428 | Şş | U+015E+U+015F |  |
| 51 | Щ | U+0429 | Ş | U+015E |  |
| 52 | Щӏ | U+0429+U+04CF | Ş' | U+015E+U+0027 |  |
| 53 | Ъ | U+042A | ∅ | — |  |
| 54 | Ы | U+042B | I | U+0049 |  |
| 55 | Ь | U+042C | ∅ | — |  |
| 56 | Ю | U+042E | Ü / Yü | U+00DC / U+0059+U+00FC |  |
| 57 | Я | U+042F | Ya | U+0059+U+0061 |  |
| 58 | Ӏ | U+04C0 | ' | U+0027 |  |

<a id="upper-case"></a>

### 4.3 Upper case

| # | kbd | U+ | tr (kbd) | U+ | Notes |
|---|---|---|---|---|---|
| 1 | А | U+0410 | A | U+0041 |  |
| 2 | Э | U+042D | E | U+0045 |  |
| 3 | Б | U+0411 | B | U+0042 |  |
| 4 | В | U+0412 | V | U+0056 |  |
| 5 | Г | U+0413 | G | U+0047 |  |
| 6 | ГУ | U+0413+U+0423 | GU | U+0047+U+0055 |  |
| 7 | ГЪ | U+0413+U+042A | Ğ | U+011E |  |
| 8 | ГЪУ | U+0413+U+042A+U+0423 | ĞU | U+011E+U+0055 |  |
| 9 | Д | U+0414 | D | U+0044 |  |
| 10 | ДЖ | U+0414+U+0416 | C | U+0043 |  |
| 11 | ДЗ | U+0414+U+0417 | DZ | U+0044+U+005A |  |
| 12 | Е | U+0415 | Ê / YÊ | U+00CA / U+0059+U+00CA |  |
| 13 | Ё | U+0401 | Ö / YÖ | U+00D6 / U+0059+U+00D6 |  |
| 14 | Ж | U+0416 | JJ | U+004A+U+004A |  |
| 15 | ЖЬ | U+0416+U+042C | J | U+004A |  |
| 16 | З | U+0417 | Z | U+005A |  |
| 17 | И | U+0418 | İ / Yİ | U+0130 / U+0059+U+0130 |  |
| 18 | Й | U+0419 | Y | U+0059 |  |
| 19 | К | U+041A | K | U+004B |  |
| 20 | КУ | U+041A+U+0423 | KU | U+004B+U+0055 |  |
| 21 | КЪ | U+041A+U+042A | KH | U+004B+U+0048 |  |
| 22 | КЪУ | U+041A+U+042A+U+0423 | KHU | U+004B+U+0048+U+0055 |  |
| 23 | КХЪ | U+041A+U+0425+U+042A | KXH | U+004B+U+0058+U+0048 |  |
| 24 | КХЪУ | U+041A+U+0425+U+042A+U+0423 | KXHU | U+004B+U+0058+U+0048+U+0055 |  |
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
| 35 | Р | U+0420 | R | U+0052 |  |
| 36 | С | U+0421 | S | U+0053 |  |
| 37 | Т | U+0422 | T | U+0054 |  |
| 38 | ТӀ | U+0422+U+04C0 | T' | U+0054+U+0027 |  |
| 39 | У | U+0423 | U / VU | U+0055 / U+0056+U+0055 |  |
| 40 | Ф | U+0424 | F | U+0046 |  |
| 41 | ФӀ | U+0424+U+04C0 | F' | U+0046+U+0027 |  |
| 42 | Х | U+0425 | X | U+0058 |  |
| 43 | ХУ | U+0425+U+0423 | XU | U+0058+U+0055 |  |
| 44 | ХЪ | U+0425+U+042A | XH | U+0058+U+0048 |  |
| 45 | ХЪУ | U+0425+U+042A+U+0423 | XHU | U+0058+U+0048+U+0055 |  |
| 46 | ХЬ | U+0425+U+042C | H | U+0048 |  |
| 47 | Ц | U+0426 | TS | U+0054+U+0053 |  |
| 48 | ЦӀ | U+0426+U+04C0 | TS' | U+0054+U+0053+U+0027 |  |
| 49 | Ч | U+0427 | Ç | U+00C7 |  |
| 50 | Ш | U+0428 | ŞŞ | U+015E+U+015E |  |
| 51 | Щ | U+0429 | Ş | U+015E |  |
| 52 | ЩӀ | U+0429+U+04C0 | Ş' | U+015E+U+0027 |  |
| 53 | Ъ | U+042A | ∅ | — |  |
| 54 | Ы | U+042B | I | U+0049 |  |
| 55 | Ь | U+042C | ∅ | — |  |
| 56 | Ю | U+042E | Ü / YÜ | U+00DC / U+0059+U+00DC |  |
| 57 | Я | U+042F | YA | U+0059+U+0041 |  |
| 58 | Ӏ | U+04C0 | ' | U+0027 |  |

<a id="excluded"></a>

### 4.4 Deliberately excluded

Present in the alphabet but not carried into the conversion table, because
converting the parts separately covers every case in which they occur
together.<sup><a id="fnref3"></a>[3](#fn3)</sup>

| # | kbd | U+ | tr (kbd) | U+ | Notes |
|---|---|---|---|---|---|
| 59 | ӏу | U+04CF+U+0443 | 'u | U+0027+U+0075 | covered by `ӏ` + `у` |

<sub>[↑ contents](#contents)</sub>

<a id="auxiliary"></a>

## 5. Auxiliary exemplar

Letters that occur in real material but are not part of the official Kabardian
alphabet. **They are deliberately kept out of [§4](#tables)**, so the main
tables describe the standard alphabet only. Material containing these letters
cannot be converted by §4 alone.

For their sound values see `kbd-Cyrl-ipa` *(not yet published)*.

<a id="dialectal"></a>

### 5.1 Dialectal letters

| # | Letter | U+ | tr (kbd) | U+ | Dialect | Example |
|---|---|---|---|---|---|---|
| 1 | `{гь}` | U+0433+U+044C | `gg` | U+0067+U+0067 | some sub-dialects | гьанэ (ɟaːne) = джанэ *shirt / dress* |
| 2 | `{кь}` | U+043A+U+044C | `kk` | U+006B+U+006B | some sub-dialects | кьыржын (kʲərʒən) = чыржын *a corn-flour cookie* |
| 3 | `{кӏь}` | U+043A+U+04CF+U+044C | `kk'` | U+006B+U+006B+U+0027 | some sub-dialects | гьэдыкӏьэ (ɟedəkʲʼe) = джэдыкӏэ *egg* |

Title case and all caps follow the same pattern as the tables in [§4](#tables):

| Letter | Title case | All caps |
|---|---|---|
| `{гь}` → `gg` | `{Гь}` → `Gg` | `{ГЬ}` → `GG` |
| `{кь}` → `kk` | `{Кь}` → `Kk` | `{КЬ}` → `KK` |
| `{кӏь}` → `kk'` | `{Кӏь}` → `Kk'` | `{КӀЬ}` → `KK'` |

The doubled letter is the device the main tables already use, and the added
apostrophe marks glottalisation exactly as it does there. Compare `ж` → `jj` and
`ш` → `şş`.

Each of these letters ends in `ь`. Where `ь` follows `г`, `к` or `кӏ` it belongs
to one of these dialectal letters rather than standing alone, which is what
distinguishes the two cases in running
text.<sup><a id="fnref4"></a>[4](#fn4)</sup>

Order matters here as it does in [§2.5](#order): `кӏь` is three characters long
and must be converted before `кӏ` and before `к`, or it breaks apart. Longest
match first handles this without a special rule.

<a id="normalisation"></a>

### 5.2 Normalisation before use

Some material represents these dialectal sounds inconsistently. Applying the
following substitutions first resolves the inconsistency:

| Found | Replace with |
|---|---|
| `г'` | `гь` |
| `чӏ` | `кӏь` |

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
each Kabardian letter close to the sound that the corresponding Turkish letter
usually represents — that is, at the level of both grapheme and phoneme.
[↩](#fnref1)

<a id="fn2"></a>

**2.** A form written `ê / yê` is read as `yê` when it opens a word and as `ê`
anywhere else. [↩](#fnref2)

<a id="fn3"></a>

**3.** `ӏ` and `у` each convert on their own, and converting them separately is
expected to cover every case in which they occur together. [↩](#fnref3)

<a id="fn4"></a>

**4.** `ъ` and `ь` never occur on their own; they appear only as part of a
letter, together with another character, and therefore have no transliteration
of their own. If one is left standing alone after the other letters have been
converted, it is dropped. The palochka `ӏ` differs in this respect: there are
words in which it stands alone as a letter, at the beginning of a word or inside
it. [↩](#fnref4)

<sub>[↑ contents](#contents)</sub>

<a id="references"></a>

## References

- Topçu (Papşu), M. Transliteration proposal for the Circassian languages
  *(personal communication)*.
- Omniglot. *Kabardian language, alphabet and pronunciation.*
  <https://www.omniglot.com/writing/kabardian.htm> (accessed 2024-10-23)
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

> `kbd-Cyrl-tr-Latn-transliteration` · v1.0.0 · 2026-08-14 ·
> [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) ·
> part of [ady-kbd-language-resources](https://github.com/nemerko/ady-kbd-language-resources)
