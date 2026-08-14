# Adyghe & Kabardian Language Resources

Reference material for the Circassian languages **Adyghe (`ady`)** and **Kabardian (`kbd`)**:
transliteration tables and related documentation, published as plain, citable
Markdown files. IPA correspondence tables are in preparation for release 1.1.0.

The material here is released under **CC BY 4.0** — it may be reused, adapted and built upon
by anyone, provided attribution is given. It is deliberately kept separate from the software
that consumes it, so that the language data itself carries no usage restrictions.

---

## Contents

| File | Type | Version | Status | Description |
|---|---|---|---|---|
| [`ady-Cyrl-tr-Latn-transliteration`](files/ady-Cyrl-tr-Latn-transliteration.md) | transliteration table | 1.0.0 | stable | Adyghe Cyrillic ↔ Turkish Latin |
| [`kbd-Cyrl-tr-Latn-transliteration`](files/kbd-Cyrl-tr-Latn-transliteration.md) | transliteration table | 1.0.0 | stable | Kabardian Cyrillic ↔ Turkish Latin |
| [`ady-Cyrl-tr-Latn-transliteration.json`](files/ady-Cyrl-tr-Latn-transliteration.json) | machine-readable | 1.0.0 | stable | The Adyghe table as data |
| [`kbd-Cyrl-tr-Latn-transliteration.json`](files/kbd-Cyrl-tr-Latn-transliteration.json) | machine-readable | 1.0.0 | stable | The Kabardian table as data |
| `ady-Cyrl-ipa` | IPA table | — | planned 1.1.0 | Sound value of each Adyghe letter |
| `kbd-Cyrl-ipa` | IPA table | — | planned 1.1.0 | Sound value of each Kabardian letter |

*(Version and status are taken from the front matter of each file at release time.)*

Planned files are listed before they exist, for the same reason pending rows are
kept inside the tables: a gap that is visible can be cited and tracked, a gap
that is hidden cannot. A released version is never modified, so files announced
here arrive in the next release rather than being added to this one.

---

## Scope

These resources describe **written correspondences**, not prescriptive orthographic reform.
Where a mapping is contested or varies by dialect, the table documents the variation instead
of silently choosing one form.

The transliteration tables were designed for a practical purpose: enabling Circassian speakers
in the diaspora who read Latin script but not Cyrillic to participate in corpus work. They are
phoneme-oriented and, unless a file states otherwise, **reversible** — every Latin form maps
back to exactly one Cyrillic form.

Each file is prepared by the author and reviewed before release. Who reviewed it, and in what
scope, is recorded in that file's own `reviewers` field: the specialists differ from one file
to the next, because the expertise a table needs depends on what the table describes.

---

## Conventions that apply to every file

### Palochka

Adyghe and Kabardian orthographies use the **palochka**:

| Character | Codepoint | Name |
|---|---|---|
| `Ӏ` | U+04C0 | Cyrillic Letter Palochka (uppercase) |
| `ӏ` | U+04CF | Cyrillic Small Letter Palochka (lowercase) |

Because the palochka is absent from the standard Russian keyboard layout, it is very commonly
replaced by visually similar characters. **These substitutions are errors and must not appear
in the data:**

| Wrong | Codepoint | What it actually is |
|---|---|---|
| `I` | U+0049 | Latin Capital Letter I |
| `l` | U+006C | Latin Small Letter L |
| `1` | U+0031 | Digit One |
| `І` | U+0406 | Cyrillic Capital Letter Byelorussian-Ukrainian I |
| `і` | U+0456 | Cyrillic Small Letter Byelorussian-Ukrainian I |

Every character in these files is given together with its Unicode codepoint precisely so that
this class of confusion cannot survive a copy-paste.

### Encoding

All files are **UTF-8**, LF line endings, no BOM.

---

## How to cite

Each file carries a `cite-as` field in its front matter. Cite the individual file when you use
a specific table, and the repository when you refer to the collection as a whole.

A `CITATION.cff` file is provided; GitHub renders it as a **“Cite this repository”** button.

When a release is archived, cite the version you actually used — mappings can change between
versions, and results are not comparable across a major version boundary.

---

## Versioning

Two levels are used.

**File version** — each file in `files/` carries its own `version` in the front matter, and its
own history in the *Version history* section at the end of the file. This is the version you
cite.

**Release version** — a release freezes a particular combination of file versions and is what
gets archived. Its number reflects the most severe change since the previous release.

