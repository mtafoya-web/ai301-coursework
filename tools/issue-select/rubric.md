# Rubric: is this a good first issue?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever checks
you define here. It ships empty on purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where. Name the source
     (repo-facts block, issue body, comment thread, or the locations in
     references/evidence-guide.md). "The repo" is not a source; "the last
     5 default-branch commit dates" is.
   - Pass condition: a condition someone else could apply and get your
     answer. Prefer thresholds with numbers ("a maintainer commented
     within 30 days") over adjectives ("maintainer is responsive").
   - Weight: `required` (a fail here rejects the issue) or `preferred`
     (never changes the verdict; a nice-to-have that helps rank the
     issues you accept).

2. A verdict rule below the table: how the check grades combine into
   accept or reject, including how `unclear` is treated. The verdict
   space is binary. If you write no rule for `unclear`, the skill treats
   it as fail.

Cover what actually kills first contributions. The lecture named four
families: the maintainer is alive, the repo is in use, the scope fits a
newcomer, and nobody else is already on it. A rubric that ignores a family
will fail eval issues designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| maintainer-active | Repo facts: last 5 default-branch commits and maintainer first-response sample. | Pass if there is at least one non-bot default-branch commit within 90 days of the capture date OR a maintainer first-response sample within 30 days. | required |
| repo-active | Repo facts: archived flag, latest release, and last push to any branch. | Pass if the repo is not archived and either the latest release or last push occurred within 180 days of the capture date. | required |
| newcomer-scope | Issue body, comment thread, issue age, and linked PR history. | Pass if the issue has one coherent contribution goal, even when it touches multiple related files, describes multiple possible causes, or suggests several implementation steps. Fail only if it is explicitly an umbrella/tracking issue, purely a usage/support question, a maintainer explicitly says broad/core-internal changes are required, or the history shows multiple abandoned contribution attempts over a long period. | required |
| implementation-ready | Issue body and comment thread. | Pass unless a required input, requirement, or design decision is explicitly still TBD or unresolved and must be decided before implementation can reasonably begin. Possible causes, suggested approaches, optional follow-up work, and implementation details that can be determined while solving the issue do not fail this check. | required |
| unclaimed | Repo facts for this issue: assignees and linked PRs; issue comment thread for active claim comments. | Pass if there is no current assignee, no open linked PR, and no unresolved recent claim comment indicating someone is actively working on it. | required |
| ai-policy-compatible | Repo facts: contribution policy and any AI policy files or contribution templates. | Pass if the repository does not explicitly ban AI-generated or AI-assisted contributions. Disclosure, testing, understanding, or human-review requirements still pass. Silence also passes. | required |
| good-first-issue-signal | Issue labels and issue body. | Pass if the issue has a good-first-issue or equivalent newcomer-friendly label, or the issue body explicitly presents it as beginner-friendly. | preferred |

## Verdict rule
Accept if every required check passes.

Reject if any required check fails.

Treat 'unclear' as fail for required checks

Preferred checks never change the accept/reject verdict; tehy are only ised to rank accepted issues.

