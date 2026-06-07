# Resume Agent — demo resume repo

Copy this repository to your GitHub account and connect it in the [Cursor dashboard](https://cursor.com/dashboard) so cloud agents can clone it.

## Setup

1. Create a new repo and push these files (including `.cursor/skills/`).
2. In Cursor, connect the GitHub repository for cloud agents.
3. Set `RESUME_REPO_URL` in the Resume Agent API to your repo URL.
4. Keep `resume.md` on `main` as your canonical profile.

## First run

Use the Resume Agent Chrome extension or API with a real job description. The cloud agent should:

1. Read `resume.md`
2. Follow `.cursor/skills/tailor-resume/SKILL.md`
3. Write five files under `jobs/<company>/<role>/`:
   - `gaps.md`
   - `tailored-resume.md`
   - `suggested-additions.md`
   - `cover-letter.md`
   - `change-summary.md`
4. Open a PR via `autoCreatePR`

The generated `gaps.md` should include:

- **Bottom line** with `**Tier:**`, `**Verdict:**`, and a short narrative
- **What lines up**
- **What is missing or not proven**
- **Helpful bridges** when useful
- **Do not claim** items that must not be added to `tailored-resume.md`

`suggested-additions.md` and cover-letter guidance are check-before-using outputs; the tailored resume still uses only facts from `resume.md`. Cover-letter copy should stay humble and conversational.

If the skill is not auto-detected, mention **`tailor-resume`** explicitly in the run prompt (the API does this by default).
