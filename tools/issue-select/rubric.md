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
|Maintained|The github releases tab, recent commits pushed to branches, recent issues fixed, comments made|Improvements have been made in the last 30 days|Required|
|Active|Whether the repo is in archived status; whether the author or a maintainer has commented that the project is discontinued, suspended, or looking for a new maintainer|Repo is not archived, and no comment states the project is discontinued or unmaintained|Required|
|Actionable|Whether the issue body describes one concrete change or is itself a list/index of many other issues; the issue body's reproduction steps and acceptance criteria; any "where to start" pointer to specific files or functions; maintainer-applied labels (e.g. good-first-issue, easy, help-wanted); the author association (MEMBER/COLLABORATOR/OWNER vs. NONE/CONTRIBUTOR) on any comment naming a technical cause|Fails if the issue's body is itself a tracking list or index of other issues to pick from, rather than a description of one bounded change. Otherwise passes if at least one of: the issue names a specific file or function to change, it gives clear reproduction steps plus expected vs. actual behavior, it carries a maintainer-applied good-first-issue-style label, or a maintainer/collaborator (not a random commenter) has named the specific technical cause(s) of the bug|Required|
|Confirmed dead-end|Comments and linked PRs on this specific issue, looking for explicit statements from a maintainer or contributor about difficulty|Fails only if a maintainer or contributor explicitly states the issue is hard, blocked, or requires deep internals knowledge. A linked PR being closed without merging, or the issue simply being old with no comments, is not by itself disqualifying. A pattern of many closed PRs with a visible churn pattern, however, is a valuable signal and should be denied.|Required|
|Unassigned|Assignee tab, claim comments, linked PRs|The issue should not already have another contributor working on it|Required|
|AI policy|The repo's contribution policy / CONTRIBUTING.md, specifically any section addressing AI-generated code, documentation, or tooling|Fails only if the policy states an outright ban on AI-generated code or documentation (e.g. "we do not accept AI-generated code or documentation"). A policy that permits AI tools under conditions (e.g. contributors must understand, test, and be able to explain the change) passes. No stated policy also passes.|Required|
|Interest|The description of the github repo, readme files, linked websites/papers, stated claims as to intended purpose|The issue should be directly related to applications in EMS/Medicine, or interdisciplinary fields such as the use of AI in medicine. Ideally should be linked to research papers/have relevance to the aforementioned scientific community|Preferred|
|Reach|Star count, watcher count, fork count|Higher ranks an accepted issue higher; there is no minimum required|Preferred|

## Verdict rule

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict, they
rank accepted issues; unclear counts as fail." -->
Accept if every required check passes. Preferred checks only rank accepted issues and do not exclude otherwise passing checks. If unclear, accept and bring up during ranking for manual human verification.