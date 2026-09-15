---
# ─── identity ───────────────────────────────────────────────
id: kbd-Cyrl-alphabet
title: "Kabardian (kbd) Cyrillic Alphabet"
type: alphabet                       # alphabet | transliteration-table | ipa-table | guide
version: 1.0.0
status: stable                       # draft | stable | deprecated
updated: 2026-09-15

# ─── subject ────────────────────────────────────────────────
languages: [kbd]                        # ISO 639-2
scripts: [Cyrl]                      # ISO 15924

# ─── people ─────────────────────────────────────────────────
authors:
  - name: M. Uğur Nemlioğlu
    orcid: 0000-0002-1969-2356
reviewers:
  - name: Murat Topçu
    scope: letter forms and alphabetical order

# ─── provenance and use ─────────────────────────────────────
based-on: >
  Unicode CLDR main and auxiliary exemplar sets for kbd, prepared and
  maintained by the author in the CLDR Survey Tool. The letter forms and the
  alphabetical order were confirmed by the reviewer named above before
  submission to Unicode.
license: CC-BY-4.0
summary: >
  The letters of the Kabardian Cyrillic alphabet in alphabetical order, with their
  lower-, title- and upper-case forms, together with the auxiliary letters used
  for dialectal sounds that are not part of the official alphabet.
cite-as: >
  Nemlioğlu, M. U. (2026). Kabardian (kbd) Cyrillic Alphabet (Version 1.0.0)
  [Data set]. ady-kbd-language-resources.
  https://github.com/nemerko/ady-kbd-language-resources
machine-readable: kbd-Cyrl-alphabet.json
related:
  - ady-Cyrl-alphabet
  - kbd-Cyrl-tr-Latn-transliteration
  - kbd-Cyrl-ipa
---

<!-- ══════════════════════════ COVER ══════════════════════════
     Rendered from the front matter above, which is the normative
     source. If you change a field, update this block to match.
     ═══════════════════════════════════════════════════════════ -->

