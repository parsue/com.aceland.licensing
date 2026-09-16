# AceLand Licensing

Editor-only licensing core used by **AceLand paid packages**.

> This package is a shared dependency for AceLand's paid Editor tooling. It is not a
> general-purpose utility and exposes no public usage API of its own. **Install it only
> when a paid AceLand package asks for it** (the dependent package will guide you).

## What it is

A single precompiled, obfuscated Editor assembly that AceLand paid packages link
against to perform their license checks. It runs only in the Unity Editor.

- **Runtime and player builds are never gated.** Shipped games and their builds run
  without any license check.
- **No manual setup.** There is nothing to configure or call by hand. The paid package
  that depends on it drives everything.

## Do I need to install this?

- **No** — if you don't use any AceLand paid package.
- **Only when prompted** — a paid AceLand package that needs it will request the
  install. In that case add it through the paid package's guidance / dependency.

## Compatibility

- Unity **2022.3 LTS** and newer (through the latest LTS).
- Editor-only, `netstandard2.1`, no external dependencies.

## License

© AceLand Workshop — Parsue. All rights reserved.
