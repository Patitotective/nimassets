# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.3] - 2022-02-08

## Fixed

 - Fixed Issue #6 with `when defined(windows)` instead of using `distros.detectOs(Windows)`.

## Changed

 - Changed return type of `getAssetToByteSeq` from `string` to the correct `seq[byte]`

## Removed

 - Removed `distros` for `detectOs(Windows)` since it caused issues.

## [0.2.2] - 2021-12-04

### Added

- Add support for encoding asset to seq[byte]
- Add zstd compression
- Add zstd and base64 combined encoding (zstd -> byteArrayToString -> base64)

## [0.2.1] - 2021-07-28

### Changed

- Minor formatting. Removed trailing whitespace from generated assetfile.

### Added

- New testcase for the fast version of the bundler

## [0.2.0] - 2021-07-20

### Added

- This changelog
- The MIT LICENSE file that was mentioned in the .nimble file
- A simple test inside the tests directory
- Nimble tasks that will be executed before `nimble test` to generate the assetfile to be tested.

### Changed

- The generated assetfile now uses the `[]=` operator instead of `.add` for registering assets in the internal table since `.add` for tables has been deprecated since Nim 1.4
- Examples now live inside the `examples` directory
- The binary will now be built using the -d:release flag

## [0.1.0] - 2018

- Initial Release