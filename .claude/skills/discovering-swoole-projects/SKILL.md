---
name: discovering-swoole-projects
description: Use when asked to find new Swoole-related GitHub projects/libraries to consider adding to this awesome list, or to research the Swoole ecosystem for actively maintained repositories not yet covered by README.md.
---

# Discovering Swoole Projects

## Overview

Searches GitHub for repositories that depend on or integrate with Swoole,
drops ones already listed in `README.md`, ones on the ignore list, ones that
look abandoned, and ones with too few stars to be worth reviewing. Writes the
survivors as a numbered report under `./temp/` and also presents them in the
reply, then lets the user pick entries by index to add to `README.md`
directly — without running `git add`/`commit`/`push`.

Uses the `gh` CLI, which anyone running this skill needs installed and
authenticated (`gh auth login`) themselves — this skill has no
project-specific or personal configuration baked in, so it's safe to commit
and share. Run it from the repository root — steps 1 and 9 use paths
(`README.md`, `./temp/`) relative to it.

## Procedure

1. **Build the exclusion set** — every `owner/repo` already linked from
   `README.md` (inline and reference-style links both match this regex; note
   the optional `https?:` — the README's intro line links the core
   `swoole/swoole-src` repo with a protocol-relative `//github.com/...` URL):
   ```bash
   grep -oE '(https?:)?//github\.com/[A-Za-z0-9_.-]+/[A-Za-z0-9_.-]+' README.md \
     | sed -E 's#(https?:)?//github\.com/##' | tr 'A-Z' 'a-z' | sort -u
   ```
   This still won't catch a project linked via its own custom domain instead
   of GitHub (e.g. Hypervel is listed as `https://hypervel.org`, not its
   GitHub URL) — for each surviving candidate, also grep its bare repo name
   against README.md as a cheap secondary check before treating it as new,
   and read the surrounding line to confirm it's a real match, not a
   coincidental word (generic repo names like `http` or `.github` will
   false-positive here).

2. **Check the ignore list** below. Exclude any candidate that is one of the
   ignored projects. Also exclude a candidate that depends on one, but only
   where that ignore-list row's own "Why" says to (check its
   `composer.json`, per step 5) — dependent-exclusion isn't implied for
   every row, only where stated.

3. **Gather candidates from multiple sources** — a single keyword search is
   noisy (see Gotchas), so combine:
   - Keyword search, name/description only:
     `gh search repos swoole --match=name,description --archived=false --sort=stars --limit 100 --json fullName,url,description,stargazersCount,pushedAt,isArchived`
   - Topic search: same command with `--topic=swoole` instead of the
     positional query + `--match`.
   - Dependency search (finds real users of the package, not just mentions) —
     repeat for each require-string that signals a real Swoole dependency
     (`swoole/swoole`, `ext-swoole`, `swoole/library`, `swoole/hyperf`, etc.):
     `gh search code "swoole/swoole" --filename=composer.json --limit 50 --json repository`
     then enrich each hit (code search returns no stars/dates):
     `gh repo view <owner>/<repo> --json nameWithOwner,url,description,stargazerCount,pushedAt,isArchived`
     (note the field is `stargazerCount` here, not `stargazersCount` — see Gotchas).

4. **Merge and dedupe** all candidates into one map keyed by lowercased
   `owner/repo`, then drop any key present in the exclusion set (step 1) or
   the ignore list (step 2).

5. **Filter for relevance** (manual judgment, per this repo's `CLAUDE.md`):
   drop anything where Swoole is just an incidental keyword hit — e.g. giant
   unrelated curated lists, tutorials, repos whose owner tags dozens of
   unrelated framework names (topic-tag spam), or forks of `swoole/swoole-src`
   itself. A candidate's own description not mentioning Swoole doesn't
   necessarily disqualify it: check its `composer.json` for a real
   `require`/`suggest` on `swoole/swoole` or `ext-swoole` with an explanatory
   comment (`gh api repos/<owner>/<repo>/contents/composer.json --jq '.content' | base64 -d | grep -i swoole`)
   before dropping a candidate whose description is silent on Swoole. This
   same check is how you catch a candidate depending on an ignore-listed
   project (step 2) — grep the decoded `composer.json` for the ignored
   package name instead of `swoole`.

6. **Filter for maintenance**: drop any repo where `isArchived` is true, or
   `pushedAt` is more than 365 days before today's date.

7. **Filter for stars**: drop any repo with 5 stars or fewer.

8. **Sort** survivors by `stargazersCount`/`stargazerCount` descending.

9. **Write the report and present it** — build the numbered table described
   in Output format below, save it to `./temp/new-swoole-projects-<YYYY-MM-DD>.md`
   (today's date; create `./temp/` if it doesn't exist), and also paste the
   same table into the reply. Follow with a one-line prompt asking which
   indices to add to `README.md`. Don't use a multiple-choice tool for this;
   the count and combination of picks is arbitrary, so ask in plain text
   (e.g. "Reply with the index numbers to add, like `1,4,7`.").

10. **On the user's reply**, add the selected repos to `README.md`, one at a
    time, following this repo's `CLAUDE.md` exactly (section placement,
    alphabetical ordering within the section, the
    `- [name](URL) - Description.` entry format, and nested-entry
    indentation where a candidate belongs under an existing parent entry).
    For each one, decide the `:globe_with_meridians:` marker the same way
    the rest of the list uses it (see Non-English marker below) rather than
    guessing from the search result's description alone.
    **Never run `git add`, `git commit`, or `git push`** — leave the edited
    `README.md` as an uncommitted working-tree change for the user to review
    and commit themselves.

