# Suggestion mining

Purpose: derive check-before-using additions the reader can confirm or reject.

Algorithm:

1. Start from `gaps.md` and `job-language-mapping.md`.
2. For each gap, scan `resume.md` for related facts: same employer, same system, same data flow, same partner team, or related concept.
3. Write a yes/no question that names the resume fact and the missing detail.
4. Explain why the answer matters for the job.
5. Propose bullet wording only inside an "if true" field.
6. Include a verification cue: artifact, metric, incident, code path, stakeholder, or story to check.

Hard rules:

- Never propose wording for a job requirement with no related fact in `resume.md`.
- Never turn a suggestion into a fact in `tailored-resume.md`.
- Do not ask broad fishing questions like "have you done billing?" Name the existing fact that motivated the question.
- Split multi-part questions when someone could truthfully answer yes to one part and no to another.
- Prefer 5-8 high-signal suggestions over a long checklist.

Good shape:

`Question for you`: Your Stripe lifecycle webhook work at Startup Labs - did it include retry-safe handling for duplicate events?

Bad shape:

`Question for you`: Have you built exactly-once billing systems?
