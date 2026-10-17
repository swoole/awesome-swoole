# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

An "awesome list": a single curated `README.md` of Swoole-related projects, libraries, and resources. There is no application code, build step, or test suite. Nearly all changes are edits to `README.md`.

## Link checking

CI (`.github/workflows/awesomebot.yml`) runs [awesome_bot](https://github.com/dkhamsing/awesome_bot) on every push to `main` and daily. To run it locally before committing:

```bash
gem install awesome_bot -v 1.20.0
awesome_bot README.md --request-delay 2 --set-timeout 45 --allow-dupe --white-list amazon.com,amazon.co.jp,drupal.org
```

If a valid URL is falsely reported as broken (e.g., the site blocks bots), add its domain to the `--white-list` in the workflow file rather than removing the entry.

## Adding a new project/library

To find candidate projects, use the `discovering-swoole-projects` Claude
Code skill (`.claude/skills/discovering-swoole-projects/SKILL.md`) — it
searches GitHub for actively maintained Swoole-related repositories not
already listed here and lets you pick which to add.

Constraints and conventions when adding an entry to `README.md`:

1. **Relevance**: The project must be related to Swoole — built on it, integrating with it, or explicitly supporting it. General-purpose PHP packages that merely happen to work under Swoole don't belong unless coroutine-friendliness/Swoole support is a stated feature.
2. **Section**: Place the entry under the most specific existing section (e.g., a Hyperf queue component goes under _Tasks and Queues_, not _Frameworks_). Use _Miscellaneous_ only when nothing else fits. If adding a new section, also add it to the manually-maintained Table of Contents and keep the TOC anchor links working.
3. **Entry format**: `- [project-name](URL) - Description.`
   - The name is usually `vendor/package` (as on GitHub/Packagist) or the project's display name (e.g., `Hyperf`, `Simps`).
   - The description is one or two complete sentences ending with a period, stating what the project does. Neutral tone; no marketing superlatives beyond what's factual.
4. **Ordering**: Entries within a section are ordered alphabetically (case-insensitive). Grouped sub-lists (e.g., per-framework groups under _Framework Integration_) are also alphabetical. Two deliberate exceptions:
   - _Laravel Octane_ stays pinned first in the Laravel group under _Framework Integration_, as the first-party option.
   - _Swoole Videos_ is ordered chronologically (oldest first), not alphabetically.
5. **Non-English documentation**: Append the `:globe_with_meridians:` emoji to entries whose documentation is written in a non-English language (this is explained by the NOTE near the top of the README).
6. **Hyperf marker**: Append the `:jigsaw:` emoji to entries that are Hyperf components or are built on Hyperf (this is also explained by the NOTE near the top of the README). When an entry has both markers, `:globe_with_meridians:` comes first and `:jigsaw:` second (e.g. `... Description. :globe_with_meridians: :jigsaw:`). Don't use `:jigsaw:` anywhere else in the README.
7. **Status markers**:
   - Work-in-progress projects get a trailing `#WIP` tag.
   - Abandoned/unmaintained projects that are still worth listing use strikethrough (`~~[name](url)~~`) with a note explaining the status and, when possible, pointing to a replacement (see the `yasd` entry).
   - Archived repositories should say so in the description (see the `Siler` entry).
8. **Reference-style links**: Some entries use reference-style links (`[Phluxor]`) with definitions collected alphabetically at the bottom of the README. Prefer inline links for new entries; if a name is linked from multiple places, use a reference-style link and add its definition to the bottom list in alphabetical order.
9. **Nested entries**: Related sub-projects nest one level under a parent entry with 4-space indentation (e.g., the Docker images under _Docker_ in _Development Environment_).
10. **Verify before adding**: Confirm the URL resolves (CI will catch broken links, but check locally first) and that the project is not already listed elsewhere in the README, including under a different section or name.

## Removing or updating entries

- Prefer marking a project as unmaintained (strikethrough + note) over deleting it, unless the repository is gone or the project was never Swoole-related.
- When a repository moves, keep the listed name that users know but point the link at the new location (e.g., `longlang/phpkafka` links to `swoole/phpkafka`).
