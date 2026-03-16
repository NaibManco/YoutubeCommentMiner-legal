---
permalink: /privacy-policy/
---

# Privacy Policy（MVP）— YouTube Comment Miner

Last updated: 2026-03-10

## Summary
YouTube Comment Miner is a Chrome extension that helps users analyze YouTube comments and export results. The MVP version processes data locally and does not upload comment content to any server.

## Data We Access
- YouTube video identifier (videoId) provided by the user
- Comment data returned by YouTube Data API v3 for the specified video

## Data We Store (Local Only)
Stored via Chrome `chrome.storage.local`:
- User-provided YouTube Data API key (BYOK mode)
- UI settings (e.g., selected ruleset, demo mode)
- Local cache of fetched results (keyed by videoId + ruleset, TTL 24h)

## Data We Do NOT Collect / Share
- We do not sell or share personal data.
- We do not upload comment content to any cloud service.
- We do not run background polling; actions are user-triggered.

## Data Retention & Deletion
- Cached results expire by default after 24 hours.
- You can clear cached data via the extension UI (Clear Cache).
- You can remove your saved API key via Options (Clear Key).

## Security
- This repo contains only legal/compliance documents.
- The extension does not embed any public API key in the extension repository build.
- API keys (when provided) are stored locally in the browser.

## Contact
For issues or requests, contact the developer via the Chrome Web Store listing.
