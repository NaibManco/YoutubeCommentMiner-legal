---
permalink: /privacy-policy/
---

# Privacy Policy（MVP）— YouTube Comment Miner

Last updated: 2026-11-23

## Summary
YouTube Comment Miner is a Chrome extension that helps users analyze YouTube comments and export results. Comment tagging and file export happen locally in your browser; we do not sell user data or upload your exported comment sets to our servers.

## Data We Access
- YouTube video identifier (videoId) provided by the user
- Comment data returned by YouTube Data API v3 for the specified video
- Bundled local sample comments when demo data is used without an API key

## Data We Store (Local Only)
Stored via Chrome `chrome.storage.local`:
- User-provided YouTube Data API key (BYOK mode)
- Optional Credit Pass code and remaining page balance snapshot (Credit Pass mode)
- UI settings (e.g., selected ruleset)
- Local cache of fetched results (keyed by credential mode, videoId, ruleset, maxPages and pageSize; TTL 24h)

## Demo Mode
- Built-in local demo data is bundled with the extension and does not call the YouTube API.
- If you have not added your own API key or Credit Pass, the extension uses a shared demo key. Requests still go directly from your browser to Google's YouTube Data API and are subject to demo limits.
- Users can add their own YouTube Data API key to fetch real comments without demo limits.

## Optional Credit Pass Mode
- If you activate an optional prepaid Credit Pass code (`YTCM-*`), fetch requests (`videoId`, `maxResults`, `pageToken`, `installId`, and your Credit Pass code) are sent to our Cloudflare Worker proxy so it can call Google's YouTube Data API v3 on your behalf without requiring you to set up a Google Cloud API key.
- The proxy caches public YouTube comment pages for up to 12 hours and stores only Credit Pass balances and daily page counts (no personal identity or browsing history).
- You can remove your saved Credit Pass anytime via Options (`Remove pass`).

## Data We Do NOT Collect / Share
- We do not sell or share personal data.
- We do not upload comment content to any cloud service.
- We do not run background polling; actions are user-triggered.

## Data Retention & Deletion
- Cached results expire by default after 24 hours.
- You can clear cached data via the extension UI (Clear Cache).
- You can remove your saved API key via Options (Remove key).

## Security
- This repo contains only legal/compliance documents.
- The extension does not embed any public API key in the extension repository build.
- API keys (when provided) are stored locally in the browser.
- Demo Web Store packages may contain a restricted public demo key. This key is used only for limited demo requests to YouTube Data API v3 and can be disabled by the maintainer.

## Contact
For issues or requests, contact the developer via the Chrome Web Store listing.
