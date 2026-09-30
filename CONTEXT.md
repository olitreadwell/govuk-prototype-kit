# alphagov/govuk-prototype-kit context
> refreshed 2026-09-30 | upstream default: main @ b2a3a0f9d7fdbcdec7eac6934dcb05385bdd845b

## Identity & policies
- upstream: alphagov/govuk-prototype-kit, default branch `main`, primary language JavaScript (Node CLI + Express app), English-first: yes (README, CONTRIBUTING, docs all en-GB).
- CLA/DCO: none (CONTRIBUTING.md has no CLA bot and no DCO sign-off requirement; no .github CLA workflow).
- AI-assisted PR policy: unstated (no AI/LLM/generated mention in CONTRIBUTING, README or .github; no AI_POLICY.md at repo or alphaGov/.github org level).
- signed commits required: no (branches/main/protection -> 404; prior fork PRs merged-able).
- PR template: none (`community/profile` reports `pull_request_template: null`; no PULL_REQUEST_TEMPLATE under `.github/` or repo root; org `alphagov/.github` has no PR template either). Bodies use the pipeline fallback.
- external tracker: GitHub issues only.

## Conventions (verified from merged PRs)
- branch naming: plain kebab-case description from the maintainers (`update-govuk-frontend`, `remove-deprecated-task-list`, `fix-build-release-port`, `update-links`); no `type/` prefix. Fork branches use the same style (fork PR #1 = `fix-404-page-layout`).
- commit style: imperative sentence, capitalised, no Conventional-Commit prefix (`Remove out-of-date support release documentation`, `Update release documentation`).
- test command: `npm test` (runs `test:unit` + `test:integration` + `lint`); lint alone is `npm run lint` (standard).
- CI checks that gate a PR: Validate, Lint, Tests (Node 22/24/26 x macOS/Windows/Ubuntu), Tests (Acceptance), Tests (Heroku). All ran green on fork PR #1.
- how outside PRs actually get merged: responsive; recent external merges `owenatgov` typo #2655 (2026-09-17) and `chrispymm` plugin #2478 (2026-09-02). CONTRIBUTING says "minimal support" but small external PRs do land.

## Maintainer picture
- active maintainers: NickColley, romaricpascal, domoscargin, 36degrees (all merged PRs in the last week are theirs).
- areas in flight (avoid): release-script extraction/removal (#2702, #2685), flaky step-by-step tests (#2699), dependency bumps.
- docs/issue-template link content is quiet — no in-flight PR touches it.

## Issue-area health
- #2521 (404 header with Frontend v6): maintainer-confirmed still open, maintainer explained root cause (2026-03-27) and re-confirmed on 2026-09-28. Covered by fork PR #1 (`fix-404-page-layout`).
- #2583 (pre-release version pick): maintainer-owned, open design discussion on approach ("next" tag) — area in flux, do not touch.
- Most open issues are maintainer-authored internal work items (EPIC / release / test refactor) — not external-pick material.

## Gap ledger (dedupe — READ FIRST, never re-pick)
- 2026-08-26 issue #2521 — pr-opened — fork PR #1 renders 404/500 via `nunjucksManagementEnv`; do not re-attempt.
- 2026-09-30 self-found dead links (GDS Way + Design System community backlog) — pr-opened — see mined gaps below.

## Mined gaps (discovered, not yet attempted)
- 2026-09-30 docs dead links — `CONTRIBUTING.md` and `.github/ISSUE_TEMPLATE/tech-debt.yaml` point at `gds-way.cloudapps.digital` (NXDOMAIN, 000); `.github/ISSUE_TEMPLATE/feature-request.md` points at `design-system.service.gov.uk/community/backlog/` (410 Gone). Replacements verified live (gds-way.digital.cabinet-office.gov.uk pages return 200 with the same anchors; the live community backlog is github.com/alphagov/govuk-design-system-backlog/issues). Dedupe: no upstream issue/PR covers them. — status: attempted
