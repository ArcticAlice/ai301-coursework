# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

"https://github.com/codepath/pathreview-ai301-fa26-s1/issues/45"

[The individual Path Review issue page. A link to the repository or the issue list
does not satisfy this field.]

**Verdict output**

[Your skill's live-mode output for this issue, pasted verbatim and ending with the
fenced JSON verdict block. A summary does not satisfy this field.]

**The verdict must record `accept` for this issue.** Choose an issue your own skill
accepts. If your skill rejects every candidate you try, that is a signal about your
rubric rather than about the issues: revise it and re-run — retries are unlimited and a
partial re-run costs about $0.20 — or run the skill on different candidates. Output
recording `reject` for the issue you chose earns no credit for this field.

2. #45 — Property-based tests for the PII scrubber [accept]

Identical required-check profile: unassigned, 0 comments, labels-only timeline, no linked PR. newcomer-signal fails the same way (tier-2, no GFI label).

Fit: also Python and also tier-2, but ranked second because hypothesis property-based testing is a different paradigm from the example-based testing taught in class — you'd be learning the tool and the domain at once.

{
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/45",
    "checks": [
      {"name": "maintainer-recent-activity", "grade": "pass", "evidence": "Aburke225 (COLLABORATOR) commit f89c06fc on 2026-09-16, 6 days before today 2026-09-22"},
      {"name": "repo-not-abandoned", "grade": "pass", "evidence": "archived: false; pushed_at 2026-09-16T21:48:27Z"},
      {"name": "issue-bounded-scope", "grade": "pass", "evidence": "Single target file tests/unit/test_pii_scrubber.py; one deliverable, not an umbrella issue"},
      {"name": "issue-not-support-request", "grade": "pass", "evidence": "'Add property-based tests using hypothesis' — a concrete change, not a usage question"},
      {"name": "issue-not-assigned", "grade": "pass", "evidence": "assignee: null, assignees: (empty)"},
      {"name": "issue-no-active-pr", "grade": "pass", "evidence": "Only open PR repo-wide is #74 referencing issue #60; issue 45 timeline has no cross-referenced PR"},
      {"name": "issue-not-claimed", "grade": "pass", "evidence": "comments count: 0; timeline contains only three 'labeled' events by Aburke225"},
      {"name": "maintainer-response-time", "grade": "pass", "evidence": "Issue #43 opened 2026-09-10, Aburke225 (COLLABORATOR) replied 2026-09-16 = 6 days"},
      {"name": "contributor-activity", "grade": "pass", "evidence": "Contributors beyond owner: jamjamgobambam 10, ascherj 2, margaretfero-codepath 1; open PR #74 by nianiiier"},
      {"name": "issue-clear-requirements", "grade": "pass", "evidence": "Specifies the library (hypothesis), the target file, and the invariant: scrubber always removes PII"},
      {"name": "issue-reproducible", "grade": "pass", "evidence": "Not a bug report; body states the gap — no property-based coverage for varied PII formats"},
      {"name": "issue-testable", "grade": "pass", "evidence": "Property tests self-verify the invariant; README documents 'make test-unit'"},
      {"name": "contributor-documentation", "grade": "pass", "evidence": "docs/CONTRIBUTING.md covers branch naming, commit conventions, CI requirements, code style"},
      {"name": "contributor-setup", "grade": "pass", "evidence": "README: 'cp .env.example .env; docker compose up -d; make setup; make run' and 'make test-unit'"},
      {"name": "maintainer-guidance", "grade": "pass", "evidence": "Body authored by COLLABORATOR Aburke225 prescribes the tool and approach; no unanswered questions in thread"},
      {"name": "newcomer-signal", "grade": "fail", "evidence": "Labels are enhancement, tests, tier-2 — no 'good first issue' or 'help wanted'"}
    ],
    "verdict": "accept"
  },

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**

[The agreement score of each run you did, in order. A single run is a complete answer if
only one run occurred. **The last score in your list must match the agreement line in the
`eval-run.txt` you committed** — that file is the record of your final run.]

**Issue analysis**

[One scored issue, identified by id (`issue-01` through `issue-20`; the `calib-`
issues are not scored). State your rubric's decision, the gold label, and the
reasoning that produced your rubric's result.]

**Check rationale**

[One check from the `rubric.md` uploaded to `tools/issue-select/`, quoted as it is
currently written, with the reasoning behind its current form.]

**Trade-offs**

[What the quoted check gives up. Any one of these is a complete answer: an issue whose
result it changes, a canary you re-ran with `--only`, a case you accept it will miss, or a
stated reason nothing changed elsewhere. "Nothing changed, and here is how I know" earns
the point in full when the reason follows.]

---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

**Selection rationale**

[Answer all three:

1. The issue's fit to your interests and to the time available.
2. What the verdict identified correctly, and what you weighed that the rubric could
   not.
3. The anticipated difficulty in claiming it.]

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
