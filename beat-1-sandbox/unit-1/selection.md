# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

https://github.com/codepath/pathreview-ai301-fa26-s3/issues/6

**Verdict output**

[Your skill's live-mode output for this issue, pasted verbatim and ending with the
fenced JSON verdict block. A summary does not satisfy this field.]

**The verdict must record `accept` for this issue.** Choose an issue your own skill
accepts. If your skill rejects every candidate you try, that is a signal about your
rubric rather than about the issues: revise it and re-run — retries are unlimited and a
partial re-run costs about $0.20 — or run the skill on different candidates. Output
recording `reject` for the issue you chose earns no credit for this field.

```
Summary

All three issues are candidates from the correct repo (codepath/pathreview-ai301-fa26-s3), which is active (not archived, pushed 2026‑09‑16, ~13 days ago) and has no stated AI-contribution ban (no CONTRIBUTING.md/AI-policy restriction — silence passes). All three accept.

Ranked (fit: healthcare/EMS-adjacent ML background, general SWE experience):

1. #58 – Bias detector patterns too narrow — tier‑1, safety-labeled, clean self-contained regex fix with solid repro steps, no competing open PR.
2. #53 – PII scrubber misses parenthesized phone numbers — explicitly labeled "good first issue," extremely well-trodden (10 reproduction reports, consistent root-cause diagnosis), but flagged: an open, unmerged PR (#77) already targets this exact fix. The scope house rule only waives claim comments, not linked PRs, so I graded "Unassigned" unclear rather than silently deciding — worth checking whether the classroom credit model (PR-per-student, not first-to-merge) still makes this fair game before you start.
3. #6 – Hybrid retriever skips keyword indexing — accepted, well-described directly by the maintainer, but tier‑2/4–6h estimated and untouched by anyone, so it's a bigger, less-trodden first step than the two regex bugs.

None of the three are meaningfully related to EMS/medicine (repo is an AI portfolio-review tool), so the "Interest" preferred check fails for all three equally and didn't drive the ranking.

[
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/58",
    "checks": [
      {"name": "Maintained", "grade": "pass", "evidence": "Repo pushed_at 2026-09-16, ~13 days before today (2026-09-29), within 30 days"},
      {"name": "Active", "grade": "pass", "evidence": "repo archived: false; no comment states discontinuation"},
      {"name": "Actionable", "grade": "pass", "evidence": "Body names specific file `bias_detector.py`, gives reproduction snippet plus observed vs expected, and lists the 9 related failing tests"},
      {"name": "Confirmed dead-end", "grade": "pass", "evidence": "No maintainer/contributor comment states the issue is hard/blocked; both commenters (RichardGabelman, Dannypxp) reproduced it without difficulty"},
      {"name": "Unassigned", "grade": "pass", "evidence": "assignees: []; comments are classmate claims (RichardGabelman, Dannypxp), which the Path Review house rule says don't block; no linked/open PR found via search"},
      {"name": "AI policy", "grade": "pass", "evidence": "No CONTRIBUTING.md at repo root, docs/CONTRIBUTING.md has no AI-use section at all — silence passes"},
      {"name": "Interest", "grade": "fail", "evidence": "Repo is 'PathReview', an AI portfolio-review tool for developers — bias-detector regex work has no EMS/medicine/clinical relevance"},
      {"name": "Reach", "grade": "pass", "evidence": "6 stars, 146 forks (classroom forks)"}
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/53",
    "checks": [
      {"name": "Maintained", "grade": "pass", "evidence": "Repo pushed_at 2026-09-16, ~13 days before today, within 30 days"},
      {"name": "Active", "grade": "pass", "evidence": "repo archived: false; no discontinuation comment"},
      {"name": "Actionable", "grade": "pass", "evidence": "Carries a maintainer-applied 'good first issue' label plus names `pii_scrubber.py`, reproduction snippet, and 4 named failing tests"},
      {"name": "Confirmed dead-end", "grade": "pass", "evidence": "No maintainer states it's hard/blocked; 10 independent contributor reproductions all converge on the same simple root cause (missing space in a separator regex class)"},
      {"name": "Unassigned", "grade": "unclear", "evidence": "assignees: [] and many classmate claim comments (waived by house rule), BUT PR #77 'fix: redact parenthesized US phone numbers in PII scrubber' is open (not merged) and directly targets this issue — the house rule text only waives 'claim comments', not linked PRs, so this is flagged for manual judgment rather than assumed to pass"},
      {"name": "AI policy", "grade": "pass", "evidence": "docs/CONTRIBUTING.md has no AI-use restriction — silence passes"},
      {"name": "Interest", "grade": "fail", "evidence": "Same repo domain (AI portfolio-review tool); PII-regex work has no EMS/medicine relevance"},
      {"name": "Reach", "grade": "pass", "evidence": "6 stars, 146 forks (classroom forks)"}
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/6",
    "checks": [
      {"name": "Maintained", "grade": "pass", "evidence": "Repo pushed_at 2026-09-16, ~13 days before today, within 30 days"},
      {"name": "Active", "grade": "pass", "evidence": "repo archived: false; no discontinuation comment"},
      {"name": "Actionable", "grade": "pass", "evidence": "One bounded bug (missing keyword indexing call + per-batch normalization) with a single named file `rag/retriever/hybrid.py`, described directly by the issue author who has COLLABORATOR association, plus an estimated-effort note (not a tracking list)"},
      {"name": "Confirmed dead-end", "grade": "pass", "evidence": "0 comments; no maintainer statement of difficulty (tier-2/'intermediate' label and 4-6h estimate are not an explicit hard/blocked statement)"},
      {"name": "Unassigned", "grade": "pass", "evidence": "assignees: []; comments: 0; no linked/mentioned PR found via search — fully unclaimed"},
      {"name": "AI policy", "grade": "pass", "evidence": "docs/CONTRIBUTING.md has no AI-use restriction — silence passes"},
      {"name": "Interest", "grade": "fail", "evidence": "RAG/hybrid-retrieval scoring bug in a portfolio-review tool — no EMS/medicine relevance"},
      {"name": "Reach", "grade": "pass", "evidence": "6 stars, 146 forks (classroom forks)"}
    ],
    "verdict": "accept"
  }
]
```

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**
16/20, 18/20, 20/20

