# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Unreleased

## 3.1.1 - 2022-04-11

### Fixed

- Adding check to on-call relationship step to prevent potential error.

## 3.1.0 - 2022-04-07

### Changed

- We are now querying for what 'abilities' are enabled for the querying API key
  and disabling unsupported steps accordingly.
- Decoupled several steps from building relationships to prevent unnecessary
  disabling of steps due to a missing 'ability'.

## 3.0.2 - 2021-04-29

### Changed

- Fixed broken pagination in PagerDuty integration. Pagination expected a
  boolean response body property called `more`, but the property actually exists
  in the response body at `data.more`.

## 3.0.1 - 2021-04-27

### Changed

- Improved messaging for errors from `validateInvocation`.

## 3.0.0 - 2021-03-19

### Changed

- Migrated to latest integration SDK for improved error handling and reporting.

- Relationships
  - `User - ONCALL -> Service` has been changed to `User - MONITORS -> Service`.
    Relationships are best expressed as verbs, and `MONITORS` is the preferred
    verb in this type of relationship.

### Fixed

- A number of type check errors after upgrading TypeScript

## 2.2.0 - 2021-03-19

### Added

- New Properties
  - `User`: `id`, `type`, `email`, `role`, `jobTitle`, `timeZone`, `billed`,
    `description`, `invitationSent`, `webLink`

## [1.0.6]

### Added

- Checking for PagerDuty Admins

## [1.0.5]

### Fixes

- Services active flag always being set to false

## [1.0.4]

### Fixes

- Duplicate relationships between PagerDuty entities

## [1.0.2]

Initial Release
