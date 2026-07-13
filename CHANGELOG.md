# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.14.0] - 2026-07-13

### Added

- Initial unified versioning across Chrome, Firefox, and Tampermonkey builds.

### Changed

- Aligned version numbers across all three targets (previously out of sync).

### Fixed

- Resolved an issue where the toolbar did not appear on Goodreads book pages using locale-prefixed URLs (e.g., `/en/book/show/...`, `/de/book/show/...`). Added additional `@match` patterns to cover these paths.

[Unreleased]: https://github.com/Cyperaceae/good2dou/compare/v1.14.0...HEAD
[1.14.0]: https://github.com/Cyperaceae/good2dou/releases/tag/v1.14.0