[The agreement score of each run you did, in order. A single run is a complete answer if
only one run occurred. **The last score in your list must match the agreement line in the
`eval-run.txt` you committed** — that file is the record of your final run.]

**Issue analysis**

[One scored issue, identified by id (`issue-01` through `issue-20`; the `calib-`
issues are not scored). State your rubric's decision, the gold label, and the
reasoning that produced your rubric's result.]
issue-12 originally stated that it should be accepted when the gold label decision is reject. This is because I initially did not have a check to
ensure that AI contributions were allowed in that repo, which they are not. After adding the check, we now properly reject.

**Check rationale**

[One check from the `rubric.md` uploaded to `tools/issue-select/`, quoted as it is
currently written, with the reasoning behind its current form.]
"|Maintained|The github releases tab, recent commits pushed to branches, recent issues fixed, comments made|Improvements have been made in the last 30 days|Required|". This check is to ensure that the repo is actively being used so we aren't committing to a dead project.
**Trade-offs**

[What the quoted check gives up. Any one of these is a complete answer: an issue whose
result it changes, a canary you re-ran with `--only`, a case you accept it will miss, or a
stated reason nothing changed elsewhere. "Nothing changed, and here is how I know" earns
the point in full when the reason follows.]
I chose a cutoff of 30 days so
that the grader could be complete rather than rely on adjectives, but having such a hard cutoff point means I may miss projects that happen to fall just outside of the boundary.
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

The issue doesn't completely fit my interests, which lie in medicine, but I have prior experience with BM25 and have some familiarity with this debugging. It appears to be of medium difficulty but I am confident I will be able to complete it sucessfully. The grader was able to identify that the issue is well-described by the maintainer, but it ranked it lowest out of the three issues I considered. I personally decided that it was the best fit for me based on my additional interests that the grader did not know about, since it was prompted to only be aware of EMS/medicine relevance. I anticipate no difficulty in claiming it.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