Both follow [Semantic Versioning](https://semver.org/), applied to data as follows:

| Level | Meaning | Examples |
|---|---|---|
| **MAJOR** | An existing entry changed or was removed. Output produced with the previous version is no longer reproducible. | An IPA symbol set is replaced; a variant code is renamed; a row is deleted |
| **MINOR** | Something new was added; nothing existing was touched. | A dialect is added to a table; audio links are added where there were none; a new file joins the repository |
| **PATCH** | No mapping was touched. | Wording, formatting, a corrected typo in a description, a fixed external link |

### The “Affects output” rule

Correcting a genuine error in the data — a character written with the wrong codepoint, a row in
the wrong column — is recorded as a **PATCH**, because the previous value was never the intended
content. But such a correction still changes what anyone reprocessing their material will get.

Therefore any change that alters the result of processing, **at any level**, must be marked in
both the changelog and the file's version history:

```markdown
- ⚠ **Affects output** — the `ӏ` row was written with U+04C0 (uppercase);
  corrected to U+04CF (lowercase). Material produced with v1.0.0 should be
  regenerated.
```

If a change alters output and is *not* marked this way, it must be released as MAJOR instead.
The marker exists so that no output-changing correction can pass unnoticed.

---

## Stability and permanence

These files are meant to be referenced by other work — research, tooling and language
planning projects. That is only useful if the references keep resolving, so the following
hold:

- **Identifiers are permanent.** The `id` of a file never changes and is never reused for
  different content.
- **Files are not deleted.** A resource that is superseded is marked `status: deprecated`,
  keeps its content, and points to whatever replaces it. Existing citations stay valid.
- **Paths are not rearranged** without leaving the old path in place.
- **Released versions are immutable.** Corrections produce a new version; they never rewrite
  a version that has already been released.
- **Incomplete entries are shown, not hidden.** Where a mapping has not been established yet,
  the row is present and marked *(pending)* rather than omitted, so that the gap can itself be
  cited and tracked.

What may change is content in `draft` status, and anything the version history announces.

---

## File standard

Every file in `files/` follows the same shape. A blank template is being prepared together
with the IPA tables for release 1.1.0; until then, start from an existing file.

A file is laid out like a small book:

| Part | Contents |
|---|---|
| **Front matter** | YAML block: identity, version, subject, people, provenance, licence, citation. This is the **normative** record. |
| **Cover** | The same information rendered for a human reader, inside a quoted block so that it is framed in any Markdown viewer. Derived from the front matter. |
| **Table of contents** | |
| **Body** | Scope → Conventions → Content → Notes and limitations |
| **Footnotes** | |
| **References** | |
| **Footer** | Version history for this file, then a one-line imprint. |

Two sections are mandatory for anything that defines a mapping:

- **Conventions → Codepoints.** Every character appears with its Unicode codepoint, and the
  codepoints are generated from the characters rather than typed by hand.
- **Conventions → Directionality and apparent collisions.** Whether the mapping is intended to
  work in both directions, whether that has been verified, every reading that is not
  one-to-one, and the rule that resolves it. Collisions are derived from the data, not listed
  by hand.

### Identifiers

The filename and the `id` are a **human-readable compound label, not a language tag.**
`ady-Cyrl-tr-Latn-transliteration` sets two tags side by side and adds a description of what the
file is. Read as a single BCP 47 tag it would not even be well-formed — and its first three
segments, `ady-Cyrl-tr`, *are* well-formed but mean “Adyghe, Cyrillic script, region Turkey”,
which is not what the file describes. Names are chosen to be legible in a directory listing;
they are not meant to be parsed.

The machine-readable identifier is the `transform` field, using
[BCP 47 Extension T (RFC 6497)](https://www.rfc-editor.org/rfc/rfc6497), the standard for
transformed content:

```yaml
transform: tr-Latn-t-ady-Cyrl          # Turkish Latin, transformed from Adyghe Cyrillic
reverse-transform: ady-Cyrl-t-tr-Latn
```

Every file that defines a transformation carries this field, and it is repeated on the cover so
a reader can see it without reading the front matter. **Software should key on `transform`, never
on the filename** — including the machine-readable siblings of these tables.

One thing worth knowing when reading such tags: BCP 47 is **case-insensitive**. The familiar
convention — lowercase language, Titlecase script, UPPERCASE region — is a writing habit that
carries no meaning. What decides whether `tr` means the Turkish language or the region Turkey is
its **position**, not its case.

### Footnotes

Footnotes are written out explicitly — a `<a id="fnN">` anchor, a numbered paragraph and a link
back — rather than with the `[^1]` shorthand. The shorthand is not part of CommonMark: renderers
that support it move the definitions to the end of the document, and renderers that do not
support it print `[^1]` in the middle of the sentence. Writing them out keeps the footnotes
under their own heading, above the references, and readable in every viewer including a plain
text editor.

This follows the same reasoning as the explicit `<a id="...">` anchors used for section links:
where a convenience feature renders differently across viewers, the file spells it out instead.

Repository-wide history lives in [`CHANGELOG.md`](CHANGELOG.md); each file additionally carries
its own history in its footer.

---

## Languages and translations

Files are written in **English**, which is the normative version. Translations are added
beside the original, distinguished by a language tag in the filename:

```
ady-Cyrl-tr-Latn-transliteration.md          ← English, normative
ady-Cyrl-tr-Latn-transliteration.tr.md       ← Turkish
ady-Cyrl-tr-Latn-transliteration.ady.md      ← Adyghe
ady-Cyrl-tr-Latn-transliteration.ru.md       ← Russian
```

The suffix — and only the suffix — is a [BCP 47](https://www.rfc-editor.org/info/bcp47)
language tag, naming the language the prose is written in. The stem before it is a compound
label; see [Identifiers](#identifiers) above. Use the shortest tag that
identifies the language (`tr`, not `tr-TR`), and add a subtag only when it distinguishes
something real (`ady-Cyrl` versus `ady-Latn`).

Two rules keep translations trustworthy:

1. **Only prose is translated.** Tables, codepoints and mappings are identical in every
   language version. A translation that changes data is a defect, not a translation.
2. **Every translation records what it was translated from**, using these front matter fields:

   ```yaml
   translation-of: ady-Cyrl-tr-Latn-transliteration
   translated-from-version: 1.2.0
   ```

   If the source file has moved on since that version, the translation is out of date and
   should say so in its `status`.

Translation contributions are welcome. Open a pull request with the new file; there is no need
to ask first.

---

## Licence

[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)

You may share and adapt this material for any purpose, including commercially, as long as you
give appropriate credit, provide a link to the licence, and indicate if changes were made.

---

## Related

- [TXT File Creator & Validator for MCV (ady, kbd)](https://github.com/nemerko/TXTFile-CV4MCV-ady-kbd) —
  the Excel/VBA tool that uses these tables. The tool is released under a separate,
  more restrictive licence; the language data in this repository is not.
