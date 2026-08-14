# Changelog

Repository-level history: which files a release contains, and what changed
between releases. Per-file detail lives in the *Version history* section at the
end of each file — that is also the version a citation refers to. See
[README → Versioning](README.md#versioning).

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/);
versioning follows [Semantic Versioning](https://semver.org/) as applied to
data. Any entry that changes the result of processing carries the marker
⚠ **Affects output**, regardless of its version level.

---

## [1.0.0] — 2026-08-14

First release. Everything in it is new, so there is nothing to fix, change or
deprecate yet.

### Added

- Repository scaffolding: `README.md`, `LICENSE`, `CITATION.cff`, `CHANGELOG.md`.
- `files/ady-Cyrl-tr-Latn-transliteration.md` (1.0.0)
- `files/kbd-Cyrl-tr-Latn-transliteration.md` (1.0.0)
- `files/ady-Cyrl-tr-Latn-transliteration.json` (1.0.0)
- `files/kbd-Cyrl-tr-Latn-transliteration.json` (1.0.0)

---

<!--
Entry format — copy this shape for each release:

## [1.1.0] — YYYY-MM-DD

### Added
- `files/xxx.md` (1.1.0): new dialect column for Shapsug.

### Changed
- ⚠ **Affects output** — `files/xxx.md` (2.0.0): the IPA symbol set was replaced;
  material produced with 1.x should be regenerated.

### Fixed
- ⚠ **Affects output** — `files/xxx.md` (1.0.1): the `ӏ` row was written with
  U+04C0 (uppercase); corrected to U+04CF (lowercase).
- `files/xxx.md` (1.0.1): corrected a broken external audio link.

### Deprecated
- `files/yyy.md`: superseded by `files/zzz.md`; kept so existing citations resolve.
-->
