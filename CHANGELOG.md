# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]

## [0.1.1] - 2025-08-25

### Added
- Added `aria-live="polite"` to `#points` label to improve accessibility for live updates.
- Displayed processor life on each card.
 - New grid layout and playful visual style for processor cards; 360px card width (user adjusted to 390px allowed).

### Changed
- Synced initial points display with `gameData.points` on load.
- Replaced automator with fuel tank model (fuel capacity, fuel consumption, add fuel action).
- Added Run/Pause toggle for processors; life depletes only when running.
- Added Repair action to restore life to max for a cost.
- Added Upgrade popup with Speed, Fuel Tank, and Life upgrades.
- Standardized units and labels to seconds (`s`) and `pt/sec` for clarity.
- Cleaned up any running processor interval on card removal to prevent hidden updates.

### Persistence
 - Implemented local save/load via localStorage; processors and points persist across sessions.

### UI
 - Simplified upgrade popup to three labeled buttons and added a close button; improved styling and ensured visibility.

### Fixed
- Corrected typo `conent` -> `content` when creating processor speed paragraph.
- Corrected inconsistent alert message about processor cost (now reflects `processorCost`).
- In `lib/JDom@0.2.js`:
  - Fixed JSDoc typos: `chilren` -> `children`.
  - Added null check in `render` and throw explicit error when selector not found.
  - Fixed `update` error logging (`error` -> `err`).
  - Fixed typo in error string: "assgined" -> "assigned".

### Notes
- External third-party widget is still loaded without SRI/CSP; consider adding a CSP and SRI in a future release.

