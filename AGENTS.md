# Resume repository

For job tailoring runs, use the **`tailor-resume`** skill:

- Read `.cursor/skills/tailor-resume/SKILL.md` (or invoke `/tailor-resume`)
- Treat `resume.md` as the single source of truth for facts
- Write per-job outputs under `jobs/<company-slug>/<role-slug>/`: `gaps.md`, `tailored-resume.md`, `suggested-additions.md`, `cover-letter.md`, and `change-summary.md`
- In `gaps.md`, include a plain-language `**Tier:**` and `**Verdict:**` under **Bottom line**.

Do not invent experience. Unsupported requirements belong in `gaps.md`, not the tailored resume. Suggested additions are direct check-before-using questions for the user, not facts.
