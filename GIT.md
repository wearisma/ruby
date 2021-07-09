## Table of Contents
  1. [Create a PR](#create-a-pr)
  1. [Resolve merge conflicts](#resolve-merge-conflicts)

## Create a PR

 - Branch name
   - For features: `feature-blah` or `add-blah` 
   - For bug fix: `fix-blah`
   - For small update: `update-blah`
   - Note that our CI  not pick up branches with names starting with "feature/", "fix/" etc (anything with a slash in it). Lets not use this naming pattern for our branches. lets separate words in branch names with a hyphen.
 
 - PR message
   - Please write down a brief of PR changes, so that reviewer can understand what the PR is about easily.
   - Attach front-end screenshots if there's any front-end changes.
   - Write down migration script in the PR message if any.
 
 - After PR is created
   - Attach the PR to Trello card
   - Request reviewer to review your PR

## Resolve merge conflicts

We don’t normally use the merging mechanism because of how our releases work. We rebase.
Merging basically pulls the master branch commits to the current branch and then you can resolve the conflicts in a “merge commit”.

The problem is that it’s difficult to cherry-pick these merge commits.
Rebasing places your commits on the top of the lastest master.

```
git checkout master
git pull
git checkout <your branch>
git rebase master
```
While rebasing, some commits that result in conflict will pause for you to resolve them. You can follow the instructions in console. 
