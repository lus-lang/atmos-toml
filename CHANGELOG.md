# Changelog

## 1.0.0

**Release date:** TBD

Version 1.0.0 is the first release of `toml`, which reads and writes TOML 1.0 with offset date times as values of the `time` module.

- Added `toml.decode`, `toml.encode`, `toml.localtime`, and `toml.iserror`.
  - `toml.decode`: Parses a TOML document into a table.
  - `toml.encode`: Writes a table as a TOML document.
  - `toml.localtime`: Returns a local date, time, or date and time.
  - `toml.iserror`: Tests whether a value is an error object that `toml.decode` raised.
