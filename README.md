# hourly-ai-news-agent

This repository stores the working outputs and lightweight configuration for an hourly AI news workflow.

## Purpose

Each hourly run should gather candidate AI news items, evaluate source quality, compile a digest, record coverage notes, and preserve enough metadata for downstream posting and auditing.

## Repository structure

- `digests/` - final digest markdown files for each run
- `raw-scans/` - raw scan outputs, intermediate notes, or source capture files
- `coverage-logs/` - coverage summaries describing which source types were checked and where gaps remained
- `tweet-history/` - metadata about posts or tweets created from digest outputs
- `config/` - simple workflow policies and configuration notes

## Expected hourly outputs

Hourly runs should save:

1. Digest markdown in `digests/`
   - ranked stories
   - source links
   - short summaries
   - why-it-matters notes

2. Scan coverage summaries in `coverage-logs/`
   - source categories checked
   - major sources covered
   - known gaps or missed categories
   - notes on skipped sources when relevant

3. Post metadata in `tweet-history/`
   - whether a post was published
   - headline or summary used
   - links or references included
   - timestamps and any status notes

Optional supporting artifacts can be saved in `raw-scans/`, including raw search results, scraped notes, and intermediate candidate lists.

## Usage guidance

- Prefer primary sources when available, such as company blogs, official docs, release notes, research lab announcements, and regulator or standards body publications.
- Use secondary reporting for context when primary sourcing is unavailable or incomplete.
- Keep filenames timestamped for easy chronological review.
- Preserve enough metadata to audit why a story was included or excluded.

See `config/source-policy.md` for the source selection policy.
