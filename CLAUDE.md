# alpenglow-software-legal

Legal documents for Alpenglow Software apps. Today it holds one file, `index.md`: the privacy policy for Cap Counter, a water polo coaching app (effective May 7, 2026). GitHub Pages renders it from `main` at `https://benjrohrs.github.io/alpenglow-software-legal/`. This file is public, like the rest of the repo.

## Git

- Every change goes on its own branch and through a PR. Never push to `main`.
- GitHub enforces this here: `main` is protected (PR required, admins included, no force pushes or deletions), with 0 required reviews and no required status checks. There is no CI.
- Merge with `gh pr merge --squash --delete-branch`; no review is needed.
- Merging publishes: GitHub Pages rebuilds from `main` and the change is live within a few minutes.
- The repo's settings, including the branch protection, are managed by Terraform in Alpenglow's private infra repo; don't change them through the GitHub UI or API.
- Commands given to Ben go on one line, with no `\` continuations.

## Checks before merging

- No build step. Read the rendered Markdown in the PR's file view.
- Don't rename or move `index.md`: the published URL depends on it, and an App Store listing may link to it.
- When the policy text changes, update the effective date at the top.
- A change to a policy's substance (what data an app collects or where it goes) needs Ben's OK before merging. New documents for other apps are fine to propose in a PR.

## What a cloud session can't do

- Change App Store listings or the URLs they link to: that's Ben's.
- Read the design docs, which live on Ben's Mac. When a cloud session makes a decision worth recording, put it in the PR description so a Mac session can copy it into the docs.
- Never print secret values; check them by length or prefix only.
