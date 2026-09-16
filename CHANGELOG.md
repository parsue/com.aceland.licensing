# Changelog
All notable changes to this project will be documented in this file.

---
# Release - published

## [1.0.1] - 2026-09-16
### Fixed
- License window now reliably rebinds when opened for a different product. Previously, opening one product's License window and then another product's License menu did not switch the window content (a single shared window instance kept the first product's binding). The window now re-binds the incoming product handle, refreshes its title, and focuses / repaints on every open.
- As a side effect, this resolves the apparent "second product cannot start its trial" symptom: the window was still showing the first product's "trial in progress" state and hiding the Start Trial button. Per-product trial isolation (per-product machine-id salt, storage folder, and backend document) was already correct; only the shared window's stale binding was at fault.

## [1.0.0] - 2026-09-12
### Added
- Shared Editor-only licensing core for AceLand paid packages: offline signed-token verification, machine-id seat binding, backend verify / trial calls, and a reusable license window.
- Products register a `LicenseProductDescriptor` and consume a per-product `LicenseHandle`; each product is isolated by machine-id salt, storage folder, and backend trial document.
- Friendly degradation and fail-closed gate: unlicensed editors keep the runtime and builds fully functional and never gated; only development-time paid Editor tools are gated.
### Notes
- First stable release. Runtime and builds are never gated.
