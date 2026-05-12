# Changelog

All notable changes to this skill will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this skill adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] — 2026-05-12

### Added
- **Profile Comparison** with concrete dimension-by-dimension contrasts and a side-by-side Quick Reference table, surfacing both where profiles differ most and where they're nearly identical
- **Per-Platform Sub-Variants** that inherit from a parent profile and override specific dimensions for platforms like LinkedIn, Twitter, or Instagram; stored as `[profile].[platform].md` alongside the parent
- **Drift Detection** that compares newly submitted samples against a saved profile and scores drift per dimension (Stable / Mild Drift / Significant Drift) with a recommendation to refresh
- Auto-prompting for drift checks when a profile hasn't been updated in 6+ months and new text scores divergently
- Four new Workflow Examples: comparing profiles, creating a sub-variant, running a drift check, and the existing rewrite flow updated to mention variants

### Changed
- Frontmatter now includes `version` and `metadata.openclaw.emoji` fields
- Core capabilities list expanded from 4 to 7 to reflect the new features
- Trigger description expanded to cover profile comparison, sub-variants, and drift-detection phrases

### Removed
- License section removed from README (license now managed at the ClawHub platform level)

## [1.0.0] — 2026-04-12

### Added
- Initial release
- Voice profile builder that analyzes 3-5 writing samples across sentence patterns, vocabulary signature, flow and structure, tone and personality, and punctuation/formatting habits
- AI Detection Scoring with category breakdowns (vocabulary, structure, tone, mechanics) and a 0-100 risk rating
- Rewriting engine that applies a saved voice profile to AI-generated text, preserving meaning while transforming surface mechanics
- Multi-profile management (list, switch, update, delete) in a local `profiles/` directory
- Quick Reference section in each profile to distill the most distinctive 8-10 traits
