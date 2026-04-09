# Regulatory Pulse Data

Public data feed for the Lark workplace widget **Regulatory Pulse**.

This repository hosts a single machine-generated JSON file — `pulse.json` — that is refreshed daily by a local collector running on the maintainer's machine. The Lark widget fetches this file directly via `raw.githubusercontent.com` and renders the latest high-relevance regulatory announcements.

## Files

| Path | Purpose |
|---|---|
| `pulse.json` | Latest scored regulatory announcements (public) |
| `pulse-archive/` | Historical snapshots, one file per day |

## Pipeline

```
RSS/HTML sources → local Python collector → Claude scoring → pulse.json → git push → Lark widget
```

## Disclaimer

Content summaries are AI-generated (Claude) from publicly published regulatory communications. Not legal advice. Refer to the original source for authoritative text.
