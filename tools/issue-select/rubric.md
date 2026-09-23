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
families: the maintainer is alive, the repo is in use, the scope fits a newcomer, and nobody else is already on it. A rubric that ignores a family will fail eval issues designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| maintainer-recent-activity | Repo-facts block: recent default-branch commits or other recent maintainer activity | At least one maintainer has performed a substantive action within 180 days of the repo-facts capture date (live mode: within 180 days of today) | required |
| repo-not-abandoned | Repo-facts block: `archived:` and last push to any branch | Repo is not archived and the last push to any branch is within 365 days of the capture date (live mode: within 365 days of today) | required |
| issue-bounded-scope | Issue body and comment thread | Issue is not an umbrella/tracking issue and there is no clear evidence from the issue or maintainers that it requires multiple unrelated changes or is currently too broad to implement as one contribution | required |
| issue-not-support-request | Issue title and body | Issue describes a concrete bug or specific change rather than primarily asking how to use the project | required |
| issue-not-assigned | Repo-facts block: `this issue: assignees:` | Assignees list is empty | required |
| issue-no-active-pr | Repo-facts block: `linked PRs:` and PRs mentioned in the comment thread | No currently open PR is clearly intended to resolve or substantially implement the issue | required |
| issue-not-claimed | Comment thread and explicit indications of ongoing work | There is no clear, current indication that another contributor is actively working on or has claimed the issue | required |
| maintainer-response-time | Repo-facts block: maintainer first-response sample | At least one sampled issue received a maintainer response within 30 days of being opened | preferred |
| contributor-activity | Recent commits, merged PRs, and contributor history | There is evidence that people other than the primary maintainer/owner have contributed to the repository | preferred |
| issue-clear-requirements | Issue body and comment thread | The issue provides enough information to understand the requested behavior or change | preferred |
| issue-reproducible | Issue body and comment thread | For a bug, the issue provides a reproduction, concrete symptoms, or enough information to understand the problem | preferred |
| issue-testable | Issue body, comment thread, and repository test instructions | There is a reasonable way to determine whether the issue has been resolved | preferred |
| contributor-documentation | README, CONTRIBUTING documentation, and developer documentation | Documentation provides useful information for contributing, if such documentation exists | preferred |
| contributor-setup | README, CONTRIBUTING documentation, and development/test instructions | The repository provides instructions for setting up or testing the project, if such instructions exist | preferred |
| maintainer-guidance | Comment thread | Maintainers have provided implementation or requirements guidance when clarification was needed | preferred |
| newcomer-signal | Issue labels and comment thread | The issue has an explicit newcomer signal such as `good first issue`, `help wanted`, or a maintainer statement that newcomers can work on it | preferred |

## Verdict rule

Accept the issue if every required check passes. A required check fails only when the available evidence indicates that its pass condition is not satisfied.

For required checks, `unclear` counts as fail only when the missing information prevents determining that the issue is available and actionable. Preferred checks never change the accept/reject verdict.
