# docvault
# DocVault

Self-hosted, cross-platform document & media organizer with local INT8 OCR and semantic vector search.

## Architecture
- `crates/core`: Rust core engine (`sqlite-vec`, `ort` ONNX Runtime, `UniFFI` bindings)
- `apps/macos`: Native SwiftUI client (baseline)
- `apps/windows`: Tauri v2 + React/TypeScript client (DirectML + CPU fallback)
- `apps/android`: Kotlin + Jetpack Compose client (`cargo-ndk` + NNAPI/GPU delegate)

## Upcoming Devin Bot Milestones
- [ ] Fix flaky DirectML fallback test on Windows CI
- [ ] Wire up UniFFI batch-search API in `apps/android`
- [ ] Maintain nightly cross-platform OCR golden snapshot regressions