> # Kabardian (kbd) Cyrillic Alphabet
>
> *The letters of the Kabardian Cyrillic alphabet in alphabetical order, with their
> lower-, title- and upper-case forms, together with the auxiliary letters used
> for dialectal sounds that are not part of the official alphabet.*
>
> | | |
> |---|---|
> | **Identifier** | `kbd-Cyrl-alphabet` |
> | **Type** | Alphabet |
> | **Version** | 1.0.0 — 2026-09-15 |
> | **Status** | Stable |
> | **Language** | Kabardian (`kbd`) |
> | **Script** | Cyrillic (`Cyrl`) |
> | **Letters** | 59 in the main exemplar, 3 auxiliary |
> | **Author** | M. Uğur Nemlioğlu ([ORCID](https://orcid.org/0000-0002-1969-2356)) |
> | **Reviewer** | Murat Topçu — letter forms and alphabetical order |
> | **Licence** | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
>
> **Cite as —** Nemlioğlu, M. U. (2026). *Kabardian (kbd) Cyrillic Alphabet*
> (Version 1.0.0) [Data set]. ady-kbd-language-resources.

---

## Table of contents

- [1. Scope](#1-scope)
- [2. Conventions](#2-conventions)
  - [2.1 Notation](#21-notation)
  - [2.2 Codepoints](#22-codepoints)
  - [2.3 Case and ambiguity](#23-case-and-ambiguity)
  - [2.4 Two different orders](#24-two-different-orders)
- [3. Exemplar](#3-exemplar)
- [4. Table](#4-table)
- [5. Auxiliary exemplar](#5-auxiliary-exemplar)
  - [5.1 Dialectal letters](#51-dialectal-letters)
- [6. Notes and limitations](#6-notes-and-limitations)
- [Footnotes](#footnotes)
- [References](#references)
- [Version history](#version-history)

---

## 1. Scope

This file records two things: **which letters belong to the Kabardian Cyrillic
alphabet**, and **in what order they are conventionally arranged**. For every
letter it gives the lower-, title- and upper-case form and the Unicode
codepoints of each.

It deliberately does not give sound values — those belong to
`kbd-Cyrl-ipa` *(not yet published)* — and it does not map the letters onto any
other writing system; that is the work of the transliteration tables. The
alphabet is the **source object** from which those files are derived, and it is
published separately so that each of them can be shaped by its own use.

A consequence worth stating plainly, because it is easy to get wrong: **the
order of rows in another file of this repository is not a statement about the
alphabet.** A transliteration table arranges its rows so that the reader can
follow the mapping and compare related languages; an IPA table arranges its
rows by what it is describing. Each order is chosen for that file's purpose.
The alphabetical order of Kabardian is the one recorded here, and only here.

This file describes written usage. It is not a proposal for orthographic
reform and it does not prescribe how the language should be written.

## 2. Conventions

### 2.1 Notation

| Symbol | Meaning |
|---|---|
| `{…}` | a multigraph: two or more characters that behave as one letter (`{кӏу}`) |
| `+` | joins the codepoints of a multigraph (`U+043A+U+04CF`) |
| `—` | not applicable |

The exemplar sets in [§3](#3-exemplar) use Unicode CLDR exemplar notation: a
space separates letters, and braces group the characters of a multi-character
letter.

### 2.2 Codepoints

Every character is given with its Unicode codepoint. This is not decoration: it
is how a reader tells the palochka `ӏ` (U+04CF) apart from the Latin `l`
(U+006C) that is routinely typed in its place. See the repository
[README](../README.md#palochka) for the full list of look-alikes.

**Codepoints in this file are generated from the characters themselves, not
typed by hand.** A mismatch between a glyph and its stated codepoint is a defect;
please report it.

### 2.3 Case and ambiguity

An alphabet has no direction, so the question that a transliteration table
answers under this heading — which mappings are not one-to-one — does not
arise here. Two other ambiguities do, and both are resolved by recording the
forms explicitly rather than leaving them to be computed.

**Title case and upper case are different strings for multigraphs.** In `{кӏ}`
the title form raises only the first character, giving `{Кӏ}`, while the upper
form raises both, giving `{КӀ}`. A consumer that derives one from the other at
run time will produce one of them wrongly, and the error is hard to see because
the two differ by a single glyph. [§4](#4-table) therefore lists all three forms
side by side.

**Case conversion must not depend on the runtime locale.** In Turkish locales
the Latin `I` lower-cases to `ı` rather than `i`; software that applies a
locale-sensitive case operation while looking for palochka look-alikes will
silently mis-handle exactly the character this file exists to protect. Compare
and convert with invariant or ordinal semantics.

### 2.4 Two different orders

This file carries two orders and they are not the same.

**Alphabetical order** is the one in [§4](#4-table), given by the index column.
It is the conventional order of the alphabet and it must not be recomputed by
sorting on codepoints: `ё` is U+0451 and sorting by codepoint would move it past
`я` to the end of the list.

**Matching order** is what software needs when it identifies letters in running
text. Because several letters are multigraphs, matching proceeds from the
longest sequence to the shortest: a `{кӏь}` found before `{кӏ}` and before `к`
stays intact, whereas the reverse order breaks it apart. The array in the
machine-readable file is in alphabetical order and must be re-sorted by length
before it is applied.

## 3. Exemplar

**Main exemplar** — 59 letters:

```
а э б в г {гу} {гъ} {гъу} д {дж} {дз} е ё ж {жь} з и й к {ку} {кӏ} {кӏу} {къ} {къу} {кхъ} {кхъу} л {лъ} {лӏ} м н о п {пӏ} р с т {тӏ} у ф {фӏ} х {ху} {хь} {хъ} {хъу} ц {цӏ} ч ш щ {щӏ} ъ ы ь ю я ӏ {ӏу}
```

**Auxiliary exemplar** — 3 letters:

```
{гь} {кь} {кӏь}
```

The letters above are built from **34 distinct characters**. In alphabetical
order these are:

```
аэбвгдеёжзийклмнопрстуфхцчшщъыьюяӏ
АЭБВГДЕЁЖЗИЙКЛМНОПРСТУФХЦЧШЩЪЫЬЮЯӀ
```

This character inventory is what a validator needs in order to answer whether a
single character belongs to the alphabet. The letter inventory in
[§4](#4-table) is what everything else needs.

## 4. Table

| # | Letter | U+ | Title | U+ | Upper | U+ | Type |
|---|---|---|---|---|---|---|---|
| 1 | `а` | U+0430 | `А` | U+0410 | `А` | U+0410 | single |
| 2 | `э` | U+044D | `Э` | U+042D | `Э` | U+042D | single |
| 3 | `б` | U+0431 | `Б` | U+0411 | `Б` | U+0411 | single |
| 4 | `в` | U+0432 | `В` | U+0412 | `В` | U+0412 | single |
| 5 | `г` | U+0433 | `Г` | U+0413 | `Г` | U+0413 | single |
| 6 | `{гу}` | U+0433+U+0443 | `Гу` | U+0413+U+0443 | `ГУ` | U+0413+U+0423 | digraph |
| 7 | `{гъ}` | U+0433+U+044A | `Гъ` | U+0413+U+044A | `ГЪ` | U+0413+U+042A | digraph |
| 8 | `{гъу}` | U+0433+U+044A+U+0443 | `Гъу` | U+0413+U+044A+U+0443 | `ГЪУ` | U+0413+U+042A+U+0423 | trigraph |
| 9 | `д` | U+0434 | `Д` | U+0414 | `Д` | U+0414 | single |
| 10 | `{дж}` | U+0434+U+0436 | `Дж` | U+0414+U+0436 | `ДЖ` | U+0414+U+0416 | digraph |
| 11 | `{дз}` | U+0434+U+0437 | `Дз` | U+0414+U+0437 | `ДЗ` | U+0414+U+0417 | digraph |
| 12 | `е` | U+0435 | `Е` | U+0415 | `Е` | U+0415 | single |
| 13 | `ё` | U+0451 | `Ё` | U+0401 | `Ё` | U+0401 | single |
| 14 | `ж` | U+0436 | `Ж` | U+0416 | `Ж` | U+0416 | single |
| 15 | `{жь}` | U+0436+U+044C | `Жь` | U+0416+U+044C | `ЖЬ` | U+0416+U+042C | digraph |
| 16 | `з` | U+0437 | `З` | U+0417 | `З` | U+0417 | single |
| 17 | `и` | U+0438 | `И` | U+0418 | `И` | U+0418 | single |
| 18 | `й` | U+0439 | `Й` | U+0419 | `Й` | U+0419 | single |
| 19 | `к` | U+043A | `К` | U+041A | `К` | U+041A | single |
| 20 | `{ку}` | U+043A+U+0443 | `Ку` | U+041A+U+0443 | `КУ` | U+041A+U+0423 | digraph |
| 21 | `{кӏ}` | U+043A+U+04CF | `Кӏ` | U+041A+U+04CF | `КӀ` | U+041A+U+04C0 | digraph |
| 22 | `{кӏу}` | U+043A+U+04CF+U+0443 | `Кӏу` | U+041A+U+04CF+U+0443 | `КӀУ` | U+041A+U+04C0+U+0423 | trigraph |
| 23 | `{къ}` | U+043A+U+044A | `Къ` | U+041A+U+044A | `КЪ` | U+041A+U+042A | digraph |
| 24 | `{къу}` | U+043A+U+044A+U+0443 | `Къу` | U+041A+U+044A+U+0443 | `КЪУ` | U+041A+U+042A+U+0423 | trigraph |
| 25 | `{кхъ}` | U+043A+U+0445+U+044A | `Кхъ` | U+041A+U+0445+U+044A | `КХЪ` | U+041A+U+0425+U+042A | trigraph |
| 26 | `{кхъу}` | U+043A+U+0445+U+044A+U+0443 | `Кхъу` | U+041A+U+0445+U+044A+U+0443 | `КХЪУ` | U+041A+U+0425+U+042A+U+0423 | tetragraph |
| 27 | `л` | U+043B | `Л` | U+041B | `Л` | U+041B | single |
| 28 | `{лъ}` | U+043B+U+044A | `Лъ` | U+041B+U+044A | `ЛЪ` | U+041B+U+042A | digraph |
| 29 | `{лӏ}` | U+043B+U+04CF | `Лӏ` | U+041B+U+04CF | `ЛӀ` | U+041B+U+04C0 | digraph |
| 30 | `м` | U+043C | `М` | U+041C | `М` | U+041C | single |
| 31 | `н` | U+043D | `Н` | U+041D | `Н` | U+041D | single |
| 32 | `о` | U+043E | `О` | U+041E | `О` | U+041E | single |
| 33 | `п` | U+043F | `П` | U+041F | `П` | U+041F | single |
| 34 | `{пӏ}` | U+043F+U+04CF | `Пӏ` | U+041F+U+04CF | `ПӀ` | U+041F+U+04C0 | digraph |
| 35 | `р` | U+0440 | `Р` | U+0420 | `Р` | U+0420 | single |
| 36 | `с` | U+0441 | `С` | U+0421 | `С` | U+0421 | single |
| 37 | `т` | U+0442 | `Т` | U+0422 | `Т` | U+0422 | single |
| 38 | `{тӏ}` | U+0442+U+04CF | `Тӏ` | U+0422+U+04CF | `ТӀ` | U+0422+U+04C0 | digraph |
| 39 | `у` | U+0443 | `У` | U+0423 | `У` | U+0423 | single |
| 40 | `ф` | U+0444 | `Ф` | U+0424 | `Ф` | U+0424 | single |
| 41 | `{фӏ}` | U+0444+U+04CF | `Фӏ` | U+0424+U+04CF | `ФӀ` | U+0424+U+04C0 | digraph |
| 42 | `х` | U+0445 | `Х` | U+0425 | `Х` | U+0425 | single |
| 43 | `{ху}` | U+0445+U+0443 | `Ху` | U+0425+U+0443 | `ХУ` | U+0425+U+0423 | digraph |
| 44 | `{хь}` | U+0445+U+044C | `Хь` | U+0425+U+044C | `ХЬ` | U+0425+U+042C | digraph |
| 45 | `{хъ}` | U+0445+U+044A | `Хъ` | U+0425+U+044A | `ХЪ` | U+0425+U+042A | digraph |
| 46 | `{хъу}` | U+0445+U+044A+U+0443 | `Хъу` | U+0425+U+044A+U+0443 | `ХЪУ` | U+0425+U+042A+U+0423 | trigraph |
| 47 | `ц` | U+0446 | `Ц` | U+0426 | `Ц` | U+0426 | single |
| 48 | `{цӏ}` | U+0446+U+04CF | `Цӏ` | U+0426+U+04CF | `ЦӀ` | U+0426+U+04C0 | digraph |
| 49 | `ч` | U+0447 | `Ч` | U+0427 | `Ч` | U+0427 | single |
| 50 | `ш` | U+0448 | `Ш` | U+0428 | `Ш` | U+0428 | single |
| 51 | `щ` | U+0449 | `Щ` | U+0429 | `Щ` | U+0429 | single |
| 52 | `{щӏ}` | U+0449+U+04CF | `Щӏ` | U+0429+U+04CF | `ЩӀ` | U+0429+U+04C0 | digraph |
| 53 | `ъ` | U+044A | `Ъ` | U+042A | `Ъ` | U+042A | single |
| 54 | `ы` | U+044B | `Ы` | U+042B | `Ы` | U+042B | single |
| 55 | `ь` | U+044C | `Ь` | U+042C | `Ь` | U+042C | single |
| 56 | `ю` | U+044E | `Ю` | U+042E | `Ю` | U+042E | single |
| 57 | `я` | U+044F | `Я` | U+042F | `Я` | U+042F | single |
| 58 | `ӏ` | U+04CF | `Ӏ` | U+04C0 | `Ӏ` | U+04C0 | single |
| 59 | `{ӏу}` | U+04CF+U+0443 | `Ӏу` | U+04C0+U+0443 | `ӀУ` | U+04C0+U+0423 | digraph |

## 5. Auxiliary exemplar

Letters that occur in real material but are not part of the official Kabardian
alphabet. **They are deliberately kept out of [§4](#4-table)**, so the main
table describes the standard alphabet only. They carry no position in the
alphabetical order.

For their sound values see `kbd-Cyrl-ipa` *(not yet published)*.

### 5.1 Dialectal letters

| # | Letter | U+ | Title | U+ | Upper | U+ | Dialect |
|---|---|---|---|---|---|---|---|
| 1 | `{гь}` | U+0433+U+044C | `Гь` | U+0413+U+044C | `ГЬ` | U+0413+U+042C | some sub-dialects |
| 2 | `{кь}` | U+043A+U+044C | `Кь` | U+041A+U+044C | `КЬ` | U+041A+U+042C | some sub-dialects |
| 3 | `{кӏь}` | U+043A+U+04CF+U+044C | `Кӏь` | U+041A+U+04CF+U+044C | `КӀЬ` | U+041A+U+04C0+U+042C | some sub-dialects |

## 6. Notes and limitations

The main exemplar records the official alphabet as it is taught and printed. It
is an inventory of letters, not of sounds: where one letter stands for more than
one sound, or where dialects differ in how a letter is pronounced, that variation
is described in the IPA file rather than here.

The auxiliary exemplar is not a closed list. It records the dialectal letters
that are established in written use; other dialectal sounds are written with the
letters of the main alphabet and so leave no separate trace here.

Collation beyond the plain letter order — how strings compare when they differ
in case, or how multigraphs are weighted against their component letters — is
not defined by this file.

---

## Footnotes

This version has no footnotes.

## References

Unicode CLDR, exemplar characters for `kbd`. Prepared and maintained by the
author in the CLDR Survey Tool.

---

<!-- ══════════════════════════ FOOTER ═════════════════════════ -->

## Version history

Changes to **this file only**. Repository-wide history is in
[`CHANGELOG.md`](../CHANGELOG.md). Any change that alters the result of
processing is marked ⚠ **Affects output**, whatever its version level.

### 1.0.0 — 2026-09-15

- Initial release.

---

> `kbd-Cyrl-alphabet` · v1.0.0 · 2026-09-15 ·
> [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) ·
> part of [ady-kbd-language-resources](https://github.com/nemerko/ady-kbd-language-resources)
