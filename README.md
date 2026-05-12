# Voice Match Humanizer

An OpenClaw skill that clones your writing voice from samples and applies it to any text.

Unlike generic humanizers that strip AI patterns and call it a day, this skill learns *your* specific writing fingerprint (sentence structure, vocabulary, tone, quirks) and uses it to transform AI-generated text so it sounds like you actually wrote it.

**Current version: 1.1.0**

## What's new in 1.1.0

- **Profile Comparison**: side-by-side diff of two saved profiles with a contrast table, so you can spot redundant profiles or pick the right one for a given piece
- **Per-Platform Sub-Variants**: keep a core voice and create platform-specific overrides (e.g., `blog-voice.linkedin.md` tightens for LinkedIn while inheriting the parent's vocabulary signature)
- **Drift Detection**: compares new samples against a saved profile and flags meaningful shifts so you know when to refresh

See [CHANGELOG.md](CHANGELOG.md) for the full release history.

## What it does

- **Build voice profiles** from your writing samples (blog posts, emails, LinkedIn posts, newsletters)
- **Score text** for AI detection risk with a detailed breakdown across vocabulary, structure, tone, and mechanics
- **Rewrite AI-generated text** to match a saved voice profile
- **Manage multiple named profiles** for different contexts ("blog-voice," "linkedin-voice," "email-voice")
- **Compare profiles** to see how two voices differ (1.1.0)
- **Per-platform sub-variants** that inherit a parent voice and adapt for specific platforms (1.1.0)
- **Drift detection** that alerts when new writing has shifted away from a saved profile (1.1.0)

## How it works

1. Feed the skill 3-5 samples of your real writing
2. It analyzes your sentence patterns, word choices, tone, humor style, punctuation habits, and more
3. It saves a reusable voice profile you can apply to any future text
4. When you have AI-generated content, it rewrites it to match your profile

Profiles are saved as markdown files and persist across sessions. Create as many as you need for different writing contexts, plus per-platform sub-variants for surface tweaks.

## Example usage

```
"Build a voice profile from my blog posts in ~/writing/blog/"

"Does this LinkedIn post sound like AI wrote it?"

"Rewrite this draft using my blog-voice profile"

"Compare my blog-voice and email-voice profiles"

"Make a LinkedIn variant of my blog-voice"

"Has my writing drifted from my saved profile?"
```

## Installation

```bash
openclaw skill install chris-openclaw/voice-match-humanizer
```

## Why not just use a regular humanizer?

Most humanizer skills treat "human" as one generic voice. They remove AI patterns, but the result still doesn't sound like *you*. A marketing director's emails don't sound like a developer's blog posts, and neither sounds like a founder's investor updates. This skill captures those differences and, with sub-variants, can adjust them per platform.
