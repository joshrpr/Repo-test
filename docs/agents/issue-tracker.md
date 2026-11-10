# Issue tracker: GitHub

Issues and specs live in GitHub Issues for `joshrpr/Repo-test`.
Use the `gh` CLI from this clone.

## Operations

- Verify the target with `gh repo view --json nameWithOwner`.
- Create: `gh issue create --title "..." --body-file <file>`.
- Read: `gh issue view <number> --json number,title,body,labels,comments`.
- List: `gh issue list --state open`, with label filters as needed.
- Comment: `gh issue comment <number> --body-file <file>`.
- Label: `gh issue edit <number> --add-label "<label>"`.
- Remove a label: `gh issue edit <number> --remove-label "<label>"`.
- Close: post the explanation as a comment, then `gh issue close <number>`.

Use temporary UTF-8 files for multiline bodies and comments.

File issues in this repository. If gh resolves to another repository,
confirm the intended target with the user before creating an issue.

## Relationships

Use GitHub sub-issues for parent/child relationships. If unavailable,
put `Part of #<parent>` in the child and a task list in the parent.

Use native GitHub issue dependencies for blockers. If unavailable,
put `Blocked by: #<number>, #<number>` near the top of the child body.
A ticket is unblocked when all its blockers are closed.

## Pull requests as a triage surface

PRs as a request surface: no.

## Skill instructions

“Publish to the issue tracker” means create a GitHub issue.
“Fetch the relevant ticket” means read the referenced GitHub issue.

## Wayfinding operations

- Map: one issue labelled `wayfinder:map`, containing Notes,
  Decisions-so-far, and Fog.
- Child tickets: sub-issues labelled `wayfinder:<type>`, where type is
  research, prototype, grilling, or task.
- Frontier: open, unblocked, unassigned children; first in map order wins.
- Claim: assign the ticket to the driving developer before starting work.
- Resolve: comment with the answer, close the child, and append a short
  summary and link to the map's Decisions-so-far.
