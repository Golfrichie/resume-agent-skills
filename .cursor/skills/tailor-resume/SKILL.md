---
name: tailor-resume
description: Tailor resume.md for a specific job - gaps, honest tailored resume, suggested additions, humble cover letter, and change summary.
---

# Tailor resume for one job

## Source of truth

- Read `resume.md` before editing anything.
- Job requirements not supported by `resume.md` go in `gaps.md` under **Do not claim** only - never into `tailored-resume.md`.
- `suggested-additions.md` is a check-before-using file. It asks you direct questions about related details, but those suggestions are not facts until `resume.md` is updated.

## Workflow

1. **Read the job** — Read the per-run prompt (company, role, URL, job description, output paths). Load `references/job-description-buckets.md` and `references/job-language-mapping.md`; classify requirements and note related experience separately from direct matches.
2. **Gaps** — Load `references/gaps.md`. Pick the fit tier from that reference and include the required `**Verdict:**` line. Write `jobs/<company-slug>/<role-slug>/gaps.md` with **Bottom line**, **What lines up**, **What is missing or not proven**, optional **Helpful bridges**, and **Do not claim**.
3. **Find possible additions** — Load `references/suggestion-mining.md`, `references/bullet-craft.md`, and `references/suggested-additions.md`. Build working notes from matches, related experience, and gaps. Write `suggested-additions.md` as check-before-using questions only.
4. **Tailor** — Load `references/keyword-alignment.md`, `references/markdown-resume-structure.md`, and `references/bullet-craft.md`. Write `tailored-resume.md` by rephrasing, reordering, splitting, or recomposing facts from `resume.md` only.
5. **Prepare** — Load `references/cover-letter-pattern.md`. Write `cover-letter.md` from verified resume facts and job requirements. Keep it to a short, conversational note — 2-3 short paragraphs, friendly greeting, friendly sign-off, no formal letterhead. Stay on verified strengths; do not flag gaps in the letter (they live in `gaps.md`). Do not treat suggestions as verified facts.
6. **Change summary** — Load `references/change-summary.md`. Document the output set and every meaningful tailored-resume edit in `change-summary.md`.
7. **Quality** — Skim `references/anti-patterns.md`, `references/agent-governance.md`, `references/master-profile-contract.md`, `references/ats-formatting-and-parsing.md`, and `references/export-and-plaintext-test.md`. Confirm every claim in `tailored-resume.md` and the cover letter traces to `resume.md`; suggestions remain clearly marked as questions.

## Output paths

Per-run prompt specifies:

- `jobs/<company-slug>/<role-slug>/gaps.md`
- `jobs/<company-slug>/<role-slug>/tailored-resume.md`
- `jobs/<company-slug>/<role-slug>/suggested-additions.md`
- `jobs/<company-slug>/<role-slug>/cover-letter.md`
- `jobs/<company-slug>/<role-slug>/change-summary.md`

Slug rules: lowercase, hyphenated; strip legal suffixes (Inc, LLC, Ltd) from company names.

## Output hierarchy

- `tailored-resume.md` is a view of `resume.md`, not a second source of truth.
- `suggested-additions.md` is a checklist of questions for you; nothing in it may be used as fact until `resume.md` changes.
- `cover-letter.md` may discuss gaps and bridges, but may not claim unverified suggestions as experience.
- `change-summary.md` is the reviewer entry point for all five outputs.

## PR

Title: `feat: tailor resume for <role> at <company>`

Commit all five job output files on the agent branch. Do not modify `resume.md` on `main` unless the user explicitly asks to update the master profile.
