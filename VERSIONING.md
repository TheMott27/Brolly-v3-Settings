# Brolly v3 Settings — Versioning and Release Workflow

## Repository roles

This repository is the private testing stream for the Brolly v3 settings page. It is independent of the public 2.x settings repository and must be updated alongside the watchface when a configuration change is required.

## Version format

The settings page follows the Brolly v3 watchface version for each coordinated testing and public release.

| Stream | Repository visibility | Version rule | Example |
|---|---|---|---|
| Testing | Private | Increase the final integer by one for each testing push | `3.0.0` → `3.0.1` → `3.0.2` |
| Public release | Public, only after explicit user instruction | Increase the middle integer by one for each approved public release and reset the testing integer to `0` | `3.0.23` → `3.1.0`, then `3.1.8` → `3.2.0` |

## Branch and promotion rules

The initial private development branch is `Brolly-v3.0.0`. Each testing upload must use a version-named branch in the form `Brolly-v<version>` and must be pushed to the private settings testing repository. When a watchface change adds, removes, or changes a configurable setting, the settings-page counterpart must be updated and tested in the same version.

No content is to be pushed to a public v3 repository unless the user gives an explicit instruction to publish that specific version. A public release must be based on a tested private version, use the next public release number, and identify the private testing version from which it was promoted.