## Non-English marker

Per the README's own note, `:globe_with_meridians:` means "documentation
written in non-English languages" — it describes the *project's docs*, not
the one-line description you write for the list entry (that description is
always written in English regardless). Before adding each selected entry:

- Fetch the repo's own README to check its actual language, e.g.
  `gh api repos/<owner>/<repo>/readme --jq '.content' | base64 -d | head -c 2000`.
- Add the marker only if that README (or its docs site, if it links one) is
  primarily in a non-English language. A repo whose GitHub *description* or
  topics happen to be in Chinese/Japanese/etc. isn't itself evidence either
  way — check the actual docs.
- Don't guess from the search result's `description` field alone — it has
  produced both false positives and false negatives in practice.

## Ignore list

Projects excluded from candidate results regardless of the filters above —
add a row here to extend it:

| Project | Why |
|---|---|
| EasySwoole (`easy-swoole` org, e.g. `easy-swoole/easyswoole`) | Excluded by maintainer request. Also exclude any other candidate whose `composer.json` requires an `easy-swoole/*` package. |
| `swoole/typephp` | Excluded by maintainer request. |
| `swoole/phpx` | Excluded by maintainer request. |
| `hyperf/hyperf-skeleton` | Excluded by maintainer request. |
| `daodao97/apidog` | Excluded by maintainer request. |
| `swoole/phpy` | Excluded by maintainer request. |

## Output format

Save this table to `./temp/new-swoole-projects-<YYYY-MM-DD>.md` (most stars
first) and paste the same content into the reply — a short header plus the
table is enough, no need for a full research-report writeup:

```markdown
# New Swoole projects — <YYYY-MM-DD>

| # | Repo | Stars | Last commit | Description |
|---|---|---:|---|---|
| 1 | [owner/repo](https://github.com/owner/repo) | 1234 | 2026-08-01 | One-line description. |
| 2 | [owner2/repo2](https://github.com/owner2/repo2) | 88 | 2026-07-15 | One-line description. |
```

Every "Repo" column entry, in this table and in any supplementary table you
add to the report (e.g. a breakdown of why survivors were excluded), must be
a markdown link to the GitHub repo (`[owner/repo](https://github.com/owner/repo)`)
— never bare `owner/repo` text.

## Gotchas

- **JSON field names differ between `gh` subcommands**: `gh search repos`
  exposes `stargazersCount`; `gh repo view` exposes `stargazerCount` (no
  trailing "s" on "stargazer"). Mixing them up silently errors with "Unknown
  JSON field".
- **Keyword search is noisy**: `--match=readme` (or omitting `--match`
  entirely) surfaces huge unrelated repos (other awesome-lists, tutorials)
  that merely mention "swoole" somewhere in their README. Prefer
  `--match=name,description` for the keyword search, and always eyeball
  descriptions in step 5 rather than trusting the filter alone.
- **`--updated`/sort=updated is not the same as "actively maintained"** —
  always check the actual `pushedAt` value against the 1-year cutoff rather
  than relying on search ordering.
- Case in GitHub URLs isn't significant for repo identity; always lowercase
  both sides before comparing against the README's exclusion set.
- Apply the star filter (step 7) as early as your data allows — repo-search
  results already carry star counts, so filter those before spending an API
  call enriching a dependency-search hit that would be dropped anyway.
- The GitHub search `description` field is not a reliable signal for the
  `:globe_with_meridians:` marker — a Chinese description doesn't mean the
  actual README/docs are in Chinese, and vice versa. Check the real README
  (see Non-English marker) before adding the marker.
- `gh search code` (used in the dependency search and for `composer.json`
  checks) has a much tighter GitHub rate limit than `gh search repos`. If a
  run starts failing with rate-limit errors partway through, pause and
  retry rather than dropping those candidates from the results.
- Rerunning the skill same-day overwrites that day's report file at the
  same path — that's intentional, not a bug to work around.
